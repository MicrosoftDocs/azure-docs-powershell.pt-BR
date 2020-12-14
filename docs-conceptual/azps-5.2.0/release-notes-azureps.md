---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 25d4df411c6df652170880c123e2fbdf24546193
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856065"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="47f15-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="47f15-103">Azure PowerShell release notes</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="47f15-104">5.2.0 – Dezembro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-104">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-105">Az.Accounts</span></span>
* <span data-ttu-id="47f15-106">Gerenciado para analisar o tempo de ExpiresOn do token bruto se não for possível obter da biblioteca subjacente</span><span class="sxs-lookup"><span data-stu-id="47f15-106">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="47f15-107">Mensagem de aviso aprimorada se a autenticação interativa não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="47f15-107">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-108">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-109">[Alteração da falha] 'New-AzApiManagementProduct', por padrão, não tem limite de assinatura.</span><span class="sxs-lookup"><span data-stu-id="47f15-109">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-110">Az.Compute</span></span>
* <span data-ttu-id="47f15-111">Get-AzVm editado para filtrar por '-Name' antes de verificar a limitação devido a muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="47f15-111">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="47f15-112">Novo cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span><span class="sxs-lookup"><span data-stu-id="47f15-112">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="47f15-113">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="47f15-113">Az.ContainerRegistry</span></span>
* <span data-ttu-id="47f15-114">Parâmetro 'Name' com suporte e valor da entrada de pipeline para 'Get-AzContainerRegistryUsage' [nº 13605]</span><span class="sxs-lookup"><span data-stu-id="47f15-114">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="47f15-115">Exceções refinadas para 'Connect-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="47f15-115">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-116">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-117">SDK do .NET do ADF atualizado para a versão 4.13.0</span><span class="sxs-lookup"><span data-stu-id="47f15-117">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="47f15-118">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="47f15-118">Az.HealthcareApis</span></span>
* <span data-ttu-id="47f15-119">Suporte adicionado para chaves gerenciadas pelo cliente</span><span class="sxs-lookup"><span data-stu-id="47f15-119">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-120">Az.IotHub</span></span>
* <span data-ttu-id="47f15-121">Problema de token SAS corrigido.</span><span class="sxs-lookup"><span data-stu-id="47f15-121">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-122">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-123">'Todos' com suporte como uma opção quando são definidas políticas de acesso do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="47f15-123">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="47f15-124">Nova versão com suporte do módulo do SecretManagement [nº 13366]</span><span class="sxs-lookup"><span data-stu-id="47f15-124">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="47f15-125">ByteArray, String, PSCredential e Hashtable com suporte para 'SecretValue' em SecretManagementModule [nº 12190]</span><span class="sxs-lookup"><span data-stu-id="47f15-125">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="47f15-126">[Alteração da falha] Superfície de API de cmdlets recriada com relação ao HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="47f15-126">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-127">Az.Monitor</span></span>
* <span data-ttu-id="47f15-128">Parâmetro 'Rule' de 'New-AzAutoscaleProfile' alterado para aceitar lista vazia.</span><span class="sxs-lookup"><span data-stu-id="47f15-128">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="47f15-129">[Nº 12903]</span><span class="sxs-lookup"><span data-stu-id="47f15-129">[#12903]</span></span>
* <span data-ttu-id="47f15-130">Adição de novos cmdlets para dar suporte à criação de configurações de diagnóstico mais flexíveis:</span><span class="sxs-lookup"><span data-stu-id="47f15-130">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="47f15-131">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="47f15-131">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="47f15-132">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="47f15-132">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="47f15-133">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="47f15-133">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-134">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-135">O texto de ajuda e o nome do conjunto de parâmetros foram alterados para o cmdlet 'Restore-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="47f15-135">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-136">Az.Resources</span></span>
* <span data-ttu-id="47f15-137">Suporte ao parâmetro '-Tag' adicionado para 'Set-AzTemplateSpec' e 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="47f15-137">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="47f15-138">Suporte à exibição de marcas adicionado para o formatador padrão para Especificações de Modelo</span><span class="sxs-lookup"><span data-stu-id="47f15-138">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-139">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-139">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-140">Exemplo adicionado para 'Set-AzServiceFabricSetting' com o parâmetro SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="47f15-140">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="47f15-141">Cmdlets relacionados a aplicativos atualizados para alertar que o suporte é apenas para recursos implantados do ARM</span><span class="sxs-lookup"><span data-stu-id="47f15-141">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="47f15-142">Cmdlets de certificado de cluster de 'Add-AzureRmServiceFabricClusterCertificate' e 'Remove-AzureRmServiceFabricClusterCertificate' marcados para substituição</span><span class="sxs-lookup"><span data-stu-id="47f15-142">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-143">Az.Sql</span></span>
* <span data-ttu-id="47f15-144">SecondaryType adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="47f15-144">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="47f15-145">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-145">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="47f15-146">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-146">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="47f15-147">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="47f15-147">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="47f15-148">HighAvailabilityReplicaCount adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="47f15-148">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="47f15-149">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-149">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="47f15-150">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-150">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="47f15-151">ReadReplicaCount tornado um alias de HighAvailabilityReplicaCount no seguinte:</span><span class="sxs-lookup"><span data-stu-id="47f15-151">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="47f15-152">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-152">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="47f15-153">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-153">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-154">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-154">Az.Storage</span></span>
* <span data-ttu-id="47f15-155">Upload de arquivos do Azure de até 4 TiB com suporte</span><span class="sxs-lookup"><span data-stu-id="47f15-155">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="47f15-156">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-156">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="47f15-157">Azure.Storage.Blobs atualizado para 12.7.0</span><span class="sxs-lookup"><span data-stu-id="47f15-157">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="47f15-158">Azure.Storage.Files.Shares atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="47f15-158">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="47f15-159">Azure.Storage.Files.DataLake atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="47f15-159">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="47f15-160">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="47f15-160">Az.StorageSync</span></span>
* <span data-ttu-id="47f15-161">Recurso de política de camadas de sincronização adicionado com política de download e modo de cache local</span><span class="sxs-lookup"><span data-stu-id="47f15-161">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-162">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-162">Az.Websites</span></span>
* <span data-ttu-id="47f15-163">Impedir regras de restrição de acesso duplicadas</span><span class="sxs-lookup"><span data-stu-id="47f15-163">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="47f15-164">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="47f15-164">Thanks to our community contributors</span></span>
* <span data-ttu-id="47f15-165">Andrew Dawson (@dawsonar802), por atualizar Get-AzKeyVaultCertificate.md – obter certificado e salvá-lo como seção pfx para trabalhar com o PowerShell Core (nº 13557)</span><span class="sxs-lookup"><span data-stu-id="47f15-165">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="47f15-166">@iviark, por atualizações de APIs de saúde BYOK do Powershell (nº 13518)</span><span class="sxs-lookup"><span data-stu-id="47f15-166">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="47f15-167">John Duckmanton (@johnduckmanton), por corrigir a ortografia de TagPatchOperation (nº 13508)</span><span class="sxs-lookup"><span data-stu-id="47f15-167">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="47f15-168">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="47f15-168">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="47f15-169">Ajuda organizada do Get-AzLogicAppRunHistory (nº 13513)</span><span class="sxs-lookup"><span data-stu-id="47f15-169">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="47f15-170">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="47f15-170">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="47f15-171">Atualizar Update-AzAppConfigurationStore.md (nº 13485)</span><span class="sxs-lookup"><span data-stu-id="47f15-171">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="47f15-172">Atualizar New-AzCosmosDBAccount.md (nº 13490)</span><span class="sxs-lookup"><span data-stu-id="47f15-172">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="47f15-173">@SteppingRazor, New-AzApiManagementProduct: alterar o valor padrão do parâmetro SubscriptionsLimit para nenhum (nº 13457)</span><span class="sxs-lookup"><span data-stu-id="47f15-173">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="47f15-174">Steve Burkett (@SteveBurkettNZ), por corrigir erros de digitação para o parâmetro WorkspaceResourceId no exemplo (nº 13589)</span><span class="sxs-lookup"><span data-stu-id="47f15-174">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="47f15-175">5.1.0 – Novembro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-175">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-176">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-176">Az.Accounts</span></span>
* <span data-ttu-id="47f15-177">Correção de um problema em que a TenantId podia não ser respeitada se 'Connect-AzAccount -DeviceCode' [nº 13477] fosse usado</span><span class="sxs-lookup"><span data-stu-id="47f15-177">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="47f15-178">Adição do novo cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="47f15-178">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="47f15-179">Correção de um problema que ocorria quando o caminho do perfil do usuário estava inacessível</span><span class="sxs-lookup"><span data-stu-id="47f15-179">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="47f15-180">Correção de um problema que causava o erro Write-Object durante Connect-AzAccount [nº 13419]</span><span class="sxs-lookup"><span data-stu-id="47f15-180">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="47f15-181">Adição do parâmetro 'ContainerRegistryEndpointSuffix' a: 'Add-AzEnvironment', 'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="47f15-181">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="47f15-182">Suporte à interrupção de logon com o clique em <kbd>CTRL</kbd>+<kbd>C</kbd></span><span class="sxs-lookup"><span data-stu-id="47f15-182">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="47f15-183">Correção de um problema que fazia com que 'Connect-AzAccount -KeyVaultAccessToken' não funcionasse [nº 13127]</span><span class="sxs-lookup"><span data-stu-id="47f15-183">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="47f15-184">Correção da referência nula e da não diferenciação de maiúsculas e minúsculas no método em 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="47f15-184">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-185">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-185">Az.Aks</span></span>
* <span data-ttu-id="47f15-186">Correção do problema em que o usuário não podia usar a entidade de serviço para criar um cluster do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="47f15-186">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="47f15-187">[nº 13012]</span><span class="sxs-lookup"><span data-stu-id="47f15-187">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="47f15-188">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-188">Az.AppConfiguration</span></span>
* <span data-ttu-id="47f15-189">Disponibilidade geral do módulo 'Az.AppConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-189">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-190">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-191">Aprimoramento da mensagem de erro do comando 'New-AzDataFactoryV2LinkedServiceEncryptedCredential'</span><span class="sxs-lookup"><span data-stu-id="47f15-191">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-192">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-192">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-193">Atualização do SDK do plano de dados do ADLS para 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="47f15-193">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="47f15-194">Alterações: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="47f15-194">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="47f15-195">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="47f15-195">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="47f15-196">Adição de novos cmdlets do Pacote MSIX e atualização de cmdlets de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="47f15-196">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-197">Az.EventHub</span></span>
* <span data-ttu-id="47f15-198">Correção de comandos do cluster EventHub sem marcas</span><span class="sxs-lookup"><span data-stu-id="47f15-198">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="47f15-199">Atualização do texto da Ajuda de PartnerNamespace dos comandos AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-199">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-200">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-200">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-201">Adição dos parâmetros 'ResourceProviderConnection' e 'PrivateLink' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de link privado e saída de retransmissão</span><span class="sxs-lookup"><span data-stu-id="47f15-201">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="47f15-202">Adição do parâmetro 'AmbariDatabase' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de banco de dados personalizado do Ambari</span><span class="sxs-lookup"><span data-stu-id="47f15-202">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="47f15-203">Adição do valor de aceitação de 'AmbariDatabase' ao parâmetro 'MetastoreType' do cmdlet 'Add-AzHDInsightMetastore'</span><span class="sxs-lookup"><span data-stu-id="47f15-203">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-204">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-204">Az.IotHub</span></span>
* <span data-ttu-id="47f15-205">Permissão de marcas no cmdlet create do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-205">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-206">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-206">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-207">Suporte à atualização de marcas do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="47f15-207">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="47f15-208">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47f15-208">Az.LogicApp</span></span>
* <span data-ttu-id="47f15-209">Correção de Get-AzLogicAppRunHistory, que só recuperava a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="47f15-209">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-210">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-210">Az.Network</span></span>
* <span data-ttu-id="47f15-211">Atualização do cmdlet indicado abaixo</span><span class="sxs-lookup"><span data-stu-id="47f15-211">Updated below cmdlet</span></span> 
    - <span data-ttu-id="47f15-212">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span><span class="sxs-lookup"><span data-stu-id="47f15-212">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="47f15-213">Adição da propriedade PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="47f15-213">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="47f15-214">Adição da propriedade PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="47f15-214">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="47f15-215">Adição de novas propriedades aos cmdlets a seguir para permitir o balanceamento de carga global</span><span class="sxs-lookup"><span data-stu-id="47f15-215">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="47f15-216">'New-AzLoadBalancer':</span><span class="sxs-lookup"><span data-stu-id="47f15-216">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="47f15-217">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="47f15-217">Added Sku Tier property</span></span>
    - <span data-ttu-id="47f15-218">'New-AzPuplicIpAddress':</span><span class="sxs-lookup"><span data-stu-id="47f15-218">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="47f15-219">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="47f15-219">Added Sku Tier property</span></span>
    - <span data-ttu-id="47f15-220">'New-AzPublicIpPrefix':</span><span class="sxs-lookup"><span data-stu-id="47f15-220">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="47f15-221">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="47f15-221">Added Sku Tier property</span></span>
    - <span data-ttu-id="47f15-222">'New-AzLoadBalancerBackendAddressConfig':</span><span class="sxs-lookup"><span data-stu-id="47f15-222">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="47f15-223">Adição da propriedade LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="47f15-223">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="47f15-224">Atualização do planejamento para preterir os avisos dos seguintes cmdlets: –'New-AzVirtualHubRoute'   –'New-AzVirtualHubRouteTable'   –'Add-AzVirtualHubRoute'   –'Add-AzVirtualHubRouteTable'   –'Get-AzVirtualHubRouteTable'   –'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="47f15-224">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="47f15-225">Adição do planejamento para preterir os avisos no argumento 'RouteTable' nos seguintes cmdlets: –'New-AzVirtualHub'   –'Set-AzVirtualHub'   –'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="47f15-225">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="47f15-226">Os argumentos '-MinScaleUnits' e '-MaxScaleUnits' passaram a ser opcionais em 'Set-AzExpressRouteGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-226">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="47f15-227">Adição de novos cmdlets para dar suporte à autenticação mútua e aos perfis SSL no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="47f15-227">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="47f15-228">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-228">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="47f15-229">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-229">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="47f15-230">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-230">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="47f15-231">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-231">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="47f15-232">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-232">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="47f15-233">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-233">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="47f15-234">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-234">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="47f15-235">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-235">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="47f15-236">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-236">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="47f15-237">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-237">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="47f15-238">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-238">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="47f15-239">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-239">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="47f15-240">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-240">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="47f15-241">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-241">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="47f15-242">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-242">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="47f15-243">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-243">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="47f15-244">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-244">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-245">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-245">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-246">A especificação do BackupTime da política está em UTC.</span><span class="sxs-lookup"><span data-stu-id="47f15-246">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="47f15-247">Modificação do aviso de alteração da falha no cmdlet Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="47f15-247">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="47f15-248">Atualização do texto da Ajuda do script de exemplo para o cmdlet Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="47f15-248">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-249">Az.Resources</span></span>
* <span data-ttu-id="47f15-250">Correção de um problema em que What-If mostrava dois escopos de grupo de recursos com usos diferentes de maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="47f15-250">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="47f15-251">Atualização de 'Export-AzResourceGroup' para uso do SDK.</span><span class="sxs-lookup"><span data-stu-id="47f15-251">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="47f15-252">Adição de informações de cultura aos métodos de análise</span><span class="sxs-lookup"><span data-stu-id="47f15-252">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-253">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-253">Az.Sql</span></span>
* <span data-ttu-id="47f15-254">Correção de problemas em que Set-AzSqlDatabaseAudit não dava suporte ao banco de dados de Hiperescala e em que não era possível determinar a edição do banco de dados</span><span class="sxs-lookup"><span data-stu-id="47f15-254">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="47f15-255">Adição de MaintenanceConfigurationId a 'New-AzSqlInstance' e 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="47f15-255">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="47f15-256">Correção de um bug em GetAzureSqlDatabaseReplicationLink.cs, em que o parâmetro PartnerServerName era verificado por valor em vez de chave</span><span class="sxs-lookup"><span data-stu-id="47f15-256">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-257">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-257">Az.Websites</span></span>
* <span data-ttu-id="47f15-258">Adição de suporte para novos recursos de restrição de acesso: ServiceTag, multi-ip e http-headers</span><span class="sxs-lookup"><span data-stu-id="47f15-258">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="47f15-259">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="47f15-259">Thanks to our community contributors</span></span>
* <span data-ttu-id="47f15-260">John Q. Martin (@johnmart82) – Adição de informações de pré-requisitos do firewall (nº 13385)</span><span class="sxs-lookup"><span data-stu-id="47f15-260">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="47f15-261">Manikandan Duraisamy (@madurais-msft) – Correção do argumento PublicSubnetName (nº 13417)</span><span class="sxs-lookup"><span data-stu-id="47f15-261">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="47f15-262">@mahortas – Atualização dos valores do parâmetro -HostNames (nº 13349)</span><span class="sxs-lookup"><span data-stu-id="47f15-262">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="47f15-263">@MariachiForHire – Adição de valores compatíveis com TrafficAnalyticsInterval (nº 13304)</span><span class="sxs-lookup"><span data-stu-id="47f15-263">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="47f15-264">Michael James (@mikejwhat) – permissão para que Get-AzLogicAppRunHistory retorne mais de 30 entradas (nº 13393)</span><span class="sxs-lookup"><span data-stu-id="47f15-264">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="47f15-265">Shashikant Shakya (@shshakya) – Atualização de Restore-AzSqlInstanceDatabase.md (nº 13404)</span><span class="sxs-lookup"><span data-stu-id="47f15-265">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="47f15-266">5.0.0 – outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-266">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-267">Az.Accounts</span></span>
* <span data-ttu-id="47f15-268">[Alteração da Falha] Remoção de 'Get-AzProfile' e 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-268">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="47f15-269">Substituição da Biblioteca de Autenticação do Azure Directory pela MSAL (Biblioteca de Autenticação da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47f15-269">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-270">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-270">Az.Aks</span></span>
* <span data-ttu-id="47f15-271">[Alteração da Falha] Remoção do alias do parâmetro 'ClientIdAndSecret' em 'New-AzAksCluster' e 'Set-AzAksCluster'.</span><span class="sxs-lookup"><span data-stu-id="47f15-271">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="47f15-272">[Alteração da Falha] Alteração do valor padrão de 'NodeVmSetType' em 'New-AzAksCluster' de 'AvailabilitySet' para 'VirtualMachineScaleSets'.</span><span class="sxs-lookup"><span data-stu-id="47f15-272">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="47f15-273">[Alteração da Falha] Alteração do valor padrão de 'NetworkPlugin' em 'New-AzAksCluster' de 'None' para 'azure'.</span><span class="sxs-lookup"><span data-stu-id="47f15-273">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="47f15-274">[Alteração da Falha] Remoção do parâmetro 'NodeOsType' em 'New-AzAksCluster', pois ele é compatível somente com um valor Linux.</span><span class="sxs-lookup"><span data-stu-id="47f15-274">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="47f15-275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="47f15-275">Az.Billing</span></span>
* <span data-ttu-id="47f15-276">Adição do cmdlet 'Get-AzBillingAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-276">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="47f15-277">Adição do cmdlet 'Get-AzBillingProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-277">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="47f15-278">Adição do cmdlet 'Get-AzInvoiceSection'</span><span class="sxs-lookup"><span data-stu-id="47f15-278">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="47f15-279">Adição de novos parâmetros ao cmdlet 'Get-AzBillingInvoice'</span><span class="sxs-lookup"><span data-stu-id="47f15-279">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="47f15-280">Remoção das propriedades DownloadUrlExpiry, Type e BillingPeriodNames da resposta do cmdlet Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="47f15-280">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-281">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-281">Az.Cdn</span></span>
* <span data-ttu-id="47f15-282">Adição de cmdlets para dar suporte a uma funcionalidade de link privado e várias origens</span><span class="sxs-lookup"><span data-stu-id="47f15-282">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-283">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-284">Atualização do SDK para 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="47f15-284">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-285">Az.Compute</span></span>
* <span data-ttu-id="47f15-286">Adição do parâmetro '-VmssId ' ao 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="47f15-286">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="47f15-287">Adição do parâmetro 'PlatformFaultDomainCount' ao cmdlet 'New-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="47f15-287">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="47f15-288">Novo cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="47f15-288">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="47f15-289">Adição dos parâmetros opcionais 'Tier' e 'LogicalSectorSize' ao cmdlet New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="47f15-289">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="47f15-290">Adição dos parâmetros opcionais 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' e 'DiskMBpsReadOnly' ao cmdlet 'New-AzDiskUpdateConfig'.</span><span class="sxs-lookup"><span data-stu-id="47f15-290">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="47f15-291">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="47f15-291">Az.ContainerRegistry</span></span>
* <span data-ttu-id="47f15-292">[Alteração da Falha] Atualiza a versão da API para a 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="47f15-292">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="47f15-293">[Alteração da Falha] Remoção do SKU 'Classic' e do parâmetro 'StorageAccountName' de 'New-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="47f15-293">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="47f15-294">Adição de novos cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule' e 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="47f15-294">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="47f15-295">Adição do novo parâmetro 'NetworkRuleSet' ao 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="47f15-295">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="47f15-296">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="47f15-296">Az.Databricks</span></span>
* <span data-ttu-id="47f15-297">Correção de um bug que pode causar a atualização do workspace do Databricks sem que ocorra falha do `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="47f15-297">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-298">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-298">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-299">Atualização do SDK do .NET do ADF para a versão 4.12.0</span><span class="sxs-lookup"><span data-stu-id="47f15-299">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="47f15-300">Atualização do SDK cliente da criptografia do ADF para a versão 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="47f15-300">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="47f15-301">Adição dos comandos 'Stop-AzDataFactoryV2TriggerRun' e 'Invoke-AzDataFactoryV2TriggerRun'</span><span class="sxs-lookup"><span data-stu-id="47f15-301">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="47f15-302">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="47f15-302">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="47f15-303">Exigir a propriedade Location para criar objetos ARM de nível superior.</span><span class="sxs-lookup"><span data-stu-id="47f15-303">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="47f15-304">\* `ApplicationGroupType` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="47f15-304">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="47f15-305">\* `HostPoolArmPath` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="47f15-305">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="47f15-306">\* Adição do `PreferredAppGroupType` ao `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="47f15-306">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="47f15-307">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="47f15-307">Az.Functions</span></span>
* <span data-ttu-id="47f15-308">[Alteração da Falha] Remoção do parâmetro de opção 'IncludeSlot' de todos os parâmetros, exceto de um conjunto de parâmetros de 'Get-AzFunctionApp'.</span><span class="sxs-lookup"><span data-stu-id="47f15-308">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="47f15-309">O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados em que '-IncludeSlot' for especificado.</span><span class="sxs-lookup"><span data-stu-id="47f15-309">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="47f15-310">Atualização do 'New-AzFunctionApp':</span><span class="sxs-lookup"><span data-stu-id="47f15-310">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="47f15-311">Correção do -DisableApplicationInsights para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.</span><span class="sxs-lookup"><span data-stu-id="47f15-311">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="47f15-312">[Nº 12728]</span><span class="sxs-lookup"><span data-stu-id="47f15-312">[#12728]</span></span>
  - <span data-ttu-id="47f15-313">[Alteração da Falha] Remoção do suporte para criar aplicativos de funções do PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="47f15-313">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="47f15-314">[Alteração da Falha] Alteração da versão de runtime padrão da 6.2 para a 7.0 do Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="47f15-314">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="47f15-315">[Alteração da Falha] Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="47f15-315">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="47f15-316">[Alteração da Falha] Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="47f15-316">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-317">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-317">Az.HDInsight</span></span>
 * <span data-ttu-id="47f15-318">Para o cmdlet New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="47f15-318">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="47f15-319">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="47f15-319">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="47f15-320">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-320">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="47f15-321">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="47f15-321">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="47f15-322">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="47f15-322">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="47f15-323">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="47f15-323">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="47f15-324">Adição de novos parâmetros: 'StorageFileSystem' e 'StorageAccountManagedIdentity' para dar suporte ao ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="47f15-324">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="47f15-325">Adição do novo parâmetro 'EnableIDBroker' para dar suporte ao Agente de IDs do HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-325">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="47f15-326">Adição de novos parâmetros: Parâmetros 'KafkaClientGroupId', 'KafkaClientGroupName' e 'KafkaManagementNodeSize' para dar suporte ao Proxy REST do Kafka</span><span class="sxs-lookup"><span data-stu-id="47f15-326">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="47f15-327">Para o cmdlet New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="47f15-327">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="47f15-328">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="47f15-328">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="47f15-329">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-329">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="47f15-330">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="47f15-330">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="47f15-331">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="47f15-331">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="47f15-332">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="47f15-332">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="47f15-333">Para o cmdlet Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="47f15-333">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="47f15-334">Substituição do parâmetro 'StorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="47f15-334">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="47f15-335">Para o cmdlet Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="47f15-335">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="47f15-336">Substituição do parâmetro 'Domain' por 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="47f15-336">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="47f15-337">Remoção do requisito obrigatório para o parâmetro 'OrganizationalUnitDN'</span><span class="sxs-lookup"><span data-stu-id="47f15-337">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-338">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-338">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-339">[Alteração da Falha] O parâmetro DisableSoftDelete foi preterido em 'New-AzKeyVault', bem como EnableSoftDelete em 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="47f15-339">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="47f15-340">[Alteração da Falha] Remoção do atributo SecretValueText para evitar a exibição de SecretValue de modo direto [Nº 12266]</span><span class="sxs-lookup"><span data-stu-id="47f15-340">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="47f15-341">Um novo tipo de recurso é compatível: HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="47f15-341">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="47f15-342">Comandos CRUD de cmdlets e do HSM gerenciado para operar chaves no HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="47f15-342">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="47f15-343">Backup/restauração completos do HSM, criação de chave AES, backup/restauração do domínio de segurança e RBAC</span><span class="sxs-lookup"><span data-stu-id="47f15-343">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="47f15-344">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="47f15-344">Az.ManagedServices</span></span>
* <span data-ttu-id="47f15-345">[Alteração da Falha] Atualização de parâmetros de convenções de nomenclatura e exemplos associados</span><span class="sxs-lookup"><span data-stu-id="47f15-345">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-346">Az.Network</span></span>
* <span data-ttu-id="47f15-347">[Alteração da Falha] Remoção do parâmetro 'HostedSubnet' e adição de 'Subnet' como alternativa</span><span class="sxs-lookup"><span data-stu-id="47f15-347">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="47f15-348">Adição de novos cmdlets às Rotas do Par no Nível do Roteador Virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-348">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="47f15-349">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="47f15-349">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="47f15-350">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="47f15-350">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="47f15-351">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="47f15-351">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="47f15-352">Adição do parâmetro '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="47f15-352">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="47f15-353">Adição do parâmetro '-SkuName' e, para isso, o SKU foi executado com um Alias</span><span class="sxs-lookup"><span data-stu-id="47f15-353">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="47f15-354">Remoção do parâmetro '-Sku'</span><span class="sxs-lookup"><span data-stu-id="47f15-354">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="47f15-355">[Alteração da Falha] O argumento 'Connectionlink' agora é obrigatório em 'Start-AzVpnConnectionPacketCapture' e 'Stop-AzVpnConnectionPacketCapture'</span><span class="sxs-lookup"><span data-stu-id="47f15-355">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="47f15-356">[Alteração da Falha] Atualização do 'New-AzNetworkWatcherConnectionMonitorEndPointObject' para remover o parâmetro '-Filter'</span><span class="sxs-lookup"><span data-stu-id="47f15-356">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="47f15-357">[Alteração da Falha] Substituição do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' por 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="47f15-357">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="47f15-358">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndPointObject':</span><span class="sxs-lookup"><span data-stu-id="47f15-358">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="47f15-359">Adição do parâmetro '-Type'</span><span class="sxs-lookup"><span data-stu-id="47f15-359">Added parameter '-Type'</span></span>
    - <span data-ttu-id="47f15-360">Adição do parâmetro '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="47f15-360">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="47f15-361">Adição do parâmetro '-Scope'</span><span class="sxs-lookup"><span data-stu-id="47f15-361">Added parameter '-Scope'</span></span>
* <span data-ttu-id="47f15-362">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' com o novo parâmetro '-DestinationPortBehavior'</span><span class="sxs-lookup"><span data-stu-id="47f15-362">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-363">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-363">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-364">Correção da Restauração da Carga de Trabalho para permissões de colaborador.</span><span class="sxs-lookup"><span data-stu-id="47f15-364">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="47f15-365">Adição de novos conjuntos e novas validações de parâmetros ao cmdlet Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="47f15-365">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-366">Az.Resources</span></span>
* <span data-ttu-id="47f15-367">Correção de um bug de análise</span><span class="sxs-lookup"><span data-stu-id="47f15-367">Fixed parsing bug</span></span>
* <span data-ttu-id="47f15-368">Atualização de cmdlets What-If do modelo do ARM para remover uma mensagem de visualização dos resultados</span><span class="sxs-lookup"><span data-stu-id="47f15-368">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="47f15-369">Correção de um problema em que ocorria falha nos cmdlets de implantação de modelo caso '-WhatIf' fosse definido em um escopo maior [Nº13038]</span><span class="sxs-lookup"><span data-stu-id="47f15-369">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="47f15-370">Correção de um problema em que cmdlets de implantação de modelo não preservavam maiúsculas e minúsculas para parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="47f15-370">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="47f15-371">Adição de uma versão de API padrão para ser usada no cmdlet 'Export-AzResourceGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-371">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="47f15-372">Adição de cmdlets às Especificações de Modelo ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec' e 'Export-AzTemplateSpec')</span><span class="sxs-lookup"><span data-stu-id="47f15-372">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="47f15-373">Adição de um suporte para implantar Especificações de Modelo usando cmdlets de implantação existentes (por meio do novo parâmetro -TemplateSpecId)</span><span class="sxs-lookup"><span data-stu-id="47f15-373">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="47f15-374">Atualização do parâmetro 'Get-AzResourceGroupDeploymentOperation' para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="47f15-374">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="47f15-375">Remoção do parâmetro '-ApiVersion' de cmdlets '\*-AzDeployment'.</span><span class="sxs-lookup"><span data-stu-id="47f15-375">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-376">Az.Sql</span></span>
* <span data-ttu-id="47f15-377">Correção de um problema em que ocorria uma falha de New-AzSqlDatabaseExport caso networkIsolation não fosse especificado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="47f15-377">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="47f15-378">Correção de um problema em que New-AzSqlDatabaseExport e New-AzSqlDatabaseImport não retornavam OperationStatusLink no objeto de resultado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="47f15-378">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="47f15-379">Atualizar a URL de regiões emparelhadas do Azure em avisos de redundância de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="47f15-379">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="47f15-380">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-380">Az.Storage</span></span>
* <span data-ttu-id="47f15-381">Remoção da propriedade obsoleta RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="47f15-381">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="47f15-382">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-382">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="47f15-383">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-383">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="47f15-384">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-384">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="47f15-385">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-385">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="47f15-386">Alterar o Tipo de DaysAfterModificationGreaterThan de int para int?</span><span class="sxs-lookup"><span data-stu-id="47f15-386">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="47f15-387">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-387">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="47f15-388">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-388">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="47f15-389">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="47f15-389">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="47f15-390">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="47f15-390">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="47f15-391">Criação/atualização de compartilhamento de arquivo compatível com uma camada de acesso</span><span class="sxs-lookup"><span data-stu-id="47f15-391">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="47f15-392">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="47f15-392">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="47f15-393">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="47f15-393">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="47f15-394">Definição/atualização/removção recursiva de ACL compatível com um item do Datalake Gen2</span><span class="sxs-lookup"><span data-stu-id="47f15-394">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="47f15-395">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="47f15-395">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="47f15-396">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="47f15-396">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="47f15-397">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="47f15-397">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="47f15-398">Política de acesso de Contêiner compatível com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="47f15-398">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="47f15-399">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-399">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="47f15-400">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-400">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="47f15-401">Alteração da saída do cmdlet da política de acesso ao Contêiner get/set mudando o tipo de Permissão de propriedade filho de enum para String</span><span class="sxs-lookup"><span data-stu-id="47f15-401">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="47f15-402">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-402">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="47f15-403">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-403">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="47f15-404">Correção de um problema do script de exemplo da política de gerenciamento de conjuntos com JSON</span><span class="sxs-lookup"><span data-stu-id="47f15-404">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="47f15-405">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-405">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-406">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-406">Az.Websites</span></span>
* <span data-ttu-id="47f15-407">Adição de suporte para o tipo de preço Premium V3</span><span class="sxs-lookup"><span data-stu-id="47f15-407">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="47f15-408">Atualização do SDK de Sites para a versão 3.1.0</span><span class="sxs-lookup"><span data-stu-id="47f15-408">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="47f15-409">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="47f15-409">Thanks to our community contributors</span></span>
* <span data-ttu-id="47f15-410">@atul-ram, por atualizar Get-AzDelegation.md (nº 13176)</span><span class="sxs-lookup"><span data-stu-id="47f15-410">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="47f15-411">@dineshreddy007, por obter as Funções de Aplicativos atribuídas de modo correto em caso de registro do Stack HCI usando um token WAC.</span><span class="sxs-lookup"><span data-stu-id="47f15-411">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="47f15-412">(nº 13249)</span><span class="sxs-lookup"><span data-stu-id="47f15-412">(#13249)</span></span>
* <span data-ttu-id="47f15-413">@kongou-ae, por atualizar New-AzOffice365PolicyProperty.md (nº 13217)</span><span class="sxs-lookup"><span data-stu-id="47f15-413">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="47f15-414">Lohith Chowdary Chilukuri (@Lochiluk), por atualizar Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="47f15-414">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="47f15-415">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="47f15-415">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="47f15-416">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13203)</span><span class="sxs-lookup"><span data-stu-id="47f15-416">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="47f15-417">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13190)</span><span class="sxs-lookup"><span data-stu-id="47f15-417">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="47f15-418">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13189)</span><span class="sxs-lookup"><span data-stu-id="47f15-418">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="47f15-419">Adicionar links aos cmdlets referenciados (nº 13137)</span><span class="sxs-lookup"><span data-stu-id="47f15-419">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="47f15-420">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13204)</span><span class="sxs-lookup"><span data-stu-id="47f15-420">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="47f15-421">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13205)</span><span class="sxs-lookup"><span data-stu-id="47f15-421">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="47f15-422">4.8.0 – Outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-422">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-423">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-423">Az.Accounts</span></span>
* <span data-ttu-id="47f15-424">Foi corrigido um problema de análise de datetime em bibliotecas comuns [#13045]</span><span class="sxs-lookup"><span data-stu-id="47f15-424">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-425">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-425">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-426">Foi adicionado o cmdlet 'New-AzCognitiveServicesAccountApiProperty'.</span><span class="sxs-lookup"><span data-stu-id="47f15-426">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="47f15-427">Parâmetro 'ApiProperty' compatível com 'New-AzCognitiveServicesAccount' e 'Set-AzCognitiveServicesAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-427">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-428">Az.Compute</span></span>
* <span data-ttu-id="47f15-429">Foi corrigido o problema em 'Update-ASRRecoveryPlan' populando o FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="47f15-429">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="47f15-430">Foram adicionados os parâmetros opcionais '-Top' e '-OrderBy' ao cmdlet 'Get-AzVmImage'.</span><span class="sxs-lookup"><span data-stu-id="47f15-430">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="47f15-431">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="47f15-431">Az.Databricks</span></span>
* <span data-ttu-id="47f15-432">Disponibilidade geral do módulo 'Az.Databricks'</span><span class="sxs-lookup"><span data-stu-id="47f15-432">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="47f15-433">Foi adicionado suporte para emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-433">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-434">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-434">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-435">Foi corrigido erro de digitação nas mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="47f15-435">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-436">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-436">Az.EventHub</span></span>
* <span data-ttu-id="47f15-437">Foi adicionado o parâmetro de opção opcional 'TrustedServiceAccessEnabled' ao cmdlet 'Set-AzEventHubNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="47f15-437">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-438">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-438">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-439">Foi adicionada uma mensagem de aviso para planejamento do preterimento dos parâmetros 'PublicNetworkAccessType' e 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="47f15-439">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="47f15-440">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="47f15-440">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="47f15-441">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-441">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="47f15-442">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="47f15-442">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="47f15-443">Adicionada mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageContainer' por 'StorageContainer'</span><span class="sxs-lookup"><span data-stu-id="47f15-443">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="47f15-444">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageRootPath' por 'StorageRootPath'</span><span class="sxs-lookup"><span data-stu-id="47f15-444">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-445">Az.IotHub</span></span>
* <span data-ttu-id="47f15-446">O SDK de dispositivos foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="47f15-446">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-447">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-448">A data detalhada da remoção da propriedade SecretValueText foi fornecida</span><span class="sxs-lookup"><span data-stu-id="47f15-448">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="47f15-449">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="47f15-449">Az.ManagedServices</span></span>
* <span data-ttu-id="47f15-450">Os avisos de alteração da falha nos cmdlets de definição e atribuição de serviços gerenciados foram atualizados</span><span class="sxs-lookup"><span data-stu-id="47f15-450">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-451">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-451">Az.Monitor</span></span>
* <span data-ttu-id="47f15-452">Foi corrigido o bug que fazia com que a mensagem de aviso não pudesse ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="47f15-452">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="47f15-453">[#12889]</span><span class="sxs-lookup"><span data-stu-id="47f15-453">[#12889]</span></span>
* <span data-ttu-id="47f15-454">Parâmetro 'SkipMetricValidation' com suporte nos critérios da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="47f15-454">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="47f15-455">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação da métrica seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="47f15-455">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-456">Az.Network</span></span>
* <span data-ttu-id="47f15-457">Política do Office365 adicionada ao recurso VPNSite</span><span class="sxs-lookup"><span data-stu-id="47f15-457">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="47f15-458">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-458">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-459">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-459">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-460">Foi adicionada a validação do nome do contêiner para backup da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="47f15-460">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="47f15-461">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47f15-461">Az.RedisCache</span></span>
* <span data-ttu-id="47f15-462">Correção dos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache' para não falharem devido a um problema de permissão relacionado ao registro do RP do Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="47f15-462">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-463">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-463">Az.Sql</span></span>
* <span data-ttu-id="47f15-464">Foi adicionado BackupStorageRedundancy ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="47f15-464">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="47f15-465">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-465">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="47f15-466">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="47f15-466">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="47f15-467">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="47f15-467">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="47f15-468">Foi removida a diferenciação de maiúsculas e minúsculas para o parâmetro BackupStorageRedundancy em todas as referências de Banco de Dados SQL</span><span class="sxs-lookup"><span data-stu-id="47f15-468">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="47f15-469">Foram atualizados os nomes das mensagens de aviso do BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="47f15-469">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-470">Az.Storage</span></span>
* <span data-ttu-id="47f15-471">Suporte para habilitar/desabilitar/obter propriedades de exclusão reversível de compartilhamento no serviço de arquivo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-471">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="47f15-472">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-472">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="47f15-473">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-473">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="47f15-474">Os compartilhamentos de arquivos de lista com suporte incluem os excluídos de uma conta de armazenamento e obtêm uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="47f15-474">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="47f15-475">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-475">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="47f15-476">Suporte para restauração de um compartilhamento de arquivo excluído</span><span class="sxs-lookup"><span data-stu-id="47f15-476">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="47f15-477">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="47f15-477">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="47f15-478">Foram alterados os cmdlets para modificar as propriedades do serviço blobs, não obtendo as propriedades originais do servidor, mas apenas definindo as propriedades modificadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="47f15-478">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="47f15-479">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-479">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="47f15-480">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-480">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="47f15-481">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-481">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="47f15-482">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-482">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="47f15-483">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-483">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="47f15-484">Foi corrigido o problema de ajuda para o valor padrão do tipo do parâmetro New-AzStorageAccount [#12189]</span><span class="sxs-lookup"><span data-stu-id="47f15-484">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="47f15-485">Foi corrigido o problema adicionando exemplo para mostrar como definir o ContentType correto no upload do blob [#12989]</span><span class="sxs-lookup"><span data-stu-id="47f15-485">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="47f15-486">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-486">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-487">Az.Accounts</span></span>
* <span data-ttu-id="47f15-488">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="47f15-488">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="47f15-489">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="47f15-489">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-490">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-490">Az.Aks</span></span>
* <span data-ttu-id="47f15-491">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="47f15-491">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="47f15-492">[#12372]</span><span class="sxs-lookup"><span data-stu-id="47f15-492">[#12372]</span></span>
* <span data-ttu-id="47f15-493">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-493">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="47f15-494">[#11239]</span><span class="sxs-lookup"><span data-stu-id="47f15-494">[#11239]</span></span>
* <span data-ttu-id="47f15-495">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="47f15-495">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="47f15-496">[#11239]</span><span class="sxs-lookup"><span data-stu-id="47f15-496">[#11239]</span></span>
* <span data-ttu-id="47f15-497">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-497">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="47f15-498">[#12371]</span><span class="sxs-lookup"><span data-stu-id="47f15-498">[#12371]</span></span>
* <span data-ttu-id="47f15-499">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="47f15-499">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-500">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-500">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-501">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="47f15-501">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-502">Az.Compute</span></span>
* <span data-ttu-id="47f15-503">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-503">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="47f15-504">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="47f15-504">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="47f15-505">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-505">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="47f15-506">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-506">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="47f15-507">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47f15-507">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="47f15-508">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="47f15-508">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="47f15-509">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="47f15-509">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="47f15-510">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-510">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="47f15-511">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-511">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="47f15-512">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="47f15-512">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-513">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-513">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-514">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="47f15-514">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-515">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-515">Az.EventHub</span></span>
* <span data-ttu-id="47f15-516">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="47f15-516">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="47f15-517">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="47f15-517">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="47f15-518">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="47f15-518">Az.Functions</span></span>
* <span data-ttu-id="47f15-519">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="47f15-519">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="47f15-520">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="47f15-520">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="47f15-521">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="47f15-521">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-522">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-523">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="47f15-523">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="47f15-524">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="47f15-524">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="47f15-525">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="47f15-525">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="47f15-526">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-526">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="47f15-527">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-527">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="47f15-528">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-528">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="47f15-529">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-529">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="47f15-530">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="47f15-530">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-531">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-532">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="47f15-532">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="47f15-533">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="47f15-533">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="47f15-534">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="47f15-534">Az.Kusto</span></span>
* <span data-ttu-id="47f15-535">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="47f15-535">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-536">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-536">Az.Network</span></span>
* <span data-ttu-id="47f15-537">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-537">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="47f15-538">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="47f15-538">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="47f15-539">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="47f15-539">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="47f15-540">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="47f15-540">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="47f15-541">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="47f15-541">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="47f15-542">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-542">Added subscription level parameter set</span></span>
    - <span data-ttu-id="47f15-543">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="47f15-543">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="47f15-544">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="47f15-544">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="47f15-545">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="47f15-545">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="47f15-546">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="47f15-546">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="47f15-547">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-547">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="47f15-548">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="47f15-548">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="47f15-549">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="47f15-549">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="47f15-550">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="47f15-550">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="47f15-551">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-551">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="47f15-552">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="47f15-552">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="47f15-553">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="47f15-553">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="47f15-554">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="47f15-554">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="47f15-555">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="47f15-555">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="47f15-556">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="47f15-556">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="47f15-557">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="47f15-557">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="47f15-558">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="47f15-558">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="47f15-559">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="47f15-559">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="47f15-560">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="47f15-560">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-561">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-561">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-562">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="47f15-562">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-563">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-563">Az.Resources</span></span>
* <span data-ttu-id="47f15-564">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="47f15-564">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="47f15-565">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="47f15-565">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="47f15-566">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="47f15-566">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="47f15-567">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="47f15-567">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-568">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-568">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-569">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="47f15-569">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="47f15-570">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="47f15-570">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="47f15-571">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="47f15-571">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="47f15-572">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="47f15-572">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="47f15-573">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="47f15-573">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="47f15-574">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-574">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="47f15-575">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-575">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="47f15-576">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="47f15-576">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="47f15-577">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="47f15-577">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="47f15-578">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="47f15-578">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="47f15-579">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="47f15-579">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="47f15-580">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="47f15-580">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="47f15-581">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="47f15-581">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="47f15-582">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="47f15-582">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="47f15-583">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="47f15-583">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="47f15-584">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="47f15-584">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-585">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-585">Az.Sql</span></span>
* <span data-ttu-id="47f15-586">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="47f15-586">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="47f15-587">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-587">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="47f15-588">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-588">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="47f15-589">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="47f15-589">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="47f15-590">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-590">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="47f15-591">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="47f15-591">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="47f15-592">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="47f15-592">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="47f15-593">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="47f15-593">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="47f15-594">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="47f15-594">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="47f15-595">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-595">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="47f15-596">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-596">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="47f15-597">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-597">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="47f15-598">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="47f15-598">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="47f15-599">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-599">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="47f15-600">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="47f15-600">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="47f15-601">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-601">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="47f15-602">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="47f15-602">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="47f15-603">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="47f15-603">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-604">Az.Storage</span></span>
* <span data-ttu-id="47f15-605">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="47f15-605">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="47f15-606">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="47f15-606">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="47f15-607">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-607">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="47f15-608">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-608">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="47f15-609">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="47f15-609">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="47f15-610">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="47f15-610">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="47f15-611">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="47f15-611">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="47f15-612">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-612">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="47f15-613">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="47f15-613">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="47f15-614">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-614">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="47f15-615">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-615">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="47f15-616">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-616">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="47f15-617">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-617">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="47f15-618">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="47f15-618">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="47f15-619">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="47f15-619">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="47f15-620">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="47f15-620">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="47f15-621">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="47f15-621">Thanks to our community contributors</span></span>
* <span data-ttu-id="47f15-622">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="47f15-622">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="47f15-623">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="47f15-623">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="47f15-624">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="47f15-624">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="47f15-625">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="47f15-625">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="47f15-626">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="47f15-626">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="47f15-627">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="47f15-627">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="47f15-628">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="47f15-628">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="47f15-629">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="47f15-629">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="47f15-630">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="47f15-630">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="47f15-631">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="47f15-631">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="47f15-632">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="47f15-632">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="47f15-633">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-633">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="47f15-634">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-634">Az.Compute</span></span>
* <span data-ttu-id="47f15-635">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="47f15-635">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="47f15-636">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-636">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-637">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-637">Az.Accounts</span></span>
* <span data-ttu-id="47f15-638">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="47f15-638">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="47f15-639">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="47f15-639">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-640">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-640">Az.Automation</span></span>
* <span data-ttu-id="47f15-641">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="47f15-641">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-642">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-642">Az.Compute</span></span>
* <span data-ttu-id="47f15-643">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="47f15-643">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="47f15-644">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="47f15-644">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="47f15-645">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-645">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="47f15-646">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="47f15-646">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-647">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-647">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-648">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="47f15-648">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-649">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-650">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="47f15-650">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-651">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-652">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="47f15-652">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="47f15-653">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="47f15-653">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="47f15-654">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="47f15-654">Az.Maintenance</span></span>
* <span data-ttu-id="47f15-655">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-655">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="47f15-656">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-656">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="47f15-657">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="47f15-657">Az.ManagedServices</span></span>
* <span data-ttu-id="47f15-658">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="47f15-658">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-659">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-659">Az.Monitor</span></span>
* <span data-ttu-id="47f15-660">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="47f15-660">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="47f15-661">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="47f15-661">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-662">Az.Resources</span></span>
* <span data-ttu-id="47f15-663">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="47f15-663">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="47f15-664">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="47f15-664">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="47f15-665">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="47f15-665">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="47f15-666">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="47f15-666">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="47f15-667">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="47f15-667">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="47f15-668">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="47f15-668">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="47f15-669">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="47f15-669">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="47f15-670">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="47f15-670">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="47f15-671">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="47f15-671">Az.SignalR</span></span>
* <span data-ttu-id="47f15-672">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="47f15-672">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="47f15-673">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="47f15-673">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-674">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-674">Az.Storage</span></span>
* <span data-ttu-id="47f15-675">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="47f15-675">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="47f15-676">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="47f15-676">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="47f15-677">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-677">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="47f15-678">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="47f15-678">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="47f15-679">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="47f15-679">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="47f15-680">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="47f15-680">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="47f15-681">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="47f15-681">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="47f15-682">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-682">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="47f15-683">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-683">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="47f15-684">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="47f15-684">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="47f15-685">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-685">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="47f15-686">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-686">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="47f15-687">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-687">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="47f15-688">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-688">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="47f15-689">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-689">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="47f15-690">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-690">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-691">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-691">Az.Accounts</span></span>
* <span data-ttu-id="47f15-692">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="47f15-692">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="47f15-693">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="47f15-693">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="47f15-694">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="47f15-694">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="47f15-695">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="47f15-695">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="47f15-696">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="47f15-696">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-697">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-697">Az.Aks</span></span>
* <span data-ttu-id="47f15-698">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="47f15-698">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="47f15-699">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="47f15-699">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-700">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-700">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-701">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-701">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="47f15-702">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-702">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="47f15-703">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="47f15-703">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="47f15-704">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="47f15-704">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="47f15-705">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-705">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="47f15-706">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="47f15-706">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="47f15-707">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="47f15-707">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="47f15-708">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-708">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="47f15-709">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-709">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="47f15-710">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="47f15-710">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="47f15-711">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-711">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="47f15-712">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="47f15-712">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-713">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-713">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-714">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="47f15-714">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-715">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-715">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-716">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="47f15-716">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-717">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-717">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-718">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="47f15-718">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="47f15-719">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="47f15-719">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="47f15-720">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-720">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="47f15-721">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="47f15-721">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="47f15-722">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="47f15-722">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="47f15-723">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-723">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="47f15-724">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="47f15-724">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-725">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-725">Az.Network</span></span>
* <span data-ttu-id="47f15-726">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-726">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="47f15-727">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="47f15-727">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="47f15-728">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="47f15-728">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="47f15-729">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="47f15-729">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-730">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-730">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-731">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="47f15-731">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="47f15-732">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="47f15-732">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="47f15-733">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="47f15-733">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-735">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-735">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-736">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-736">Az.Resources</span></span>
* <span data-ttu-id="47f15-737">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="47f15-737">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="47f15-738">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="47f15-738">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-739">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-739">Az.Sql</span></span>
* <span data-ttu-id="47f15-740">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="47f15-740">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="47f15-741">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="47f15-741">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-742">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-742">Az.Storage</span></span>
* <span data-ttu-id="47f15-743">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="47f15-743">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="47f15-744">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="47f15-744">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="47f15-745">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="47f15-745">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="47f15-746">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="47f15-746">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="47f15-747">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="47f15-747">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="47f15-748">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="47f15-748">Supported get single file share usage</span></span>
    - <span data-ttu-id="47f15-749">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-749">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="47f15-750">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-750">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-751">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-751">Az.Accounts</span></span>
* <span data-ttu-id="47f15-752">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-752">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="47f15-753">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="47f15-753">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-754">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-754">Az.Aks</span></span>
* <span data-ttu-id="47f15-755">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="47f15-755">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="47f15-756">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47f15-756">Az.AnalysisServices</span></span>
* <span data-ttu-id="47f15-757">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="47f15-757">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-758">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-758">Az.Automation</span></span>
* <span data-ttu-id="47f15-759">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="47f15-759">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-760">Az.Compute</span></span>
* <span data-ttu-id="47f15-761">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="47f15-761">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-762">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-763">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="47f15-763">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="47f15-764">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47f15-764">Az.EventGrid</span></span>
* <span data-ttu-id="47f15-765">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="47f15-765">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="47f15-766">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-766">Added new features:</span></span>
    - <span data-ttu-id="47f15-767">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="47f15-767">Input mapping</span></span>
    - <span data-ttu-id="47f15-768">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="47f15-768">Event Delivery Schema</span></span>
    - <span data-ttu-id="47f15-769">Link Privado</span><span class="sxs-lookup"><span data-stu-id="47f15-769">Private Link</span></span>
    - <span data-ttu-id="47f15-770">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="47f15-770">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="47f15-771">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="47f15-771">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="47f15-772">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="47f15-772">Azure Function As Destination</span></span>
    - <span data-ttu-id="47f15-773">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="47f15-773">WebHook Batching</span></span>
    - <span data-ttu-id="47f15-774">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="47f15-774">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="47f15-775">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="47f15-775">IpFiltering</span></span>
* <span data-ttu-id="47f15-776">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="47f15-776">Updated cmdlets:</span></span>
    - <span data-ttu-id="47f15-777">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="47f15-777">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="47f15-778">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="47f15-778">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="47f15-779">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="47f15-779">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="47f15-780">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="47f15-780">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="47f15-781">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="47f15-781">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="47f15-782">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="47f15-782">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="47f15-783">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="47f15-783">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="47f15-784">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="47f15-784">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="47f15-785">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="47f15-785">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-786">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-786">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-787">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="47f15-787">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="47f15-788">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="47f15-788">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-789">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-789">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-790">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="47f15-790">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-791">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-791">Az.Monitor</span></span>
* <span data-ttu-id="47f15-792">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="47f15-792">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-793">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-793">Az.Network</span></span>
* <span data-ttu-id="47f15-794">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="47f15-794">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="47f15-795">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-795">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="47f15-796">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="47f15-796">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="47f15-797">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="47f15-797">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="47f15-798">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="47f15-798">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="47f15-799">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="47f15-799">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="47f15-800">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-800">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="47f15-801">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-801">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="47f15-802">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="47f15-802">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="47f15-803">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="47f15-803">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="47f15-804">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="47f15-804">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="47f15-805">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="47f15-805">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="47f15-806">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="47f15-806">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="47f15-807">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-807">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="47f15-808">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="47f15-808">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="47f15-809">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="47f15-809">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="47f15-810">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="47f15-810">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-811">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-812">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="47f15-812">Removed project reference to Authentication</span></span>
* <span data-ttu-id="47f15-813">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="47f15-813">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="47f15-814">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="47f15-814">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-815">Az.Resources</span></span>
* <span data-ttu-id="47f15-816">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="47f15-816">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="47f15-817">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-817">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-818">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-818">Az.Sql</span></span>
* <span data-ttu-id="47f15-819">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="47f15-819">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="47f15-820">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="47f15-820">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="47f15-821">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="47f15-821">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-822">Az.Storage</span></span>
* <span data-ttu-id="47f15-823">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="47f15-823">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="47f15-824">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="47f15-824">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="47f15-825">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-825">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="47f15-826">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-826">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="47f15-827">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-827">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="47f15-828">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="47f15-828">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="47f15-829">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="47f15-829">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="47f15-830">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="47f15-830">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="47f15-831">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="47f15-831">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="47f15-832">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="47f15-832">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="47f15-833">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="47f15-833">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="47f15-834">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="47f15-834">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="47f15-835">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-835">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="47f15-836">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="47f15-836">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="47f15-837">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="47f15-837">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="47f15-838">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-838">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="47f15-839">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="47f15-839">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="47f15-840">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="47f15-840">Az.StorageSync</span></span>
* <span data-ttu-id="47f15-841">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="47f15-841">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="47f15-842">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-842">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="47f15-843">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="47f15-843">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="47f15-844">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="47f15-844">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-845">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-845">Az.Websites</span></span>
* <span data-ttu-id="47f15-846">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="47f15-846">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="47f15-847">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-847">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-848">Az.Accounts</span></span>
* <span data-ttu-id="47f15-849">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="47f15-849">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="47f15-850">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="47f15-850">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="47f15-851">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="47f15-851">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="47f15-852">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="47f15-852">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-853">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-853">Az.Aks</span></span>
* <span data-ttu-id="47f15-854">O uso da [API AccessProfile](/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="47f15-854">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="47f15-855">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-855">Az.Batch</span></span>
* <span data-ttu-id="47f15-856">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="47f15-856">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="47f15-857">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-857">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-858">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-858">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-859">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="47f15-859">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="47f15-860">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="47f15-860">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-861">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-861">Az.Compute</span></span>
* <span data-ttu-id="47f15-862">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="47f15-862">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="47f15-863">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="47f15-863">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="47f15-864">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="47f15-864">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="47f15-865">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="47f15-865">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="47f15-866">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="47f15-866">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-867">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-867">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-868">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="47f15-868">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-869">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-869">Az.EventHub</span></span>
* <span data-ttu-id="47f15-870">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="47f15-870">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="47f15-871">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="47f15-871">Az.Functions</span></span>
* <span data-ttu-id="47f15-872">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="47f15-872">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-873">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-873">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-874">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="47f15-874">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="47f15-875">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="47f15-875">Az.HealthcareApis</span></span>
* <span data-ttu-id="47f15-876">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="47f15-876">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="47f15-877">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="47f15-877">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-878">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-878">Az.Monitor</span></span>
* <span data-ttu-id="47f15-879">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="47f15-879">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="47f15-880">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="47f15-880">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-881">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-881">Az.Network</span></span>
* <span data-ttu-id="47f15-882">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-882">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="47f15-883">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-883">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="47f15-884">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="47f15-884">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="47f15-885">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="47f15-885">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="47f15-886">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="47f15-886">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="47f15-887">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-887">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="47f15-888">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="47f15-888">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="47f15-889">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="47f15-889">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="47f15-890">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="47f15-890">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="47f15-891">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="47f15-891">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="47f15-892">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-892">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="47f15-893">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-893">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="47f15-894">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="47f15-894">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="47f15-895">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-895">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="47f15-896">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="47f15-896">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="47f15-897">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="47f15-897">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="47f15-898">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="47f15-898">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="47f15-899">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-899">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="47f15-900">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="47f15-900">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="47f15-901">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="47f15-901">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="47f15-902">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="47f15-902">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="47f15-903">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="47f15-903">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="47f15-904">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="47f15-904">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="47f15-905">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="47f15-905">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="47f15-906">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="47f15-906">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="47f15-907">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="47f15-907">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="47f15-908">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="47f15-908">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="47f15-909">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="47f15-909">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="47f15-910">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-910">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="47f15-911">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-911">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="47f15-912">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-912">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="47f15-913">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-913">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="47f15-914">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-914">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="47f15-915">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-915">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="47f15-916">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="47f15-916">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="47f15-917">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="47f15-917">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="47f15-918">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="47f15-918">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="47f15-919">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="47f15-919">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="47f15-920">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="47f15-920">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="47f15-921">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="47f15-921">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="47f15-922">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="47f15-922">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="47f15-923">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-923">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="47f15-924">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-924">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="47f15-925">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-925">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="47f15-926">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-926">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="47f15-927">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-927">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="47f15-928">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-928">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="47f15-929">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-929">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="47f15-930">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-930">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-931">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-931">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-932">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="47f15-932">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="47f15-933">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="47f15-933">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="47f15-934">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="47f15-934">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="47f15-935">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="47f15-935">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="47f15-936">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="47f15-936">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-937">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-937">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-938">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-938">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="47f15-939">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="47f15-939">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-940">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-940">Az.Resources</span></span>
* <span data-ttu-id="47f15-941">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="47f15-941">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="47f15-942">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="47f15-942">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="47f15-943">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="47f15-943">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="47f15-944">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-944">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="47f15-945">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="47f15-945">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="47f15-946">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="47f15-946">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-947">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-947">Az.Sql</span></span>
* <span data-ttu-id="47f15-948">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="47f15-948">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="47f15-949">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="47f15-949">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="47f15-950">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="47f15-950">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-951">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-951">Az.Storage</span></span>
* <span data-ttu-id="47f15-952">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="47f15-952">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="47f15-953">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-953">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="47f15-954">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-954">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-955">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-955">Az.Websites</span></span>
* <span data-ttu-id="47f15-956">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="47f15-956">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="47f15-957">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="47f15-957">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="47f15-958">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="47f15-958">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="47f15-959">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="47f15-959">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="47f15-960">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="47f15-960">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="47f15-961">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="47f15-961">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="47f15-962">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-962">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-963">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-963">Az.Accounts</span></span>
* <span data-ttu-id="47f15-964">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="47f15-964">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="47f15-965">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47f15-965">Az.AnalysisServices</span></span>
* <span data-ttu-id="47f15-966">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-966">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-967">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-967">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-968">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-968">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="47f15-969">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="47f15-969">Az.Billing</span></span>
* <span data-ttu-id="47f15-970">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-970">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-971">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-971">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-972">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="47f15-972">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-973">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-974">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-974">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="47f15-975">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="47f15-975">Az.DataShare</span></span>
* <span data-ttu-id="47f15-976">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="47f15-976">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="47f15-977">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="47f15-977">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="47f15-978">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="47f15-978">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-979">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-980">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="47f15-980">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="47f15-981">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="47f15-981">Added optional parameters to</span></span> 
    - <span data-ttu-id="47f15-982">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="47f15-982">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="47f15-983">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="47f15-983">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-984">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-984">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-985">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="47f15-985">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="47f15-986">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47f15-986">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="47f15-987">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-987">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="47f15-988">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="47f15-988">Az.PrivateDns</span></span>
* <span data-ttu-id="47f15-989">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="47f15-989">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-990">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-990">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-991">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="47f15-991">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="47f15-992">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47f15-992">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-993">Az.Resources</span></span>
* <span data-ttu-id="47f15-994">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="47f15-994">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="47f15-995">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="47f15-995">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="47f15-996">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="47f15-996">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="47f15-997">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47f15-997">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="47f15-998">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-998">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-999">Az.Sql</span></span>
* <span data-ttu-id="47f15-1000">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="47f15-1000">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="47f15-1001">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="47f15-1001">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="47f15-1002">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="47f15-1002">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1003">Az.Storage</span></span>
* <span data-ttu-id="47f15-1004">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-1004">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="47f15-1005">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1005">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="47f15-1006">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="47f15-1006">Highlights since the last release</span></span>
* <span data-ttu-id="47f15-1007">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="47f15-1007">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="47f15-1008">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="47f15-1008">General availability of Az.Functions</span></span> 
* <span data-ttu-id="47f15-1009">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="47f15-1009">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-1010">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1010">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1011">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="47f15-1011">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="47f15-1012">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="47f15-1012">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-1013">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-1013">Az.Aks</span></span>
* <span data-ttu-id="47f15-1014">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="47f15-1014">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="47f15-1015">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="47f15-1015">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="47f15-1016">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="47f15-1016">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-1017">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-1017">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-1018">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="47f15-1018">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="47f15-1019">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="47f15-1019">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="47f15-1020">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1020">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="47f15-1021">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="47f15-1021">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="47f15-1022">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1022">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="47f15-1023">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="47f15-1023">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="47f15-1024">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1024">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="47f15-1025">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="47f15-1025">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="47f15-1026">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1026">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="47f15-1027">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="47f15-1027">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="47f15-1028">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="47f15-1028">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="47f15-1029">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="47f15-1029">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="47f15-1030">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="47f15-1030">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="47f15-1031">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="47f15-1031">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="47f15-1032">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="47f15-1032">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="47f15-1033">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="47f15-1033">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="47f15-1034">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-1034">Az.ApplicationInsights</span></span>
* <span data-ttu-id="47f15-1035">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="47f15-1035">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="47f15-1036">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="47f15-1036">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="47f15-1037">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="47f15-1037">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="47f15-1038">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-1038">Az.Batch</span></span>
* <span data-ttu-id="47f15-1039">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="47f15-1039">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="47f15-1040">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1040">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="47f15-1041">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="47f15-1041">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="47f15-1042">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1042">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="47f15-1043">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1043">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="47f15-1044">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="47f15-1044">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="47f15-1045">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1045">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="47f15-1046">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1046">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="47f15-1047">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1047">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1048">Az.Compute</span></span>
* <span data-ttu-id="47f15-1049">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="47f15-1049">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="47f15-1050">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1050">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="47f15-1051">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="47f15-1051">Breaking changes</span></span>
    - <span data-ttu-id="47f15-1052">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1052">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="47f15-1053">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1053">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="47f15-1054">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1054">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="47f15-1055">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="47f15-1055">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="47f15-1056">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="47f15-1056">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="47f15-1057">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="47f15-1057">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="47f15-1058">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="47f15-1058">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1059">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1060">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1060">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-1061">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-1061">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-1062">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="47f15-1062">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="47f15-1063">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="47f15-1063">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="47f15-1064">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="47f15-1064">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="47f15-1065">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="47f15-1065">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="47f15-1066">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="47f15-1066">Az.Functions</span></span>
* <span data-ttu-id="47f15-1067">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="47f15-1067">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-1068">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-1068">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-1069">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="47f15-1069">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="47f15-1070">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="47f15-1070">Az.HealthcareApis</span></span>
* <span data-ttu-id="47f15-1071">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="47f15-1071">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-1072">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1072">Az.IotHub</span></span>
* <span data-ttu-id="47f15-1073">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="47f15-1073">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="47f15-1074">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="47f15-1074">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="47f15-1075">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="47f15-1075">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="47f15-1076">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="47f15-1076">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="47f15-1077">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="47f15-1077">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="47f15-1078">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1078">New cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1079">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1079">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="47f15-1080">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1080">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="47f15-1081">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1081">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="47f15-1082">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1082">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="47f15-1083">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="47f15-1083">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="47f15-1084">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1084">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-1085">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-1085">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-1086">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="47f15-1086">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="47f15-1087">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="47f15-1087">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="47f15-1088">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="47f15-1088">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="47f15-1089">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="47f15-1089">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="47f15-1090">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="47f15-1090">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="47f15-1091">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="47f15-1091">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="47f15-1092">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-1092">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-1093">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1093">Az.Monitor</span></span>
* <span data-ttu-id="47f15-1094">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="47f15-1094">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="47f15-1095">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="47f15-1095">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="47f15-1096">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="47f15-1096">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="47f15-1097">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="47f15-1097">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="47f15-1098">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="47f15-1098">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="47f15-1099">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="47f15-1099">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="47f15-1100">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="47f15-1100">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1101">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1101">Az.Network</span></span>
* <span data-ttu-id="47f15-1102">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="47f15-1102">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="47f15-1103">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="47f15-1103">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="47f15-1104">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="47f15-1104">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="47f15-1105">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-1105">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="47f15-1106">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="47f15-1106">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="47f15-1107">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-1107">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-1108">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="47f15-1108">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="47f15-1109">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="47f15-1109">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="47f15-1110">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="47f15-1110">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="47f15-1111">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="47f15-1111">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="47f15-1112">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-1112">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="47f15-1113">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="47f15-1113">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="47f15-1114">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="47f15-1114">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="47f15-1115">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="47f15-1115">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="47f15-1116">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="47f15-1116">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="47f15-1117">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="47f15-1117">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="47f15-1118">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="47f15-1118">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="47f15-1119">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-1119">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="47f15-1120">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-1120">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="47f15-1121">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-1121">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="47f15-1122">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-1122">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="47f15-1123">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="47f15-1123">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="47f15-1124">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="47f15-1124">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="47f15-1125">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="47f15-1125">Updated cmdlet:</span></span>
        - <span data-ttu-id="47f15-1126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="47f15-1126">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-1127">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-1127">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-1128">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="47f15-1128">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="47f15-1129">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="47f15-1129">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="47f15-1130">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="47f15-1130">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="47f15-1131">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="47f15-1131">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="47f15-1132">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="47f15-1132">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="47f15-1133">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="47f15-1133">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="47f15-1134">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="47f15-1134">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="47f15-1135">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="47f15-1135">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1136">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-1137">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1137">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="47f15-1138">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="47f15-1138">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="47f15-1139">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="47f15-1139">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="47f15-1140">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1140">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="47f15-1141">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="47f15-1141">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1142">Az.Resources</span></span>
* <span data-ttu-id="47f15-1143">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="47f15-1143">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="47f15-1144">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="47f15-1144">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="47f15-1145">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="47f15-1145">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="47f15-1146">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="47f15-1146">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="47f15-1147">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="47f15-1147">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="47f15-1148">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="47f15-1148">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="47f15-1149">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="47f15-1149">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="47f15-1150">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="47f15-1150">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="47f15-1151">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="47f15-1151">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="47f15-1152">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="47f15-1152">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="47f15-1153">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="47f15-1153">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="47f15-1154">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="47f15-1154">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="47f15-1155">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="47f15-1155">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="47f15-1156">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="47f15-1156">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="47f15-1157">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="47f15-1157">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="47f15-1158">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="47f15-1158">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="47f15-1159">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1159">'New-AzDeployment'</span></span>
    - <span data-ttu-id="47f15-1160">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1160">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="47f15-1161">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1161">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="47f15-1162">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1162">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-1163">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-1163">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-1164">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="47f15-1164">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1165">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1165">Az.Sql</span></span>
* <span data-ttu-id="47f15-1166">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="47f15-1166">Enhance performance of:</span></span>
    - <span data-ttu-id="47f15-1167">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="47f15-1167">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="47f15-1168">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="47f15-1168">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="47f15-1169">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="47f15-1169">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="47f15-1170">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="47f15-1170">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="47f15-1171">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="47f15-1171">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="47f15-1172">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="47f15-1172">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="47f15-1173">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="47f15-1173">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="47f15-1174">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="47f15-1174">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="47f15-1175">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-1175">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="47f15-1176">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="47f15-1176">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1177">Az.Storage</span></span>
* <span data-ttu-id="47f15-1178">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1178">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="47f15-1179">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="47f15-1179">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="47f15-1180">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1180">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="47f15-1181">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="47f15-1181">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="47f15-1182">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="47f15-1182">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="47f15-1183">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="47f15-1183">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="47f15-1184">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="47f15-1184">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="47f15-1185">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="47f15-1185">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="47f15-1186">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="47f15-1186">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="47f15-1187">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="47f15-1187">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="47f15-1188">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="47f15-1188">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="47f15-1189">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="47f15-1189">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="47f15-1190">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="47f15-1190">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="47f15-1191">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-1191">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="47f15-1192">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1192">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="47f15-1193">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1193">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="47f15-1194">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-1194">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="47f15-1195">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-1195">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="47f15-1196">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-1196">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="47f15-1197">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="47f15-1197">Supported failover Storage account</span></span>
    - <span data-ttu-id="47f15-1198">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="47f15-1198">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="47f15-1199">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-1199">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="47f15-1200">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-1200">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="47f15-1201">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="47f15-1201">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="47f15-1202">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="47f15-1202">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="47f15-1203">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="47f15-1203">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="47f15-1204">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="47f15-1204">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="47f15-1205">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-1205">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="47f15-1206">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-1206">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="47f15-1207">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="47f15-1207">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="47f15-1208">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="47f15-1208">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="47f15-1209">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="47f15-1209">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="47f15-1210">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="47f15-1210">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="47f15-1211">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="47f15-1211">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="47f15-1212">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="47f15-1212">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="47f15-1213">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="47f15-1213">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="47f15-1214">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="47f15-1214">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="47f15-1215">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="47f15-1215">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="47f15-1216">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="47f15-1216">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="47f15-1217">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47f15-1217">Az.TrafficManager</span></span>
* <span data-ttu-id="47f15-1218">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="47f15-1218">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-1219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-1219">Az.Websites</span></span>
* <span data-ttu-id="47f15-1220">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1220">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="47f15-1221">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1221">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="47f15-1222">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="47f15-1222">Highlights since the last release</span></span>
* <span data-ttu-id="47f15-1223">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="47f15-1223">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-1224">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1224">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1225">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="47f15-1225">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-1226">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-1226">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-1227">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="47f15-1227">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="47f15-1228">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="47f15-1228">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-1229">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-1229">Az.Cdn</span></span>
* <span data-ttu-id="47f15-1230">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="47f15-1230">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-1231">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1231">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-1232">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="47f15-1232">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1233">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1233">Az.Compute</span></span>
* <span data-ttu-id="47f15-1234">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1234">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="47f15-1235">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="47f15-1235">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1236">Az.IotHub</span></span>
* <span data-ttu-id="47f15-1237">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1237">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1238">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="47f15-1238">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="47f15-1239">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="47f15-1239">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="47f15-1240">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="47f15-1240">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="47f15-1241">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1241">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1242">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="47f15-1242">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="47f15-1243">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="47f15-1243">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="47f15-1244">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="47f15-1244">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="47f15-1245">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1245">New cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1246">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-1246">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="47f15-1247">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-1247">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="47f15-1248">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-1248">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="47f15-1249">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-1249">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="47f15-1250">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="47f15-1250">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-1251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-1251">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-1252">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="47f15-1252">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="47f15-1253">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="47f15-1253">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="47f15-1254">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="47f15-1254">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="47f15-1255">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="47f15-1255">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="47f15-1256">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="47f15-1256">Az.Maintenance</span></span>
* <span data-ttu-id="47f15-1257">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="47f15-1257">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1258">Az.Monitor</span></span>
* <span data-ttu-id="47f15-1259">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="47f15-1259">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="47f15-1260">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="47f15-1260">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="47f15-1261">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="47f15-1261">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="47f15-1262">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="47f15-1262">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="47f15-1263">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="47f15-1263">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="47f15-1264">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="47f15-1264">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="47f15-1265">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="47f15-1265">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="47f15-1266">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="47f15-1266">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1267">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1267">Az.Network</span></span>
* <span data-ttu-id="47f15-1268">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="47f15-1268">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="47f15-1269">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-1269">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="47f15-1270">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-1270">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="47f15-1271">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-1271">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="47f15-1272">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-1272">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="47f15-1273">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="47f15-1273">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="47f15-1274">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-1274">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="47f15-1275">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="47f15-1275">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="47f15-1276">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="47f15-1276">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="47f15-1277">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1277">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="47f15-1278">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="47f15-1278">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="47f15-1279">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="47f15-1279">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="47f15-1280">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="47f15-1280">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="47f15-1281">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="47f15-1281">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="47f15-1282">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1282">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="47f15-1283">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1283">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-1284">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-1284">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-1285">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="47f15-1285">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="47f15-1286">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="47f15-1286">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-1287">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-1287">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-1288">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="47f15-1288">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1289">Az.Sql</span></span>
* <span data-ttu-id="47f15-1290">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-1290">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="47f15-1291">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="47f15-1291">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1292">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1292">Az.Storage</span></span>
* <span data-ttu-id="47f15-1293">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="47f15-1293">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="47f15-1294">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-1294">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="47f15-1295">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1295">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="47f15-1296">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1296">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="47f15-1297">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="47f15-1297">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="47f15-1298">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="47f15-1298">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="47f15-1299">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="47f15-1299">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="47f15-1300">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="47f15-1300">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="47f15-1301">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="47f15-1301">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="47f15-1302">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="47f15-1302">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="47f15-1303">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="47f15-1303">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="47f15-1304">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-1304">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="47f15-1305">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="47f15-1305">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="47f15-1306">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1306">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="47f15-1307">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-1307">General</span></span>
* <span data-ttu-id="47f15-1308">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="47f15-1308">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="47f15-1309">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="47f15-1309">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="47f15-1310">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="47f15-1310">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="47f15-1311">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="47f15-1311">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="47f15-1312">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="47f15-1312">Az.Billing</span></span>
  - <span data-ttu-id="47f15-1313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1313">Az.Compute</span></span>
  - <span data-ttu-id="47f15-1314">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="47f15-1314">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="47f15-1315">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1315">Az.EventHub</span></span>
  - <span data-ttu-id="47f15-1316">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1316">Az.IotHub</span></span>
  - <span data-ttu-id="47f15-1317">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-1317">Az.KeyVault</span></span>
  - <span data-ttu-id="47f15-1318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1318">Az.Monitor</span></span>
  - <span data-ttu-id="47f15-1319">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1319">Az.Network</span></span>
  - <span data-ttu-id="47f15-1320">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1320">Az.Resources</span></span>
  - <span data-ttu-id="47f15-1321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1321">Az.Storage</span></span>
  - <span data-ttu-id="47f15-1322">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-1322">Az.Websites</span></span>
* <span data-ttu-id="47f15-1323">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1323">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="47f15-1324">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="47f15-1324">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="47f15-1325">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="47f15-1325">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="47f15-1326">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1326">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1327">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1328">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="47f15-1328">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1329">Az.Compute</span></span>
* <span data-ttu-id="47f15-1330">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="47f15-1330">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="47f15-1331">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="47f15-1331">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="47f15-1332">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1332">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="47f15-1333">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1333">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="47f15-1334">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="47f15-1334">[#11354]</span></span>
* <span data-ttu-id="47f15-1335">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="47f15-1335">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="47f15-1336">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="47f15-1336">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="47f15-1337">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="47f15-1337">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="47f15-1338">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="47f15-1338">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="47f15-1339">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="47f15-1339">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="47f15-1340">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-1340">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="47f15-1341">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="47f15-1341">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="47f15-1342">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1342">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="47f15-1343">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="47f15-1343">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1344">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1344">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1345">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1345">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="47f15-1346">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="47f15-1346">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-1347">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-1348">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="47f15-1348">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="47f15-1349">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="47f15-1349">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-1350">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-1350">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-1351">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="47f15-1351">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-1352">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1352">Az.IotHub</span></span>
* <span data-ttu-id="47f15-1353">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47f15-1353">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="47f15-1354">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1354">New Cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1355">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="47f15-1355">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="47f15-1356">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="47f15-1356">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-1357">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-1357">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-1358">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="47f15-1358">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-1359">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1359">Az.Monitor</span></span>
* <span data-ttu-id="47f15-1360">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="47f15-1360">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1361">Az.Network</span></span>
* <span data-ttu-id="47f15-1362">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="47f15-1362">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="47f15-1363">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-1363">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="47f15-1364">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="47f15-1364">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="47f15-1365">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="47f15-1365">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="47f15-1366">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="47f15-1366">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="47f15-1367">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="47f15-1367">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-1368">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-1368">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-1369">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="47f15-1369">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-1371">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="47f15-1371">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="47f15-1372">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="47f15-1372">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="47f15-1373">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="47f15-1373">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="47f15-1374">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="47f15-1374">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="47f15-1375">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="47f15-1375">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="47f15-1376">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="47f15-1376">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1377">Az.Resources</span></span>
* <span data-ttu-id="47f15-1378">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="47f15-1378">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="47f15-1379">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="47f15-1379">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="47f15-1380">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1380">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="47f15-1381">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1381">Added example.</span></span>
* <span data-ttu-id="47f15-1382">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="47f15-1382">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="47f15-1383">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="47f15-1383">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1384">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1384">Az.Sql</span></span>
* <span data-ttu-id="47f15-1385">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="47f15-1385">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="47f15-1386">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1386">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="47f15-1387">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="47f15-1387">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="47f15-1388">Az.Support</span><span class="sxs-lookup"><span data-stu-id="47f15-1388">Az.Support</span></span>
* <span data-ttu-id="47f15-1389">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="47f15-1389">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-1390">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-1390">Az.Websites</span></span>
* <span data-ttu-id="47f15-1391">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="47f15-1391">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="47f15-1392">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="47f15-1392">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="47f15-1393">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="47f15-1393">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="47f15-1394">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="47f15-1394">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="47f15-1395">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="47f15-1395">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="47f15-1396">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1396">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-1397">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1397">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1398">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="47f15-1398">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="47f15-1399">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="47f15-1399">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="47f15-1400">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="47f15-1400">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-1401">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-1401">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-1402">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="47f15-1402">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="47f15-1403">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="47f15-1403">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="47f15-1404">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="47f15-1404">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="47f15-1405">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="47f15-1405">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-1406">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-1406">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-1407">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="47f15-1407">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-1408">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1408">Az.IotHub</span></span>
* <span data-ttu-id="47f15-1409">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-1409">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="47f15-1410">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1410">New Cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1411">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1411">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="47f15-1412">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1412">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="47f15-1413">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1413">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="47f15-1414">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1414">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="47f15-1415">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-1415">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="47f15-1416">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1416">New Cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1417">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="47f15-1417">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="47f15-1418">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="47f15-1418">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="47f15-1419">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="47f15-1419">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="47f15-1420">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="47f15-1420">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="47f15-1421">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-1421">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="47f15-1422">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-1422">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="47f15-1423">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-1423">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="47f15-1424">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1424">New Cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1425">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="47f15-1425">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="47f15-1426">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="47f15-1426">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="47f15-1427">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47f15-1427">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-1428">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1428">Az.Monitor</span></span>
* <span data-ttu-id="47f15-1429">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="47f15-1429">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1430">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1430">Az.Network</span></span>
* <span data-ttu-id="47f15-1431">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="47f15-1431">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="47f15-1432">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="47f15-1432">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="47f15-1433">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="47f15-1433">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="47f15-1434">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="47f15-1434">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1435">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1435">Az.Resources</span></span>
* <span data-ttu-id="47f15-1436">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="47f15-1436">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="47f15-1437">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="47f15-1437">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="47f15-1438">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="47f15-1438">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="47f15-1439">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="47f15-1439">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="47f15-1440">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="47f15-1440">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="47f15-1441">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="47f15-1441">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="47f15-1442">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="47f15-1442">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="47f15-1443">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="47f15-1443">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="47f15-1444">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="47f15-1444">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="47f15-1445">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="47f15-1445">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="47f15-1446">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="47f15-1446">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="47f15-1447">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1447">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="47f15-1448">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="47f15-1448">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="47f15-1449">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1449">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1450">Az.Sql</span></span>
* <span data-ttu-id="47f15-1451">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="47f15-1451">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="47f15-1452">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="47f15-1452">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="47f15-1453">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="47f15-1453">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="47f15-1454">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="47f15-1454">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="47f15-1455">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="47f15-1455">Remove an LTR backup</span></span>
    - <span data-ttu-id="47f15-1456">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="47f15-1456">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="47f15-1457">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="47f15-1457">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="47f15-1458">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-1458">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="47f15-1459">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1459">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1460">Az.Storage</span></span>
* <span data-ttu-id="47f15-1461">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-1461">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="47f15-1462">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-1462">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="47f15-1463">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="47f15-1463">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="47f15-1464">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="47f15-1464">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="47f15-1465">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="47f15-1465">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-1466">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-1466">Az.Websites</span></span>
* <span data-ttu-id="47f15-1467">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="47f15-1467">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="47f15-1468">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="47f15-1468">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="47f15-1469">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="47f15-1469">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="47f15-1470">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="47f15-1470">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="47f15-1471">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="47f15-1471">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="47f15-1472">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1472">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="47f15-1473">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="47f15-1473">Highlights since the last major release</span></span>
* <span data-ttu-id="47f15-1474">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="47f15-1474">Updated client side telemetry.</span></span>
* <span data-ttu-id="47f15-1475">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="47f15-1475">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="47f15-1476">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="47f15-1476">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-1477">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1477">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1478">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="47f15-1478">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-1479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-1479">Az.Automation</span></span>
* <span data-ttu-id="47f15-1480">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="47f15-1480">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-1481">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1481">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-1482">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1482">Updated SDK to 7.0</span></span>
* <span data-ttu-id="47f15-1483">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="47f15-1483">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1484">Az.Compute</span></span>
* <span data-ttu-id="47f15-1485">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="47f15-1485">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-1486">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-1486">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-1487">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="47f15-1487">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-1488">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1488">Az.IotHub</span></span>
* <span data-ttu-id="47f15-1489">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-1489">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="47f15-1490">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-1490">New Cmdlets are:</span></span>
    - <span data-ttu-id="47f15-1491">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1491">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="47f15-1492">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1492">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="47f15-1493">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1493">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="47f15-1494">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="47f15-1494">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-1495">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-1495">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-1496">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="47f15-1496">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1497">Az.Monitor</span></span>
* <span data-ttu-id="47f15-1498">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="47f15-1498">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="47f15-1499">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1499">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="47f15-1500">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="47f15-1500">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1501">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1501">Az.Network</span></span>
* <span data-ttu-id="47f15-1502">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1502">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="47f15-1503">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="47f15-1503">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="47f15-1504">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="47f15-1504">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="47f15-1505">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="47f15-1505">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="47f15-1506">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1506">No new cmdlets are added.</span></span> <span data-ttu-id="47f15-1507">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="47f15-1507">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-1508">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1508">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-1509">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="47f15-1509">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1510">Az.Resources</span></span>
* <span data-ttu-id="47f15-1511">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="47f15-1511">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="47f15-1512">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="47f15-1512">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="47f15-1513">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="47f15-1513">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="47f15-1514">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="47f15-1514">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="47f15-1515">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="47f15-1515">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="47f15-1516">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="47f15-1516">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="47f15-1517">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="47f15-1517">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="47f15-1518">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-1518">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1519">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1519">Az.Sql</span></span>
* <span data-ttu-id="47f15-1520">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="47f15-1520">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="47f15-1521">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="47f15-1521">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="47f15-1522">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="47f15-1522">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="47f15-1523">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47f15-1523">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="47f15-1524">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="47f15-1524">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="47f15-1525">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="47f15-1525">Az.StorageSync</span></span>
* <span data-ttu-id="47f15-1526">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1526">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="47f15-1527">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1527">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="47f15-1528">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="47f15-1528">Highlights since the last major release</span></span>
* <span data-ttu-id="47f15-1529">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="47f15-1529">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="47f15-1530">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1530">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1531">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1532">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="47f15-1532">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="47f15-1533">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="47f15-1533">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-1534">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-1534">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-1535">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="47f15-1535">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="47f15-1536">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="47f15-1536">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="47f15-1537">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="47f15-1537">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="47f15-1538">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="47f15-1538">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1539">Az.Compute</span></span>
* <span data-ttu-id="47f15-1540">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="47f15-1540">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="47f15-1541">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="47f15-1541">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="47f15-1542">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="47f15-1542">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="47f15-1543">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-1543">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="47f15-1544">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="47f15-1544">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1545">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1546">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1546">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="47f15-1547">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="47f15-1547">Az.DeploymentManager</span></span>
* <span data-ttu-id="47f15-1548">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="47f15-1548">Adds LIST operations for resources</span></span>
* <span data-ttu-id="47f15-1549">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="47f15-1549">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-1550">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-1550">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-1551">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="47f15-1551">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-1552">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-1552">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-1553">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="47f15-1553">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1554">Az.Network</span></span>
* <span data-ttu-id="47f15-1555">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="47f15-1555">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="47f15-1556">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="47f15-1556">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="47f15-1557">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="47f15-1557">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="47f15-1558">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="47f15-1558">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="47f15-1559">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="47f15-1559">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="47f15-1560">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="47f15-1560">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="47f15-1561">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="47f15-1561">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="47f15-1562">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="47f15-1562">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="47f15-1563">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-1563">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-1564">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-1564">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="47f15-1565">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-1565">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="47f15-1566">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="47f15-1566">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="47f15-1567">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="47f15-1567">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-1568">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-1568">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-1569">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="47f15-1569">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="47f15-1570">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="47f15-1570">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="47f15-1571">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="47f15-1571">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="47f15-1572">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="47f15-1572">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-1574">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1574">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="47f15-1575">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="47f15-1575">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1576">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1576">Az.Resources</span></span>
* <span data-ttu-id="47f15-1577">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="47f15-1577">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="47f15-1578">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="47f15-1578">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1579">Az.Sql</span></span>
<span data-ttu-id="47f15-1580">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="47f15-1580">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1581">Az.Storage</span></span>
* <span data-ttu-id="47f15-1582">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-1582">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="47f15-1583">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-1583">New-AzStorageAccount</span></span>
* <span data-ttu-id="47f15-1584">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="47f15-1584">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="47f15-1585">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="47f15-1585">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-1586">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-1586">Az.Websites</span></span>
* <span data-ttu-id="47f15-1587">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="47f15-1587">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="47f15-1588">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="47f15-1588">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="47f15-1589">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="47f15-1589">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-1590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1590">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1591">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="47f15-1591">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-1592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-1592">Az.Cdn</span></span>
* <span data-ttu-id="47f15-1593">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="47f15-1593">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1594">Az.Compute</span></span>
* <span data-ttu-id="47f15-1595">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="47f15-1595">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="47f15-1596">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-1596">Az.ContainerInstance</span></span>
* <span data-ttu-id="47f15-1597">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-1597">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="47f15-1598">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="47f15-1598">Az.DataBoxEdge</span></span>
* <span data-ttu-id="47f15-1599">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="47f15-1599">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="47f15-1600">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="47f15-1600">Get the Edge Storage Container</span></span>
* <span data-ttu-id="47f15-1601">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="47f15-1601">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="47f15-1602">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="47f15-1602">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="47f15-1603">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="47f15-1603">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="47f15-1604">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="47f15-1604">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="47f15-1605">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="47f15-1605">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="47f15-1606">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="47f15-1606">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="47f15-1607">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1607">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="47f15-1608">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="47f15-1608">Get the Edge Storage Account</span></span>
* <span data-ttu-id="47f15-1609">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1609">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="47f15-1610">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="47f15-1610">Create new Edge Storage Account</span></span>
* <span data-ttu-id="47f15-1611">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="47f15-1611">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="47f15-1612">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="47f15-1612">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="47f15-1613">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="47f15-1613">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="47f15-1614">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="47f15-1614">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="47f15-1615">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="47f15-1615">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="47f15-1616">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="47f15-1616">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1617">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1618">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="47f15-1618">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="47f15-1619">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1619">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="47f15-1620">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="47f15-1620">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="47f15-1621">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="47f15-1621">Az.DevTestLabs</span></span>
* <span data-ttu-id="47f15-1622">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="47f15-1622">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1623">Az.EventHub</span></span>
* <span data-ttu-id="47f15-1624">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="47f15-1624">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-1625">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-1626">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="47f15-1626">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="47f15-1627">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="47f15-1627">Az.MachineLearning</span></span>
* <span data-ttu-id="47f15-1628">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="47f15-1628">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="47f15-1629">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="47f15-1629">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="47f15-1630">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="47f15-1630">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="47f15-1631">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="47f15-1631">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="47f15-1632">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="47f15-1632">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="47f15-1633">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="47f15-1633">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="47f15-1634">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="47f15-1634">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="47f15-1635">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="47f15-1635">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1636">Az.Network</span></span>
* <span data-ttu-id="47f15-1637">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="47f15-1637">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-1638">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1638">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-1639">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1639">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="47f15-1640">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1640">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="47f15-1641">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1641">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="47f15-1642">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1642">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1643">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1643">Az.Resources</span></span>
* <span data-ttu-id="47f15-1644">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1644">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1645">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1645">Az.Sql</span></span>
* <span data-ttu-id="47f15-1646">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="47f15-1646">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="47f15-1647">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="47f15-1647">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="47f15-1648">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="47f15-1648">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="47f15-1649">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="47f15-1649">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1650">Az.Storage</span></span>
* <span data-ttu-id="47f15-1651">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="47f15-1651">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="47f15-1652">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-1652">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="47f15-1653">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="47f15-1653">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="47f15-1654">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-1654">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="47f15-1655">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-1655">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="47f15-1656">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-1656">General</span></span>
* <span data-ttu-id="47f15-1657">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="47f15-1657">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-1658">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1658">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1659">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="47f15-1659">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="47f15-1660">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="47f15-1660">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="47f15-1661">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-1661">Az.Batch</span></span>
* <span data-ttu-id="47f15-1662">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="47f15-1662">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1663">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1664">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1664">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-1665">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-1665">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-1666">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="47f15-1666">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="47f15-1667">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="47f15-1667">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="47f15-1668">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="47f15-1668">Az.HealthcareApis</span></span>
* <span data-ttu-id="47f15-1669">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="47f15-1669">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-1670">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-1670">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-1671">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="47f15-1671">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="47f15-1672">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="47f15-1672">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="47f15-1673">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="47f15-1673">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-1674">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1674">Az.Monitor</span></span>
* <span data-ttu-id="47f15-1675">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="47f15-1675">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="47f15-1676">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="47f15-1676">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="47f15-1677">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="47f15-1677">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1678">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1678">Az.Network</span></span>
* <span data-ttu-id="47f15-1679">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="47f15-1679">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1680">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1680">Az.Resources</span></span>
* <span data-ttu-id="47f15-1681">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="47f15-1681">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="47f15-1682">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="47f15-1682">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1683">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1683">Az.Sql</span></span>
* <span data-ttu-id="47f15-1684">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="47f15-1684">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1685">Az.Storage</span></span>
* <span data-ttu-id="47f15-1686">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="47f15-1686">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="47f15-1687">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="47f15-1687">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="47f15-1688">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="47f15-1688">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="47f15-1689">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="47f15-1689">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="47f15-1690">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="47f15-1690">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="47f15-1691">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="47f15-1691">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="47f15-1692">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1692">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="47f15-1693">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-1693">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="47f15-1694">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-1694">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="47f15-1695">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="47f15-1695">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="47f15-1696">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="47f15-1696">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="47f15-1697">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="47f15-1697">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="47f15-1698">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="47f15-1698">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="47f15-1699">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-1699">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="47f15-1700">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="47f15-1700">Highlights since the last major release</span></span>
* <span data-ttu-id="47f15-1701">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="47f15-1701">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="47f15-1702">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="47f15-1702">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1703">Az.Compute</span></span>
* <span data-ttu-id="47f15-1704">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="47f15-1704">VM Reapply feature</span></span>
    - <span data-ttu-id="47f15-1705">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="47f15-1705">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="47f15-1706">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="47f15-1706">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="47f15-1707">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-1707">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="47f15-1708">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="47f15-1708">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="47f15-1709">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-1709">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="47f15-1710">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="47f15-1710">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="47f15-1711">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="47f15-1711">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="47f15-1712">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="47f15-1712">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="47f15-1713">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="47f15-1713">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="47f15-1714">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-1714">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="47f15-1715">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="47f15-1715">Az.DataBoxEdge</span></span>
* <span data-ttu-id="47f15-1716">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1716">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="47f15-1717">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="47f15-1717">Get the Order</span></span>
* <span data-ttu-id="47f15-1718">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1718">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="47f15-1719">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="47f15-1719">Create new Order</span></span>
* <span data-ttu-id="47f15-1720">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1720">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="47f15-1721">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="47f15-1721">Remove the Order</span></span>
* <span data-ttu-id="47f15-1722">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="47f15-1722">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="47f15-1723">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="47f15-1723">Now creates Local Share</span></span>
* <span data-ttu-id="47f15-1724">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1724">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="47f15-1725">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="47f15-1725">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="47f15-1726">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1726">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="47f15-1727">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="47f15-1727">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="47f15-1728">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1728">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="47f15-1729">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="47f15-1729">Gets the information about Triggers</span></span>
* <span data-ttu-id="47f15-1730">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1730">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="47f15-1731">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="47f15-1731">Create new Triggers</span></span>
* <span data-ttu-id="47f15-1732">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1732">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="47f15-1733">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="47f15-1733">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1734">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1734">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1735">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1735">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="47f15-1736">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1736">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-1737">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-1737">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-1738">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="47f15-1738">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-1739">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1739">Az.EventHub</span></span>
* <span data-ttu-id="47f15-1740">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="47f15-1740">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-1741">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-1741">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-1742">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="47f15-1742">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="47f15-1743">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="47f15-1743">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="47f15-1744">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="47f15-1744">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="47f15-1745">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="47f15-1745">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1746">Az.Network</span></span>
* <span data-ttu-id="47f15-1747">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1747">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="47f15-1748">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="47f15-1748">Az.PrivateDns</span></span>
* <span data-ttu-id="47f15-1749">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1749">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-1750">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1750">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-1751">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="47f15-1751">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="47f15-1752">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="47f15-1752">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="47f15-1753">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="47f15-1753">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="47f15-1754">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47f15-1754">Az.RedisCache</span></span>
* <span data-ttu-id="47f15-1755">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1755">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="47f15-1756">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1756">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="47f15-1757">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="47f15-1757">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1758">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1758">Az.Resources</span></span>
- <span data-ttu-id="47f15-1759">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="47f15-1759">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="47f15-1760">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="47f15-1760">Updated create policy definition help example</span></span>
- <span data-ttu-id="47f15-1761">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1761">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="47f15-1762">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="47f15-1762">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="47f15-1763">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1763">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1764">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1764">Az.Sql</span></span>
* <span data-ttu-id="47f15-1765">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-1765">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="47f15-1766">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="47f15-1766">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="47f15-1767">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-1767">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="47f15-1768">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-1768">General</span></span>
* <span data-ttu-id="47f15-1769">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="47f15-1769">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-1770">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1770">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1771">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1771">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="47f15-1772">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="47f15-1772">Az.Advisor</span></span>
* <span data-ttu-id="47f15-1773">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47f15-1773">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="47f15-1774">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-1774">Az.Batch</span></span>
* <span data-ttu-id="47f15-1775">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1775">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="47f15-1776">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1776">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="47f15-1777">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="47f15-1777">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="47f15-1778">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="47f15-1778">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="47f15-1779">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="47f15-1779">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="47f15-1780">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1780">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="47f15-1781">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="47f15-1781">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="47f15-1782">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="47f15-1782">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="47f15-1783">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="47f15-1783">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="47f15-1784">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="47f15-1784">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="47f15-1785">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="47f15-1785">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="47f15-1786">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1786">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="47f15-1787">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="47f15-1787">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="47f15-1788">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1788">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="47f15-1789">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1789">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="47f15-1790">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1790">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="47f15-1791">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1791">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="47f15-1792">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1792">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="47f15-1793">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="47f15-1793">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="47f15-1794">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="47f15-1794">This operation is no longer supported.</span></span>
* <span data-ttu-id="47f15-1795">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1795">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="47f15-1796">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1796">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="47f15-1797">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1797">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="47f15-1798">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="47f15-1798">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="47f15-1799">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="47f15-1799">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="47f15-1800">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="47f15-1800">New non-verified images are also now returned.</span></span> <span data-ttu-id="47f15-1801">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="47f15-1801">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="47f15-1802">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="47f15-1802">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="47f15-1803">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="47f15-1803">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="47f15-1804">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1804">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="47f15-1805">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="47f15-1805">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="47f15-1806">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1806">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="47f15-1807">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="47f15-1807">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="47f15-1808">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="47f15-1808">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="47f15-1809">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="47f15-1809">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="47f15-1810">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="47f15-1810">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-1811">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-1811">Az.Cdn</span></span>
* <span data-ttu-id="47f15-1812">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="47f15-1812">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="47f15-1813">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="47f15-1813">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1814">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1814">Az.Compute</span></span>
* <span data-ttu-id="47f15-1815">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="47f15-1815">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="47f15-1816">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="47f15-1816">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="47f15-1817">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="47f15-1817">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="47f15-1818">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-1818">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="47f15-1819">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-1819">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="47f15-1820">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="47f15-1820">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="47f15-1821">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-1821">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="47f15-1822">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="47f15-1822">Breaking changes</span></span>
    - <span data-ttu-id="47f15-1823">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="47f15-1823">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="47f15-1824">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="47f15-1824">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1825">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1825">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1826">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1826">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-1828">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="47f15-1828">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="47f15-1829">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="47f15-1829">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="47f15-1830">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="47f15-1830">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="47f15-1831">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="47f15-1831">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="47f15-1832">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="47f15-1832">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="47f15-1833">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="47f15-1833">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-1834">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-1834">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-1835">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="47f15-1835">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-1836">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-1836">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-1837">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="47f15-1837">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="47f15-1838">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="47f15-1838">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="47f15-1839">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1839">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="47f15-1840">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="47f15-1840">Removed five cmdlets:</span></span>
    - <span data-ttu-id="47f15-1841">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="47f15-1841">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="47f15-1842">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="47f15-1842">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="47f15-1843">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="47f15-1843">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="47f15-1844">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="47f15-1844">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="47f15-1845">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="47f15-1845">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="47f15-1846">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-1846">Added three cmdlets:</span></span>
    - <span data-ttu-id="47f15-1847">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="47f15-1847">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="47f15-1848">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="47f15-1848">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="47f15-1849">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="47f15-1849">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="47f15-1850">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="47f15-1850">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="47f15-1851">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="47f15-1851">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="47f15-1852">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="47f15-1852">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="47f15-1853">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="47f15-1853">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="47f15-1854">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="47f15-1854">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="47f15-1855">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="47f15-1855">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="47f15-1856">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="47f15-1856">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="47f15-1857">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="47f15-1857">Added some scenario test cases.</span></span>
* <span data-ttu-id="47f15-1858">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1858">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-1859">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1859">Az.IotHub</span></span>
* <span data-ttu-id="47f15-1860">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="47f15-1860">Breaking changes:</span></span>
    - <span data-ttu-id="47f15-1861">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="47f15-1861">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="47f15-1862">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="47f15-1862">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="47f15-1863">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="47f15-1863">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="47f15-1864">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="47f15-1864">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="47f15-1865">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="47f15-1865">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="47f15-1866">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="47f15-1866">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="47f15-1867">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1867">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="47f15-1868">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="47f15-1868">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="47f15-1869">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="47f15-1869">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="47f15-1870">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="47f15-1870">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="47f15-1871">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="47f15-1871">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="47f15-1872">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="47f15-1872">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-1873">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-1873">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-1874">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1874">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="47f15-1875">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1875">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="47f15-1876">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1876">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="47f15-1877">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1877">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="47f15-1878">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1878">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="47f15-1879">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1879">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="47f15-1880">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1880">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="47f15-1881">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-1881">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="47f15-1882">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="47f15-1882">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-1883">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-1883">Az.Resources</span></span>
* <span data-ttu-id="47f15-1884">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="47f15-1884">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-1885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-1885">Az.Network</span></span>
* <span data-ttu-id="47f15-1886">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="47f15-1886">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="47f15-1887">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="47f15-1887">Updated cmdlet:</span></span>
        - <span data-ttu-id="47f15-1888">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1888">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-1889">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1889">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-1890">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1890">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-1891">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1891">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-1892">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1892">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="47f15-1893">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="47f15-1893">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="47f15-1894">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="47f15-1894">New cmdlet:</span></span>
        - <span data-ttu-id="47f15-1895">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="47f15-1895">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="47f15-1896">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="47f15-1896">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="47f15-1897">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="47f15-1897">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="47f15-1898">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1898">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="47f15-1899">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="47f15-1899">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="47f15-1900">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="47f15-1900">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="47f15-1901">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-1901">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="47f15-1902">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1902">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="47f15-1903">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-1903">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-1904">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="47f15-1904">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="47f15-1905">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="47f15-1905">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="47f15-1906">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="47f15-1906">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="47f15-1907">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="47f15-1907">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="47f15-1908">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1908">Set-AzVirtualHub</span></span>
* <span data-ttu-id="47f15-1909">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="47f15-1909">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="47f15-1910">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="47f15-1910">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="47f15-1911">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1911">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="47f15-1912">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1912">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="47f15-1913">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1913">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="47f15-1914">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1914">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="47f15-1915">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1915">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="47f15-1916">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-1916">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-1917">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-1917">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="47f15-1918">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="47f15-1918">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="47f15-1919">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1919">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="47f15-1920">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1920">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="47f15-1921">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1921">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="47f15-1922">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1922">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="47f15-1923">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-1923">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="47f15-1924">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="47f15-1924">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="47f15-1925">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-1925">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-1926">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="47f15-1926">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="47f15-1927">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="47f15-1927">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="47f15-1928">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="47f15-1928">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="47f15-1929">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="47f15-1929">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="47f15-1930">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="47f15-1930">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="47f15-1931">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-1931">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="47f15-1932">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="47f15-1932">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="47f15-1933">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-1933">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="47f15-1934">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="47f15-1934">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="47f15-1935">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="47f15-1935">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="47f15-1936">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="47f15-1936">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="47f15-1937">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="47f15-1937">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="47f15-1938">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-1938">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="47f15-1939">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-1939">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="47f15-1940">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="47f15-1940">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="47f15-1941">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-1941">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="47f15-1942">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-1942">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="47f15-1943">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-1943">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-1944">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-1944">New-AzIpGroup</span></span>
        - <span data-ttu-id="47f15-1945">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-1945">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="47f15-1946">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-1946">Get-AzIpGroup</span></span>
        - <span data-ttu-id="47f15-1947">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-1947">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-1948">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-1948">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-1949">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="47f15-1949">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-1950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-1950">Az.Sql</span></span>
* <span data-ttu-id="47f15-1951">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="47f15-1951">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="47f15-1952">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="47f15-1952">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="47f15-1953">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="47f15-1953">Removed deprecated aliases:</span></span>
* <span data-ttu-id="47f15-1954">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="47f15-1954">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="47f15-1955">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="47f15-1955">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="47f15-1956">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-1956">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="47f15-1957">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="47f15-1957">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="47f15-1958">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="47f15-1958">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="47f15-1959">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="47f15-1959">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-1960">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-1960">Az.Storage</span></span>
* <span data-ttu-id="47f15-1961">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-1961">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="47f15-1962">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-1962">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="47f15-1963">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-1963">Set-AzStorageAccount</span></span>
* <span data-ttu-id="47f15-1964">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="47f15-1964">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="47f15-1965">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="47f15-1965">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="47f15-1966">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="47f15-1966">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="47f15-1967">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-1967">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="47f15-1968">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-1968">General</span></span>
* <span data-ttu-id="47f15-1969">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1969">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-1970">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-1970">Az.Accounts</span></span>
* <span data-ttu-id="47f15-1971">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="47f15-1971">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-1972">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-1972">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-1973">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="47f15-1973">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="47f15-1974">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="47f15-1974">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-1975">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-1975">Az.Automation</span></span>
* <span data-ttu-id="47f15-1976">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="47f15-1976">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="47f15-1977">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-1977">Az.Batch</span></span>
* <span data-ttu-id="47f15-1978">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="47f15-1978">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-1979">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-1979">Az.Compute</span></span>
* <span data-ttu-id="47f15-1980">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-1980">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="47f15-1981">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="47f15-1981">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="47f15-1982">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="47f15-1982">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="47f15-1983">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="47f15-1983">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-1984">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-1984">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-1985">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="47f15-1985">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="47f15-1986">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="47f15-1986">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="47f15-1987">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1987">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-1988">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-1988">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-1989">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="47f15-1989">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="47f15-1990">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="47f15-1990">Az.HealthcareApis</span></span>
* <span data-ttu-id="47f15-1991">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="47f15-1991">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="47f15-1992">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="47f15-1992">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="47f15-1993">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="47f15-1993">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="47f15-1994">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="47f15-1994">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-1995">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-1995">Az.IotHub</span></span>
* <span data-ttu-id="47f15-1996">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="47f15-1996">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="47f15-1997">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="47f15-1997">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-1998">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-1998">Az.Monitor</span></span>
* <span data-ttu-id="47f15-1999">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="47f15-1999">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="47f15-2000">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="47f15-2000">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="47f15-2001">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="47f15-2001">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="47f15-2002">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47f15-2002">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2003">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2003">Az.Network</span></span>
* <span data-ttu-id="47f15-2004">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="47f15-2004">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="47f15-2005">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-2005">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="47f15-2006">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-2006">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-2007">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2007">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="47f15-2008">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2008">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="47f15-2009">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="47f15-2009">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="47f15-2010">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="47f15-2010">Updated cmdlets:</span></span>
        - <span data-ttu-id="47f15-2011">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2011">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="47f15-2012">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2012">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="47f15-2013">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2013">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="47f15-2014">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="47f15-2014">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="47f15-2015">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="47f15-2015">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="47f15-2016">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="47f15-2016">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="47f15-2017">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="47f15-2017">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="47f15-2018">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47f15-2018">Az.RedisCache</span></span>
* <span data-ttu-id="47f15-2019">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="47f15-2019">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2020">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2020">Az.Sql</span></span>
* <span data-ttu-id="47f15-2021">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="47f15-2021">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2022">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2022">Az.Storage</span></span>
* <span data-ttu-id="47f15-2023">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="47f15-2023">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="47f15-2024">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="47f15-2024">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="47f15-2025">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47f15-2025">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="47f15-2026">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="47f15-2026">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="47f15-2027">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2027">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="47f15-2028">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="47f15-2028">Az.StorageSync</span></span>
* <span data-ttu-id="47f15-2029">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="47f15-2029">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2030">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2030">Az.Websites</span></span>
* <span data-ttu-id="47f15-2031">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="47f15-2031">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="47f15-2032">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2032">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="47f15-2033">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-2033">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-2034">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-2034">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="47f15-2035">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="47f15-2035">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="47f15-2036">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2036">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2037">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2037">Az.Automation</span></span>
* <span data-ttu-id="47f15-2038">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="47f15-2038">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="47f15-2039">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="47f15-2039">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="47f15-2040">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="47f15-2040">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2041">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2041">Az.Compute</span></span>
* <span data-ttu-id="47f15-2042">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2042">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="47f15-2043">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2043">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="47f15-2044">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="47f15-2044">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="47f15-2045">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="47f15-2045">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="47f15-2046">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="47f15-2046">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="47f15-2047">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="47f15-2047">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="47f15-2048">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="47f15-2048">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="47f15-2049">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="47f15-2049">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="47f15-2050">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="47f15-2050">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-2051">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-2051">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-2052">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="47f15-2052">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="47f15-2053">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="47f15-2053">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-2054">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-2054">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-2055">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="47f15-2055">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-2056">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2056">Az.IotHub</span></span>
* <span data-ttu-id="47f15-2057">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="47f15-2057">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="47f15-2058">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="47f15-2058">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="47f15-2059">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="47f15-2059">New cmdlets are:</span></span>
    - <span data-ttu-id="47f15-2060">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="47f15-2060">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="47f15-2061">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="47f15-2061">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="47f15-2062">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="47f15-2062">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="47f15-2063">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="47f15-2063">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-2064">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-2064">Az.Monitor</span></span>
* <span data-ttu-id="47f15-2065">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="47f15-2065">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="47f15-2066">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="47f15-2066">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="47f15-2067">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="47f15-2067">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="47f15-2068">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="47f15-2068">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="47f15-2069">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="47f15-2069">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="47f15-2070">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="47f15-2070">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="47f15-2071">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="47f15-2071">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="47f15-2072">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="47f15-2072">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="47f15-2073">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="47f15-2073">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="47f15-2074">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="47f15-2074">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="47f15-2075">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="47f15-2075">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="47f15-2076">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="47f15-2076">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="47f15-2077">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="47f15-2077">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="47f15-2078">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="47f15-2078">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="47f15-2079">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="47f15-2079">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="47f15-2080">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="47f15-2080">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="47f15-2081">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="47f15-2081">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="47f15-2082">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-2082">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="47f15-2083">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="47f15-2083">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="47f15-2084">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-2084">Overall improved help files</span></span>
* <span data-ttu-id="47f15-2085">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="47f15-2085">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2086">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2086">Az.Network</span></span>
* <span data-ttu-id="47f15-2087">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="47f15-2087">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="47f15-2088">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="47f15-2088">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="47f15-2089">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="47f15-2089">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="47f15-2090">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="47f15-2090">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="47f15-2091">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="47f15-2091">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="47f15-2092">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="47f15-2092">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="47f15-2093">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="47f15-2093">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="47f15-2094">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="47f15-2094">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="47f15-2095">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2095">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="47f15-2096">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="47f15-2096">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="47f15-2097">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2097">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="47f15-2098">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-2098">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="47f15-2099">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="47f15-2099">New cmdlets</span></span>
        - <span data-ttu-id="47f15-2100">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="47f15-2100">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="47f15-2101">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2101">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="47f15-2102">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="47f15-2102">Updated cmdlet:</span></span>
        - <span data-ttu-id="47f15-2103">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="47f15-2103">New-VpnSite</span></span>
        - <span data-ttu-id="47f15-2104">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="47f15-2104">Update-VpnSite</span></span>
        - <span data-ttu-id="47f15-2105">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2105">New-VpnConnection</span></span>
        - <span data-ttu-id="47f15-2106">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2106">Update-VpnConnection</span></span>
* <span data-ttu-id="47f15-2107">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="47f15-2107">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2108">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2109">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="47f15-2109">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="47f15-2110">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="47f15-2110">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2111">Az.Resources</span></span>
* <span data-ttu-id="47f15-2112">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="47f15-2112">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-2113">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-2113">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-2114">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="47f15-2114">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="47f15-2115">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="47f15-2115">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="47f15-2116">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="47f15-2116">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="47f15-2117">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="47f15-2117">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="47f15-2118">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="47f15-2118">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="47f15-2119">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="47f15-2119">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="47f15-2120">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="47f15-2120">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="47f15-2121">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="47f15-2121">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="47f15-2122">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="47f15-2122">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="47f15-2123">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="47f15-2123">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="47f15-2124">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="47f15-2124">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="47f15-2125">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="47f15-2125">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="47f15-2126">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="47f15-2126">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="47f15-2127">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="47f15-2127">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="47f15-2128">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="47f15-2128">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="47f15-2129">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="47f15-2129">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="47f15-2130">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="47f15-2130">Az.SignalR</span></span>
* <span data-ttu-id="47f15-2131">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="47f15-2131">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2132">Az.Sql</span></span>
* <span data-ttu-id="47f15-2133">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="47f15-2133">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="47f15-2134">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="47f15-2134">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="47f15-2135">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2135">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="47f15-2136">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="47f15-2136">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="47f15-2137">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="47f15-2137">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2138">Az.Storage</span></span>
* <span data-ttu-id="47f15-2139">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-2139">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="47f15-2140">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="47f15-2140">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="47f15-2141">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2141">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="47f15-2142">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2142">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="47f15-2143">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="47f15-2143">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="47f15-2144">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2144">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="47f15-2145">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="47f15-2145">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="47f15-2146">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-2146">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="47f15-2147">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-2147">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="47f15-2148">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-2148">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="47f15-2149">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="47f15-2149">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2150">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2150">Az.Websites</span></span>
* <span data-ttu-id="47f15-2151">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="47f15-2151">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="47f15-2152">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="47f15-2152">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="47f15-2153">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="47f15-2153">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="47f15-2154">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2154">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="47f15-2155">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-2155">General</span></span>
* <span data-ttu-id="47f15-2156">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="47f15-2156">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-2157">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2157">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2158">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="47f15-2158">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-2159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-2159">Az.Aks</span></span>
* <span data-ttu-id="47f15-2160">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="47f15-2160">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="47f15-2161">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="47f15-2161">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-2162">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-2162">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-2163">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="47f15-2163">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="47f15-2164">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="47f15-2164">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="47f15-2165">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="47f15-2165">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="47f15-2166">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="47f15-2166">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="47f15-2167">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="47f15-2167">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="47f15-2168">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-2168">Az.Batch</span></span>
* <span data-ttu-id="47f15-2169">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="47f15-2169">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-2170">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-2170">Az.Cdn</span></span>
* <span data-ttu-id="47f15-2171">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="47f15-2171">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2172">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2172">Az.Compute</span></span>
* <span data-ttu-id="47f15-2173">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2173">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="47f15-2174">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-2174">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="47f15-2175">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="47f15-2175">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="47f15-2176">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-2176">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="47f15-2177">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="47f15-2177">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="47f15-2178">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="47f15-2178">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="47f15-2179">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="47f15-2179">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="47f15-2180">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="47f15-2180">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-2181">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-2181">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-2182">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="47f15-2182">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="47f15-2183">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="47f15-2183">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="47f15-2184">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="47f15-2184">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="47f15-2185">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="47f15-2185">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-2186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-2186">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-2187">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="47f15-2187">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-2188">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2188">Az.EventHub</span></span>
* <span data-ttu-id="47f15-2189">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-2189">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="47f15-2190">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="47f15-2190">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="47f15-2191">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="47f15-2191">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="47f15-2192">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="47f15-2192">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="47f15-2193">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="47f15-2193">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="47f15-2194">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="47f15-2194">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-2195">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-2195">Az.Monitor</span></span>
* <span data-ttu-id="47f15-2196">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-2196">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2197">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2197">Az.Network</span></span>
* <span data-ttu-id="47f15-2198">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2198">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="47f15-2199">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="47f15-2199">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="47f15-2200">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="47f15-2200">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="47f15-2201">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="47f15-2201">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="47f15-2202">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="47f15-2202">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="47f15-2203">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="47f15-2203">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="47f15-2204">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="47f15-2204">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-2205">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2205">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-2206">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="47f15-2206">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="47f15-2207">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="47f15-2207">Added example</span></span>
    - <span data-ttu-id="47f15-2208">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="47f15-2208">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="47f15-2209">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="47f15-2209">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="47f15-2210">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="47f15-2210">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2211">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2211">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2212">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2212">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2213">Az.Resources</span></span>
* <span data-ttu-id="47f15-2214">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="47f15-2214">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="47f15-2215">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="47f15-2215">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="47f15-2216">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="47f15-2216">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="47f15-2217">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-2217">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="47f15-2218">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47f15-2218">Az.ServiceBus</span></span>
* <span data-ttu-id="47f15-2219">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-2219">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="47f15-2220">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="47f15-2220">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="47f15-2221">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="47f15-2221">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-2222">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-2222">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-2223">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="47f15-2223">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="47f15-2224">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="47f15-2224">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="47f15-2225">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="47f15-2225">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="47f15-2226">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="47f15-2226">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="47f15-2227">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="47f15-2227">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="47f15-2228">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="47f15-2228">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2229">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2229">Az.Sql</span></span>
* <span data-ttu-id="47f15-2230">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="47f15-2230">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2231">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2231">Az.Storage</span></span>
* <span data-ttu-id="47f15-2232">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="47f15-2232">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="47f15-2233">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="47f15-2233">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="47f15-2234">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2234">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="47f15-2235">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="47f15-2235">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="47f15-2236">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="47f15-2236">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="47f15-2237">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="47f15-2237">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2238">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2238">Az.Websites</span></span>
* <span data-ttu-id="47f15-2239">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47f15-2239">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="47f15-2240">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2240">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-2241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2241">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2242">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="47f15-2242">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="47f15-2243">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2243">Az.ApplicationInsights</span></span>
* <span data-ttu-id="47f15-2244">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="47f15-2244">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2245">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2245">Az.Automation</span></span>
* <span data-ttu-id="47f15-2246">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="47f15-2246">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-2247">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2247">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-2248">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="47f15-2248">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2249">Az.Compute</span></span>
* <span data-ttu-id="47f15-2250">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="47f15-2250">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="47f15-2251">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="47f15-2251">Az.ContainerRegistry</span></span>
* <span data-ttu-id="47f15-2252">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="47f15-2252">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="47f15-2253">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="47f15-2253">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-2254">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-2254">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-2255">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-2255">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="47f15-2256">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="47f15-2256">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-2257">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2257">Az.EventHub</span></span>
* <span data-ttu-id="47f15-2258">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="47f15-2258">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="47f15-2259">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="47f15-2259">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-2260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-2260">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-2261">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="47f15-2261">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="47f15-2262">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47f15-2262">Az.LogicApp</span></span>
* <span data-ttu-id="47f15-2263">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="47f15-2263">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="47f15-2264">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="47f15-2264">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="47f15-2265">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2265">Az.ManagedServices</span></span>
* <span data-ttu-id="47f15-2266">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="47f15-2266">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2267">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2267">Az.Network</span></span>
* <span data-ttu-id="47f15-2268">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="47f15-2268">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="47f15-2269">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="47f15-2269">New cmdlets</span></span>
        - <span data-ttu-id="47f15-2270">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="47f15-2270">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="47f15-2271">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="47f15-2271">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="47f15-2272">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2272">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-2273">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2273">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-2274">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2274">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-2275">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2275">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="47f15-2276">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="47f15-2276">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="47f15-2277">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="47f15-2277">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="47f15-2278">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="47f15-2278">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="47f15-2279">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="47f15-2279">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="47f15-2280">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="47f15-2280">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="47f15-2281">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="47f15-2281">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="47f15-2282">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="47f15-2282">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="47f15-2283">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="47f15-2283">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="47f15-2284">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="47f15-2284">Updated cmdlets</span></span>
        - <span data-ttu-id="47f15-2285">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2285">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="47f15-2286">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2286">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="47f15-2287">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2287">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="47f15-2288">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2288">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="47f15-2289">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2289">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="47f15-2290">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="47f15-2290">Updated cmdlet:</span></span>
        - <span data-ttu-id="47f15-2291">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2291">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="47f15-2292">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2292">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="47f15-2293">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2293">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="47f15-2294">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="47f15-2294">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="47f15-2295">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="47f15-2295">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="47f15-2296">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="47f15-2296">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-2297">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2297">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-2298">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="47f15-2298">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="47f15-2299">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="47f15-2299">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2300">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2300">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2301">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2301">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="47f15-2302">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2302">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="47f15-2303">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2303">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="47f15-2304">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2304">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="47f15-2305">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2305">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="47f15-2306">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2306">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="47f15-2307">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2307">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="47f15-2308">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2308">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="47f15-2309">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2309">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="47f15-2310">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="47f15-2310">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2311">Az.Resources</span></span>
- <span data-ttu-id="47f15-2312">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-2312">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="47f15-2313">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="47f15-2313">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="47f15-2314">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47f15-2314">Az.ServiceBus</span></span>
* <span data-ttu-id="47f15-2315">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="47f15-2315">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="47f15-2316">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="47f15-2316">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2317">Az.Sql</span></span>
* <span data-ttu-id="47f15-2318">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="47f15-2318">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="47f15-2319">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="47f15-2319">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="47f15-2320">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="47f15-2320">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2321">Az.Storage</span></span>
* <span data-ttu-id="47f15-2322">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="47f15-2322">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="47f15-2323">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="47f15-2323">Az.StorageSync</span></span>
* <span data-ttu-id="47f15-2324">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="47f15-2324">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="47f15-2325">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="47f15-2325">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2326">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2326">Az.Websites</span></span>
* <span data-ttu-id="47f15-2327">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="47f15-2327">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="47f15-2328">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="47f15-2328">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="47f15-2329">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="47f15-2329">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="47f15-2330">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2330">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-2331">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2331">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2332">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="47f15-2332">Add support for profile cmdlets</span></span>
* <span data-ttu-id="47f15-2333">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="47f15-2333">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="47f15-2334">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="47f15-2334">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="47f15-2335">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="47f15-2335">Az.Advisor</span></span>
* <span data-ttu-id="47f15-2336">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="47f15-2336">GA release of Az.Advisor</span></span>
* <span data-ttu-id="47f15-2337">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="47f15-2337">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="47f15-2338">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-2338">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-2339">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="47f15-2339">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="47f15-2340">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="47f15-2340">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="47f15-2341">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="47f15-2341">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="47f15-2342">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="47f15-2342">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="47f15-2343">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="47f15-2343">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="47f15-2344">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="47f15-2344">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="47f15-2345">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="47f15-2345">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2346">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2346">Az.Automation</span></span>
* <span data-ttu-id="47f15-2347">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="47f15-2347">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2348">Az.Compute</span></span>
* <span data-ttu-id="47f15-2349">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2349">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-2350">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-2350">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-2351">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="47f15-2351">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="47f15-2352">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47f15-2352">Az.EventGrid</span></span>
* <span data-ttu-id="47f15-2353">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="47f15-2353">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-2354">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2354">Az.IotHub</span></span>
* <span data-ttu-id="47f15-2355">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="47f15-2355">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2356">Az.Network</span></span>
* <span data-ttu-id="47f15-2357">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="47f15-2357">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="47f15-2358">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="47f15-2358">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-2359">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2359">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-2360">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="47f15-2360">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="47f15-2361">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="47f15-2361">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-2362">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2362">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-2363">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="47f15-2363">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2364">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2364">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2365">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="47f15-2365">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2366">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2366">Az.Resources</span></span>
    - <span data-ttu-id="47f15-2367">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="47f15-2367">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="47f15-2368">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="47f15-2368">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="47f15-2369">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="47f15-2369">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="47f15-2370">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="47f15-2370">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="47f15-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47f15-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="47f15-2372">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="47f15-2372">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2373">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2373">Az.Sql</span></span>
* <span data-ttu-id="47f15-2374">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="47f15-2374">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="47f15-2375">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="47f15-2375">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="47f15-2376">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="47f15-2376">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="47f15-2377">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="47f15-2377">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="47f15-2378">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="47f15-2378">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="47f15-2379">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="47f15-2379">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="47f15-2380">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="47f15-2380">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="47f15-2381">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="47f15-2381">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="47f15-2382">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="47f15-2382">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2383">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2383">Az.Storage</span></span>
* <span data-ttu-id="47f15-2384">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="47f15-2384">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="47f15-2385">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="47f15-2385">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="47f15-2386">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="47f15-2386">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="47f15-2387">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="47f15-2387">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="47f15-2388">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2388">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="47f15-2389">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2389">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="47f15-2390">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2390">Set-AzStorageAccount</span></span>
* <span data-ttu-id="47f15-2391">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="47f15-2391">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="47f15-2392">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="47f15-2392">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="47f15-2393">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="47f15-2393">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="47f15-2394">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="47f15-2394">Az.StorageSync</span></span>
* <span data-ttu-id="47f15-2395">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="47f15-2395">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="47f15-2396">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2396">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-2397">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2397">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2398">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="47f15-2398">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="47f15-2399">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="47f15-2399">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="47f15-2400">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="47f15-2400">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="47f15-2401">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="47f15-2401">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="47f15-2402">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="47f15-2402">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2403">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2403">Az.Compute</span></span>
* <span data-ttu-id="47f15-2404">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2404">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="47f15-2405">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="47f15-2405">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="47f15-2406">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="47f15-2406">Az.Dns</span></span>
* <span data-ttu-id="47f15-2407">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2407">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="47f15-2408">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47f15-2408">Az.EventGrid</span></span>
* <span data-ttu-id="47f15-2409">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="47f15-2409">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="47f15-2410">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="47f15-2410">New cmdlets:</span></span>
    - <span data-ttu-id="47f15-2411">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="47f15-2411">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="47f15-2412">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-2412">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="47f15-2413">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="47f15-2413">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="47f15-2414">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-2414">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="47f15-2415">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="47f15-2415">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="47f15-2416">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-2416">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="47f15-2417">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="47f15-2417">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="47f15-2418">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-2418">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="47f15-2419">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="47f15-2419">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="47f15-2420">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2420">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="47f15-2421">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="47f15-2421">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="47f15-2422">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-2422">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="47f15-2423">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="47f15-2423">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="47f15-2424">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="47f15-2424">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="47f15-2425">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="47f15-2425">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="47f15-2426">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="47f15-2426">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="47f15-2427">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="47f15-2427">Updated cmdlets:</span></span>
    - <span data-ttu-id="47f15-2428">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="47f15-2428">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="47f15-2429">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2429">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="47f15-2430">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2430">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="47f15-2431">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="47f15-2431">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="47f15-2432">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="47f15-2432">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="47f15-2433">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="47f15-2433">Event subscription expiration date,</span></span>
            - <span data-ttu-id="47f15-2434">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="47f15-2434">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="47f15-2435">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="47f15-2435">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="47f15-2436">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="47f15-2436">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="47f15-2437">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="47f15-2437">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="47f15-2438">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="47f15-2438">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="47f15-2439">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="47f15-2439">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="47f15-2440">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2440">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="47f15-2441">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2441">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-2442">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-2442">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-2443">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="47f15-2443">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="47f15-2444">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="47f15-2444">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="47f15-2445">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="47f15-2445">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="47f15-2446">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="47f15-2446">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2447">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2447">Az.Network</span></span>
* <span data-ttu-id="47f15-2448">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-2448">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="47f15-2449">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="47f15-2449">New cmdlets</span></span>
        - <span data-ttu-id="47f15-2450">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="47f15-2450">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="47f15-2451">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="47f15-2451">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="47f15-2452">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="47f15-2452">New cmdlets</span></span>
        - <span data-ttu-id="47f15-2453">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="47f15-2453">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="47f15-2454">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="47f15-2454">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="47f15-2455">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="47f15-2455">New cmdlets</span></span>
        - <span data-ttu-id="47f15-2456">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="47f15-2456">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="47f15-2457">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="47f15-2457">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="47f15-2458">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="47f15-2458">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="47f15-2459">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2459">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="47f15-2460">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2460">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="47f15-2461">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="47f15-2461">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="47f15-2462">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="47f15-2462">New cmdlets</span></span>
        - <span data-ttu-id="47f15-2463">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="47f15-2463">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="47f15-2464">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="47f15-2464">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="47f15-2465">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="47f15-2465">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="47f15-2466">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2466">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="47f15-2467">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="47f15-2467">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="47f15-2468">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="47f15-2468">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="47f15-2469">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="47f15-2469">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="47f15-2470">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="47f15-2470">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="47f15-2471">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="47f15-2471">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="47f15-2472">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="47f15-2472">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="47f15-2473">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2473">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="47f15-2474">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="47f15-2474">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="47f15-2475">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2475">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="47f15-2476">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="47f15-2476">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="47f15-2477">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="47f15-2477">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="47f15-2478">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="47f15-2478">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="47f15-2479">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="47f15-2479">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="47f15-2480">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2480">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="47f15-2481">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="47f15-2481">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="47f15-2482">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="47f15-2482">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="47f15-2483">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-2483">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="47f15-2484">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="47f15-2484">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="47f15-2485">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="47f15-2485">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="47f15-2486">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="47f15-2486">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="47f15-2487">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-2487">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="47f15-2488">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-2488">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="47f15-2489">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-2489">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-2490">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2490">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-2491">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="47f15-2491">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2492">Az.Resources</span></span>
* <span data-ttu-id="47f15-2493">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="47f15-2493">Support for additional Template Export options</span></span>
    - <span data-ttu-id="47f15-2494">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-2494">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="47f15-2495">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-2495">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="47f15-2496">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="47f15-2496">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-2497">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-2497">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-2498">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="47f15-2498">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2499">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2499">Az.Sql</span></span>
* <span data-ttu-id="47f15-2500">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="47f15-2500">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="47f15-2501">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="47f15-2501">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="47f15-2502">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="47f15-2502">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="47f15-2503">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="47f15-2503">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="47f15-2504">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="47f15-2504">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="47f15-2505">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="47f15-2505">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="47f15-2506">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="47f15-2506">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="47f15-2507">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="47f15-2507">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2508">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2508">Az.Storage</span></span>
* <span data-ttu-id="47f15-2509">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-2509">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="47f15-2510">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2510">New-AzStorageAccount</span></span>
* <span data-ttu-id="47f15-2511">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="47f15-2511">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="47f15-2512">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2512">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2513">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2513">Az.Websites</span></span>
* <span data-ttu-id="47f15-2514">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="47f15-2514">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="47f15-2515">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="47f15-2515">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="47f15-2516">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2516">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="47f15-2517">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-2517">Az.Cdn</span></span>
* <span data-ttu-id="47f15-2518">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="47f15-2518">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2519">Az.Compute</span></span>
* <span data-ttu-id="47f15-2520">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="47f15-2520">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="47f15-2521">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="47f15-2521">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-2522">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2522">Az.EventHub</span></span>
* <span data-ttu-id="47f15-2523">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="47f15-2523">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="47f15-2524">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f15-2524">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2525">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2525">Az.Network</span></span>
* <span data-ttu-id="47f15-2526">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="47f15-2526">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="47f15-2527">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="47f15-2527">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-2528">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2528">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-2529">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="47f15-2529">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2530">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2531">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="47f15-2531">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="47f15-2532">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47f15-2532">Az.ServiceBus</span></span>
* <span data-ttu-id="47f15-2533">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f15-2533">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-2534">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-2534">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-2535">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="47f15-2535">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="47f15-2536">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="47f15-2536">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2537">Az.Sql</span></span>
* <span data-ttu-id="47f15-2538">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="47f15-2538">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="47f15-2539">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2539">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="47f15-2540">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="47f15-2540">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="47f15-2541">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="47f15-2541">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2542">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2542">Az.Websites</span></span>
* <span data-ttu-id="47f15-2543">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="47f15-2543">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="47f15-2544">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2544">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="47f15-2545">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-2545">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-2546">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="47f15-2546">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="47f15-2547">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="47f15-2547">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="47f15-2548">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="47f15-2548">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="47f15-2549">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="47f15-2549">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="47f15-2550">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-2550">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="47f15-2551">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="47f15-2551">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="47f15-2552">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="47f15-2552">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="47f15-2553">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="47f15-2553">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="47f15-2554">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-2554">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="47f15-2555">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="47f15-2555">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="47f15-2556">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2556">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="47f15-2557">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="47f15-2557">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="47f15-2558">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="47f15-2558">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="47f15-2559">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="47f15-2559">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="47f15-2560">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="47f15-2560">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="47f15-2561">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="47f15-2561">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="47f15-2562">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="47f15-2562">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="47f15-2563">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="47f15-2563">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="47f15-2564">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="47f15-2564">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="47f15-2565">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="47f15-2565">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="47f15-2566">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="47f15-2566">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="47f15-2567">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="47f15-2567">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="47f15-2568">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="47f15-2568">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="47f15-2569">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-2569">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="47f15-2570">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="47f15-2570">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="47f15-2571">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="47f15-2571">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="47f15-2572">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2572">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="47f15-2573">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="47f15-2573">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="47f15-2574">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="47f15-2574">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="47f15-2575">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="47f15-2575">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="47f15-2576">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="47f15-2576">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="47f15-2577">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="47f15-2577">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="47f15-2578">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="47f15-2578">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="47f15-2579">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="47f15-2579">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="47f15-2580">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="47f15-2580">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="47f15-2581">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="47f15-2581">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="47f15-2582">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="47f15-2582">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="47f15-2583">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="47f15-2583">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="47f15-2584">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="47f15-2584">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="47f15-2585">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="47f15-2585">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="47f15-2586">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2586">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="47f15-2587">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="47f15-2587">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="47f15-2588">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2588">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="47f15-2589">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="47f15-2589">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="47f15-2590">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="47f15-2590">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="47f15-2591">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2591">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="47f15-2592">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="47f15-2592">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="47f15-2593">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="47f15-2593">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="47f15-2594">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="47f15-2594">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="47f15-2595">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2595">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="47f15-2596">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="47f15-2596">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="47f15-2597">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="47f15-2597">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="47f15-2598">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="47f15-2598">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="47f15-2599">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="47f15-2599">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="47f15-2600">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="47f15-2600">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="47f15-2601">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="47f15-2601">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="47f15-2602">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="47f15-2602">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="47f15-2603">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="47f15-2603">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="47f15-2604">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="47f15-2604">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="47f15-2605">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="47f15-2605">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="47f15-2606">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="47f15-2606">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="47f15-2607">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="47f15-2607">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="47f15-2608">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="47f15-2608">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="47f15-2609">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="47f15-2609">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="47f15-2610">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="47f15-2610">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="47f15-2611">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="47f15-2611">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="47f15-2612">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="47f15-2612">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="47f15-2613">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="47f15-2613">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="47f15-2614">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="47f15-2614">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="47f15-2615">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="47f15-2615">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="47f15-2616">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="47f15-2616">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="47f15-2617">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="47f15-2617">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="47f15-2618">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="47f15-2618">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="47f15-2619">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="47f15-2619">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="47f15-2620">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="47f15-2620">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="47f15-2621">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="47f15-2621">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="47f15-2622">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="47f15-2622">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2623">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2623">Az.Automation</span></span>
* <span data-ttu-id="47f15-2624">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="47f15-2624">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="47f15-2625">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="47f15-2625">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="47f15-2626">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="47f15-2626">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="47f15-2627">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="47f15-2627">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="47f15-2628">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="47f15-2628">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="47f15-2629">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="47f15-2629">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="47f15-2630">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="47f15-2630">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2631">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2631">Az.Compute</span></span>
* <span data-ttu-id="47f15-2632">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="47f15-2632">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="47f15-2633">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="47f15-2633">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-2634">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-2634">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-2635">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2635">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-2636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-2636">Az.Monitor</span></span>
* <span data-ttu-id="47f15-2637">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-2637">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2638">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2638">Az.Network</span></span>
* <span data-ttu-id="47f15-2639">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="47f15-2639">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="47f15-2640">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="47f15-2640">Updated cmdlet:</span></span>
        - <span data-ttu-id="47f15-2641">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="47f15-2641">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="47f15-2642">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="47f15-2642">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2643">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2643">Az.Resources</span></span>
* <span data-ttu-id="47f15-2644">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="47f15-2644">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2645">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2645">Az.Sql</span></span>
* <span data-ttu-id="47f15-2646">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="47f15-2646">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="47f15-2647">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2647">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-2648">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2648">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2649">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="47f15-2649">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-2650">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2650">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-2651">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="47f15-2651">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="47f15-2652">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="47f15-2652">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2653">Az.Compute</span></span>
* <span data-ttu-id="47f15-2654">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="47f15-2654">Proximity placement group feature.</span></span>
    - <span data-ttu-id="47f15-2655">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-2655">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="47f15-2656">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2656">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="47f15-2657">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="47f15-2657">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="47f15-2658">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="47f15-2658">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="47f15-2659">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-2659">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="47f15-2660">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="47f15-2660">Breaking changes</span></span>
    - <span data-ttu-id="47f15-2661">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="47f15-2661">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="47f15-2662">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="47f15-2662">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="47f15-2663">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="47f15-2663">Az.DeploymentManager</span></span>
* <span data-ttu-id="47f15-2664">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2664">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="47f15-2665">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="47f15-2665">Az.Dns</span></span>
* <span data-ttu-id="47f15-2666">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="47f15-2666">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="47f15-2667">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="47f15-2667">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="47f15-2668">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="47f15-2668">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="47f15-2669">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-2669">Az.FrontDoor</span></span>
* <span data-ttu-id="47f15-2670">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2670">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="47f15-2671">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="47f15-2671">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="47f15-2672">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-2672">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-2673">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="47f15-2673">Removed two cmdlets:</span></span>
    - <span data-ttu-id="47f15-2674">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="47f15-2674">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="47f15-2675">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="47f15-2675">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="47f15-2676">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="47f15-2676">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="47f15-2677">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="47f15-2677">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="47f15-2678">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="47f15-2678">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="47f15-2679">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="47f15-2679">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-2680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-2680">Az.Monitor</span></span>
* <span data-ttu-id="47f15-2681">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="47f15-2681">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="47f15-2682">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="47f15-2682">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="47f15-2683">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-2683">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="47f15-2684">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="47f15-2684">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="47f15-2685">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="47f15-2685">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="47f15-2686">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="47f15-2686">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="47f15-2687">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="47f15-2687">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="47f15-2688">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="47f15-2688">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="47f15-2689">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="47f15-2689">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="47f15-2690">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="47f15-2690">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="47f15-2691">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="47f15-2691">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="47f15-2692">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="47f15-2692">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="47f15-2693">[Mais](/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="47f15-2693">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="47f15-2694">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="47f15-2694">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2695">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2695">Az.Network</span></span>
* <span data-ttu-id="47f15-2696">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="47f15-2696">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="47f15-2697">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="47f15-2697">New cmdlets</span></span>
        - <span data-ttu-id="47f15-2698">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="47f15-2698">New-AzNatGateway</span></span>
        - <span data-ttu-id="47f15-2699">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="47f15-2699">Get-AzNatGateway</span></span>
        - <span data-ttu-id="47f15-2700">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="47f15-2700">Set-AzNatGateway</span></span>
        - <span data-ttu-id="47f15-2701">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="47f15-2701">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="47f15-2702">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="47f15-2702">Updated cmdlets</span></span>
        - <span data-ttu-id="47f15-2703">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="47f15-2703">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="47f15-2704">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="47f15-2704">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="47f15-2705">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="47f15-2705">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="47f15-2706">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-2706">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="47f15-2707">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="47f15-2707">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-2708">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2708">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-2709">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="47f15-2709">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="47f15-2710">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="47f15-2710">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="47f15-2711">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="47f15-2711">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2712">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2713">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="47f15-2713">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="47f15-2714">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="47f15-2714">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="47f15-2715">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="47f15-2715">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="47f15-2716">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-2716">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="47f15-2717">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="47f15-2717">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="47f15-2718">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="47f15-2718">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="47f15-2719">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="47f15-2719">Az.Relay</span></span>
* <span data-ttu-id="47f15-2720">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="47f15-2720">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="47f15-2721">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47f15-2721">Az.ServiceBus</span></span>
* <span data-ttu-id="47f15-2722">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="47f15-2722">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2723">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2723">Az.Storage</span></span>
* <span data-ttu-id="47f15-2724">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="47f15-2724">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="47f15-2725">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="47f15-2725">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="47f15-2726">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="47f15-2726">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="47f15-2727">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2727">New-AzStorageAccount</span></span>
* <span data-ttu-id="47f15-2728">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="47f15-2728">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="47f15-2729">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2729">New-AzStorageAccount</span></span>
    - <span data-ttu-id="47f15-2730">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2730">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="47f15-2731">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2731">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2732">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2732">Az.Websites</span></span>
* <span data-ttu-id="47f15-2733">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="47f15-2733">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="47f15-2734">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="47f15-2734">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="47f15-2735">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2735">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="47f15-2736">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="47f15-2736">Highlights since the last major release</span></span>
* <span data-ttu-id="47f15-2737">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="47f15-2737">General availability of `Az` module</span></span>
* <span data-ttu-id="47f15-2738">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="47f15-2738">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="47f15-2739">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="47f15-2739">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="47f15-2740">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2740">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="47f15-2741">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="47f15-2741">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="47f15-2742">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2742">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="47f15-2743">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="47f15-2743">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-2744">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2744">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2745">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="47f15-2745">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="47f15-2746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-2746">Az.Batch</span></span>
* <span data-ttu-id="47f15-2747">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2747">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-2748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-2748">Az.Cdn</span></span>
* <span data-ttu-id="47f15-2749">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2749">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-2750">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2750">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-2751">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2751">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2752">Az.Compute</span></span>
* <span data-ttu-id="47f15-2753">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="47f15-2753">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="47f15-2754">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2754">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="47f15-2755">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="47f15-2755">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-2756">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-2756">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-2757">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="47f15-2757">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-2758">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-2758">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-2759">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2759">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="47f15-2760">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47f15-2760">Az.EventGrid</span></span>
* <span data-ttu-id="47f15-2761">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="47f15-2761">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-2762">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2762">Az.EventHub</span></span>
* <span data-ttu-id="47f15-2763">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="47f15-2763">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="47f15-2764">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="47f15-2764">Az.HDInsight</span></span>
* <span data-ttu-id="47f15-2765">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2765">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-2766">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2766">Az.IotHub</span></span>
* <span data-ttu-id="47f15-2767">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2767">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-2768">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-2768">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-2769">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2769">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="47f15-2770">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="47f15-2770">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="47f15-2771">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="47f15-2771">Az.MachineLearning</span></span>
* <span data-ttu-id="47f15-2772">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2772">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="47f15-2773">Az.Media</span><span class="sxs-lookup"><span data-stu-id="47f15-2773">Az.Media</span></span>
* <span data-ttu-id="47f15-2774">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2774">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-2775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-2775">Az.Monitor</span></span>
  * <span data-ttu-id="47f15-2776">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="47f15-2776">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="47f15-2777">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="47f15-2777">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="47f15-2778">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="47f15-2778">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="47f15-2779">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="47f15-2779">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="47f15-2780">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="47f15-2780">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="47f15-2781">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="47f15-2781">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="47f15-2782">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="47f15-2782">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2783">Az.Network</span></span>
* <span data-ttu-id="47f15-2784">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2784">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="47f15-2785">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="47f15-2785">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="47f15-2786">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="47f15-2786">Az.NotificationHubs</span></span>
* <span data-ttu-id="47f15-2787">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2787">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-2788">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2788">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-2789">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2789">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="47f15-2790">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="47f15-2790">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="47f15-2791">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2791">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2792">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2793">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2793">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="47f15-2794">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2794">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="47f15-2795">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="47f15-2795">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="47f15-2796">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="47f15-2796">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="47f15-2797">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47f15-2797">Az.RedisCache</span></span>
* <span data-ttu-id="47f15-2798">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2798">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2799">Az.Resources</span></span>
* <span data-ttu-id="47f15-2800">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="47f15-2800">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2801">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2801">Az.Sql</span></span>
* <span data-ttu-id="47f15-2802">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="47f15-2802">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="47f15-2803">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2803">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="47f15-2804">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="47f15-2804">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="47f15-2805">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="47f15-2805">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="47f15-2806">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="47f15-2806">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="47f15-2807">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="47f15-2807">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="47f15-2808">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="47f15-2808">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2809">Az.Websites</span></span>
* <span data-ttu-id="47f15-2810">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="47f15-2810">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="47f15-2811">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="47f15-2811">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="47f15-2812">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="47f15-2812">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="47f15-2813">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="47f15-2813">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="47f15-2814">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2814">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="47f15-2815">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="47f15-2815">Highlights since the last major release</span></span>
* <span data-ttu-id="47f15-2816">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="47f15-2816">General availability of `Az` module</span></span>
* <span data-ttu-id="47f15-2817">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="47f15-2817">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="47f15-2818">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="47f15-2818">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="47f15-2819">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2819">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="47f15-2820">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="47f15-2820">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="47f15-2821">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2821">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="47f15-2822">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="47f15-2822">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="47f15-2823">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2823">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2824">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="47f15-2824">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="47f15-2825">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2825">Az.AnalysisServices</span></span>
* <span data-ttu-id="47f15-2826">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="47f15-2826">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="47f15-2827">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="47f15-2827">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2828">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2828">Az.Automation</span></span>
* <span data-ttu-id="47f15-2829">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="47f15-2829">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="47f15-2830">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="47f15-2830">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="47f15-2831">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2831">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2832">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2832">Az.Compute</span></span>
* <span data-ttu-id="47f15-2833">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-2833">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="47f15-2834">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="47f15-2834">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="47f15-2835">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-2835">Az.ContainerInstance</span></span>
* <span data-ttu-id="47f15-2836">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="47f15-2836">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-2837">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-2837">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-2838">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="47f15-2838">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="47f15-2839">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="47f15-2839">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2840">Az.Resources</span></span>
* <span data-ttu-id="47f15-2841">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="47f15-2841">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="47f15-2842">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-2842">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="47f15-2843">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="47f15-2843">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="47f15-2844">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="47f15-2844">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="47f15-2845">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="47f15-2845">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="47f15-2846">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="47f15-2846">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2847">Az.Sql</span></span>
* <span data-ttu-id="47f15-2848">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="47f15-2848">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2849">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2849">Az.Storage</span></span>
* <span data-ttu-id="47f15-2850">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2850">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="47f15-2851">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="47f15-2851">New-AzStorageContext</span></span>
* <span data-ttu-id="47f15-2852">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="47f15-2852">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="47f15-2853">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="47f15-2853">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="47f15-2854">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="47f15-2854">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="47f15-2855">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2855">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="47f15-2856">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2856">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="47f15-2857">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="47f15-2857">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="47f15-2858">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2858">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="47f15-2859">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2859">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="47f15-2860">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2860">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="47f15-2861">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="47f15-2861">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="47f15-2862">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2862">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="47f15-2863">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="47f15-2863">Highlights since the last major release</span></span>
* <span data-ttu-id="47f15-2864">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="47f15-2864">General availability of `Az` module</span></span>
* <span data-ttu-id="47f15-2865">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="47f15-2865">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="47f15-2866">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="47f15-2866">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="47f15-2867">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2867">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="47f15-2868">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="47f15-2868">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="47f15-2869">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2869">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="47f15-2870">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="47f15-2870">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2871">Az.Automation</span></span>
* <span data-ttu-id="47f15-2872">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="47f15-2872">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="47f15-2873">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="47f15-2873">Dynamic grouping</span></span>
    * <span data-ttu-id="47f15-2874">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="47f15-2874">Pre-Post script</span></span>
    * <span data-ttu-id="47f15-2875">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="47f15-2875">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2876">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2876">Az.Compute</span></span>
* <span data-ttu-id="47f15-2877">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="47f15-2877">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="47f15-2878">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="47f15-2878">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-2879">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-2879">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-2880">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-2880">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2881">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2881">Az.Network</span></span>
* <span data-ttu-id="47f15-2882">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2882">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="47f15-2883">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="47f15-2883">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2884">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2884">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2885">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="47f15-2885">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="47f15-2886">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="47f15-2886">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2887">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2887">Az.Resources</span></span>
* <span data-ttu-id="47f15-2888">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47f15-2888">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="47f15-2889">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="47f15-2889">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2890">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2890">Az.Sql</span></span>
* <span data-ttu-id="47f15-2891">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="47f15-2891">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2892">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2892">Az.Storage</span></span>
* <span data-ttu-id="47f15-2893">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-2893">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="47f15-2894">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2894">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="47f15-2895">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2895">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="47f15-2896">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-2896">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="47f15-2897">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="47f15-2897">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="47f15-2898">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="47f15-2898">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="47f15-2899">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="47f15-2899">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2900">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2900">Az.Websites</span></span>
* <span data-ttu-id="47f15-2901">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="47f15-2901">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="47f15-2902">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2902">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-2903">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2903">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2904">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="47f15-2904">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="47f15-2905">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2905">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2906">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2906">Az.Automation</span></span>
* <span data-ttu-id="47f15-2907">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2907">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="47f15-2908">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="47f15-2908">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="47f15-2909">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="47f15-2909">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-2910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-2910">Az.Cdn</span></span>
* <span data-ttu-id="47f15-2911">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="47f15-2911">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2912">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2912">Az.Compute</span></span>
* <span data-ttu-id="47f15-2913">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="47f15-2913">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-2914">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-2914">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-2915">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="47f15-2915">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="47f15-2916">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47f15-2916">Az.LogicApp</span></span>
* <span data-ttu-id="47f15-2917">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="47f15-2917">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2918">Az.Network</span></span>
* <span data-ttu-id="47f15-2919">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2919">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2920">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-2921">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-2921">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="47f15-2922">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="47f15-2922">SDK Update</span></span>
* <span data-ttu-id="47f15-2923">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="47f15-2923">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="47f15-2924">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="47f15-2924">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2925">Az.Resources</span></span>
* <span data-ttu-id="47f15-2926">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="47f15-2926">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="47f15-2927">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="47f15-2927">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="47f15-2928">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="47f15-2928">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="47f15-2929">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="47f15-2929">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="47f15-2930">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="47f15-2930">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="47f15-2931">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="47f15-2931">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2932">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2932">Az.Sql</span></span>
* <span data-ttu-id="47f15-2933">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="47f15-2933">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="47f15-2934">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="47f15-2934">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-2935">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-2935">Az.Storage</span></span>
* <span data-ttu-id="47f15-2936">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2936">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="47f15-2937">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2937">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="47f15-2938">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2938">Az.AnalysisServices</span></span>
* <span data-ttu-id="47f15-2939">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-2939">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-2940">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-2940">Az.Automation</span></span>
* <span data-ttu-id="47f15-2941">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2941">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="47f15-2942">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2942">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="47f15-2943">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2943">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-2944">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2944">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-2945">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="47f15-2945">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2946">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2946">Az.Compute</span></span>
* <span data-ttu-id="47f15-2947">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="47f15-2947">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="47f15-2948">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="47f15-2948">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="47f15-2949">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="47f15-2949">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="47f15-2950">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="47f15-2950">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-2951">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-2951">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-2952">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="47f15-2952">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="47f15-2953">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2953">Az.EventHub</span></span>
* <span data-ttu-id="47f15-2954">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="47f15-2954">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-2955">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-2955">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-2956">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="47f15-2956">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="47f15-2957">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47f15-2957">Az.LogicApp</span></span>
* <span data-ttu-id="47f15-2958">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="47f15-2958">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="47f15-2959">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="47f15-2959">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="47f15-2960">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="47f15-2960">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="47f15-2961">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="47f15-2961">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="47f15-2962">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="47f15-2962">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="47f15-2963">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="47f15-2963">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="47f15-2964">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="47f15-2964">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="47f15-2965">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="47f15-2965">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="47f15-2966">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2966">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="47f15-2967">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2967">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="47f15-2968">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2968">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="47f15-2969">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-2969">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="47f15-2970">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="47f15-2970">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="47f15-2971">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-2971">Az.Monitor</span></span>
* <span data-ttu-id="47f15-2972">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="47f15-2972">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-2973">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-2973">Az.Network</span></span>
* <span data-ttu-id="47f15-2974">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="47f15-2974">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-2975">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-2975">Az.OperationalInsights</span></span>
* <span data-ttu-id="47f15-2976">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="47f15-2976">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="47f15-2977">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="47f15-2977">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="47f15-2978">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="47f15-2978">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-2979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-2979">Az.Resources</span></span>
* <span data-ttu-id="47f15-2980">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="47f15-2980">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="47f15-2981">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="47f15-2981">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="47f15-2982">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="47f15-2982">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="47f15-2983">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="47f15-2983">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-2984">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-2984">Az.Sql</span></span>
* <span data-ttu-id="47f15-2985">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="47f15-2985">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="47f15-2986">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="47f15-2986">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-2987">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-2987">Az.Websites</span></span>
* <span data-ttu-id="47f15-2988">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="47f15-2988">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="47f15-2989">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-2989">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-2990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-2990">Az.Accounts</span></span>
* <span data-ttu-id="47f15-2991">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="47f15-2991">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="47f15-2992">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2992">Az.AnalysisServices</span></span>
<span data-ttu-id="47f15-2993">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="47f15-2993">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-2994">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-2994">Az.Compute</span></span>
* <span data-ttu-id="47f15-2995">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="47f15-2995">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="47f15-2996">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="47f15-2996">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="47f15-2997">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="47f15-2997">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-2998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-2998">Az.RecoveryServices</span></span>
<span data-ttu-id="47f15-2999">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="47f15-2999">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-3000">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3000">Az.Resources</span></span>
* <span data-ttu-id="47f15-3001">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="47f15-3001">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="47f15-3002">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="47f15-3002">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="47f15-3003">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="47f15-3003">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="47f15-3004">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="47f15-3004">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-3005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-3005">Az.Sql</span></span>
* <span data-ttu-id="47f15-3006">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="47f15-3006">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="47f15-3007">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="47f15-3007">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="47f15-3008">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="47f15-3008">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="47f15-3009">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-3009">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-3010">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3010">Az.Accounts</span></span>
* <span data-ttu-id="47f15-3011">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="47f15-3011">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="47f15-3012">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="47f15-3012">Az.AnalysisServices</span></span>
* <span data-ttu-id="47f15-3013">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-3013">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-3014">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-3014">Az.RecoveryServices</span></span>
* <span data-ttu-id="47f15-3015">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-3015">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="47f15-3016">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-3016">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-3017">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3017">Az.Accounts</span></span>
* <span data-ttu-id="47f15-3018">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="47f15-3018">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="47f15-3019">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3019">Update incorrect online help URLs</span></span>
* <span data-ttu-id="47f15-3020">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="47f15-3020">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="47f15-3021">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="47f15-3021">Az.Aks</span></span>
* <span data-ttu-id="47f15-3022">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3022">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="47f15-3023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-3023">Az.Automation</span></span>
* <span data-ttu-id="47f15-3024">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="47f15-3024">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="47f15-3025">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3025">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="47f15-3026">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="47f15-3026">Az.Cdn</span></span>
* <span data-ttu-id="47f15-3027">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3027">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-3028">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-3028">Az.Compute</span></span>
* <span data-ttu-id="47f15-3029">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="47f15-3029">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="47f15-3030">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="47f15-3030">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="47f15-3031">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="47f15-3031">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="47f15-3032">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="47f15-3032">Az.ContainerRegistry</span></span>
* <span data-ttu-id="47f15-3033">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3033">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="47f15-3034">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="47f15-3034">Az.DataFactory</span></span>
* <span data-ttu-id="47f15-3035">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="47f15-3035">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-3036">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-3036">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-3037">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="47f15-3037">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="47f15-3038">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="47f15-3038">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="47f15-3039">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3039">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-3040">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-3040">Az.IotHub</span></span>
* <span data-ttu-id="47f15-3041">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="47f15-3041">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="47f15-3042">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-3042">Az.KeyVault</span></span>
* <span data-ttu-id="47f15-3043">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3043">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-3044">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-3044">Az.Network</span></span>
* <span data-ttu-id="47f15-3045">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3045">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-3046">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3046">Az.Resources</span></span>
* <span data-ttu-id="47f15-3047">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="47f15-3047">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="47f15-3048">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="47f15-3048">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="47f15-3049">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="47f15-3049">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="47f15-3050">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="47f15-3050">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="47f15-3051">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="47f15-3051">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="47f15-3052">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="47f15-3052">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="47f15-3053">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="47f15-3053">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-3054">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-3054">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-3055">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="47f15-3055">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="47f15-3056">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="47f15-3056">Fix some error messages.</span></span>
* <span data-ttu-id="47f15-3057">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="47f15-3057">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="47f15-3058">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="47f15-3058">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="47f15-3059">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="47f15-3059">Az.SignalR</span></span>
* <span data-ttu-id="47f15-3060">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3060">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-3061">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-3061">Az.Sql</span></span>
* <span data-ttu-id="47f15-3062">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3062">Update incorrect online help URLs</span></span>
* <span data-ttu-id="47f15-3063">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="47f15-3063">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="47f15-3064">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="47f15-3064">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="47f15-3065">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="47f15-3065">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-3066">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-3066">Az.Storage</span></span>
* <span data-ttu-id="47f15-3067">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3067">Update incorrect online help URLs</span></span>
* <span data-ttu-id="47f15-3068">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="47f15-3068">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="47f15-3069">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="47f15-3069">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="47f15-3070">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="47f15-3070">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="47f15-3071">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="47f15-3071">Az.TrafficManager</span></span>
* <span data-ttu-id="47f15-3072">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3072">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-3073">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-3073">Az.Websites</span></span>
* <span data-ttu-id="47f15-3074">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="47f15-3074">Update incorrect online help URLs</span></span>
* <span data-ttu-id="47f15-3075">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="47f15-3075">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="47f15-3076">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="47f15-3076">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="47f15-3077">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="47f15-3077">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="47f15-3078">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3078">Az.Accounts</span></span>
* <span data-ttu-id="47f15-3079">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="47f15-3079">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-3080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-3080">Az.Compute</span></span>
* <span data-ttu-id="47f15-3081">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="47f15-3081">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="47f15-3082">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="47f15-3082">Updated the description of ID in help files</span></span>
* <span data-ttu-id="47f15-3083">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3083">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-3084">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-3084">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-3085">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="47f15-3085">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="47f15-3086">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="47f15-3086">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="47f15-3087">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="47f15-3087">Az.EventGrid</span></span>
* <span data-ttu-id="47f15-3088">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="47f15-3088">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="47f15-3089">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="47f15-3089">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="47f15-3090">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="47f15-3090">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="47f15-3091">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="47f15-3091">Event Time-To-Live,</span></span>
        - <span data-ttu-id="47f15-3092">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="47f15-3092">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="47f15-3093">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="47f15-3093">Dead letter endpoint.</span></span>
    - <span data-ttu-id="47f15-3094">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="47f15-3094">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="47f15-3095">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="47f15-3095">Event Time-To-Live,</span></span>
        - <span data-ttu-id="47f15-3096">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="47f15-3096">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="47f15-3097">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="47f15-3097">Dead letter endpoint.</span></span>
* <span data-ttu-id="47f15-3098">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="47f15-3098">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="47f15-3099">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="47f15-3099">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="47f15-3100">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-3100">Az.IotHub</span></span>
* <span data-ttu-id="47f15-3101">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="47f15-3101">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="47f15-3102">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="47f15-3102">Az.LogicApp</span></span>
* <span data-ttu-id="47f15-3103">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="47f15-3103">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-3104">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3104">Az.Resources</span></span>
* <span data-ttu-id="47f15-3105">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="47f15-3105">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="47f15-3106">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="47f15-3106">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="47f15-3107">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="47f15-3107">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="47f15-3108">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="47f15-3108">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="47f15-3109">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="47f15-3109">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="47f15-3110">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="47f15-3110">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="47f15-3111">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="47f15-3111">Az.SignalR</span></span>
* <span data-ttu-id="47f15-3112">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3112">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-3113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-3113">Az.Sql</span></span>
* <span data-ttu-id="47f15-3114">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="47f15-3114">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="47f15-3115">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-3115">Az.Storage</span></span>
* <span data-ttu-id="47f15-3116">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="47f15-3116">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="47f15-3117">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="47f15-3117">New-AzStorageContext</span></span>
* <span data-ttu-id="47f15-3118">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="47f15-3118">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="47f15-3119">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="47f15-3119">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-3120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-3120">Az.Websites</span></span>
* <span data-ttu-id="47f15-3121">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="47f15-3121">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="47f15-3122">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3122">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="47f15-3123">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="47f15-3123">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="47f15-3124">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-3124">General</span></span>

- <span data-ttu-id="47f15-3125">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="47f15-3125">General Availability of Az Module</span></span>
- <span data-ttu-id="47f15-3126">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="47f15-3126">Online help for each module</span></span>
- <span data-ttu-id="47f15-3127">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="47f15-3127">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="47f15-3128">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="47f15-3128">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="47f15-3129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3129">Az.Accounts</span></span>
- <span data-ttu-id="47f15-3130">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="47f15-3130">Changed from Az.Profile</span></span>
- <span data-ttu-id="47f15-3131">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="47f15-3131">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="47f15-3132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-3132">Az.ApiManagement</span></span>
- <span data-ttu-id="47f15-3133">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="47f15-3133">Fixes for #7002</span></span>
- <span data-ttu-id="47f15-3134">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3134">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="47f15-3135">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="47f15-3135">Az.Batch</span></span>
- <span data-ttu-id="47f15-3136">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="47f15-3136">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="47f15-3137">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="47f15-3137">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="47f15-3138">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3138">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="47f15-3139">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="47f15-3139">Az.Billing</span></span>
- <span data-ttu-id="47f15-3140">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3140">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="47f15-3141">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="47f15-3141">Az.CognitivServices</span></span>
- <span data-ttu-id="47f15-3142">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-3142">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="47f15-3143">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="47f15-3143">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="47f15-3144">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-3144">Az.ContainerInstance</span></span>
- <span data-ttu-id="47f15-3145">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="47f15-3145">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="47f15-3146">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="47f15-3146">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="47f15-3147">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3147">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="47f15-3148">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-3148">Az.DataLakeStore</span></span>
- <span data-ttu-id="47f15-3149">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3149">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="47f15-3150">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="47f15-3150">Az.Monitor</span></span>
- <span data-ttu-id="47f15-3151">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3151">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="47f15-3152">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="47f15-3152">Az.KeyVault</span></span>
- <span data-ttu-id="47f15-3153">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="47f15-3153">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="47f15-3154">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="47f15-3154">Az.MachineLearning</span></span>
- <span data-ttu-id="47f15-3155">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="47f15-3155">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="47f15-3156">Az.Media</span><span class="sxs-lookup"><span data-stu-id="47f15-3156">Az.Media</span></span>
- <span data-ttu-id="47f15-3157">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="47f15-3157">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="47f15-3158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-3158">Az.Network</span></span>
<span data-ttu-id="47f15-3159">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="47f15-3159">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="47f15-3160">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="47f15-3160">New cmdlets added:</span></span>
        - <span data-ttu-id="47f15-3161">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-3161">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="47f15-3162">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-3162">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="47f15-3163">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-3163">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="47f15-3164">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-3164">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="47f15-3165">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-3165">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="47f15-3166">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="47f15-3166">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="47f15-3167">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="47f15-3167">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="47f15-3168">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="47f15-3168">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="47f15-3169">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="47f15-3169">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="47f15-3170">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47f15-3170">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="47f15-3171">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="47f15-3171">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="47f15-3172">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="47f15-3172">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="47f15-3173">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-3173">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="47f15-3174">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-3174">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="47f15-3175">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="47f15-3175">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="47f15-3176">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="47f15-3176">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="47f15-3177">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="47f15-3177">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="47f15-3178">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="47f15-3178">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="47f15-3179">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="47f15-3179">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="47f15-3180">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="47f15-3180">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="47f15-3181">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3181">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="47f15-3182">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-3182">Az.OperationalInsights</span></span>
- <span data-ttu-id="47f15-3183">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3183">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="47f15-3184">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="47f15-3184">Az.Profile</span></span>
- <span data-ttu-id="47f15-3185">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="47f15-3185">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-3186">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-3186">Az.RecoveryServices</span></span>
- <span data-ttu-id="47f15-3187">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3187">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="47f15-3188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3188">Az.Resources</span></span>
- <span data-ttu-id="47f15-3189">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3189">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="47f15-3190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-3190">Az.ServiceFabric</span></span>
- <span data-ttu-id="47f15-3191">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="47f15-3191">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="47f15-3192">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3192">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="47f15-3193">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="47f15-3193">Az.SIgnalR</span></span>
- <span data-ttu-id="47f15-3194">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="47f15-3194">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="47f15-3195">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-3195">Az.Sql</span></span>
- <span data-ttu-id="47f15-3196">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="47f15-3196">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="47f15-3197">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="47f15-3197">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="47f15-3198">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3198">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="47f15-3199">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-3199">Az.Storage</span></span>
- <span data-ttu-id="47f15-3200">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3200">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="47f15-3201">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-3201">Az.Websites</span></span>
- <span data-ttu-id="47f15-3202">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="47f15-3202">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="47f15-3203">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="47f15-3203">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="47f15-3204">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-3204">General</span></span>

* <span data-ttu-id="47f15-3205">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="47f15-3205">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="47f15-3206">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-3206">Az.Compute</span></span>

* <span data-ttu-id="47f15-3207">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="47f15-3207">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="47f15-3208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-3208">Az.DataLakeStore</span></span>

* <span data-ttu-id="47f15-3209">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="47f15-3209">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="47f15-3210">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="47f15-3210">Az.FrontDoor</span></span>

* <span data-ttu-id="47f15-3211">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="47f15-3211">Fixed some broken links</span></span>
    - <span data-ttu-id="47f15-3212">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="47f15-3212">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="47f15-3213">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="47f15-3213">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="47f15-3214">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="47f15-3214">Az.RecoveryServices</span></span>

* <span data-ttu-id="47f15-3215">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="47f15-3215">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="47f15-3216">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="47f15-3216">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="47f15-3217">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3217">Az.Resources</span></span>

* <span data-ttu-id="47f15-3218">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="47f15-3218">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="47f15-3219">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="47f15-3219">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="47f15-3220">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-3220">Az.Sql</span></span>

* <span data-ttu-id="47f15-3221">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="47f15-3221">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="47f15-3222">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="47f15-3222">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="47f15-3223">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="47f15-3223">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="47f15-3224">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-3224">Az.Storage</span></span>

* <span data-ttu-id="47f15-3225">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-3225">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="47f15-3226">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="47f15-3226">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="47f15-3227">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="47f15-3227">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="47f15-3228">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="47f15-3228">Support Static Website configuration</span></span>
    - <span data-ttu-id="47f15-3229">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="47f15-3229">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="47f15-3230">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="47f15-3230">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="47f15-3231">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-3231">Az.Websites</span></span>

* <span data-ttu-id="47f15-3232">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="47f15-3232">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="47f15-3233">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="47f15-3233">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="47f15-3234">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="47f15-3234">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="47f15-3235">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="47f15-3235">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="47f15-3236">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="47f15-3236">Az.ApiManagement</span></span>
* <span data-ttu-id="47f15-3237">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="47f15-3237">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="47f15-3238">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="47f15-3238">Az.Automation</span></span>
* <span data-ttu-id="47f15-3239">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="47f15-3239">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="47f15-3240">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-3240">Added Update Management cmdlets</span></span>
* <span data-ttu-id="47f15-3241">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-3241">Added Source Control cmdlets</span></span>
* <span data-ttu-id="47f15-3242">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="47f15-3242">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="47f15-3243">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="47f15-3243">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="47f15-3244">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-3244">Az.Compute</span></span>
* <span data-ttu-id="47f15-3245">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="47f15-3245">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="47f15-3246">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="47f15-3246">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="47f15-3247">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-3247">Az.ContainerInstance</span></span>
* <span data-ttu-id="47f15-3248">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="47f15-3248">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="47f15-3249">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="47f15-3249">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="47f15-3250">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="47f15-3250">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="47f15-3251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-3251">Az.Network</span></span>
* <span data-ttu-id="47f15-3252">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-3252">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="47f15-3253">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="47f15-3253">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="47f15-3254">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="47f15-3254">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="47f15-3255">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="47f15-3255">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="47f15-3256">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="47f15-3256">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="47f15-3257">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="47f15-3257">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="47f15-3258">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="47f15-3258">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="47f15-3259">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="47f15-3259">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="47f15-3260">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="47f15-3260">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="47f15-3261">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="47f15-3261">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="47f15-3262">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="47f15-3262">Az.Relay</span></span>
* <span data-ttu-id="47f15-3263">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="47f15-3263">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="47f15-3264">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3264">Az.Resources</span></span>
* <span data-ttu-id="47f15-3265">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="47f15-3265">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="47f15-3266">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="47f15-3266">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="47f15-3267">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="47f15-3267">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="47f15-3268">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-3268">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-3269">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="47f15-3269">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="47f15-3270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-3270">Az.Sql</span></span>
* <span data-ttu-id="47f15-3271">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="47f15-3271">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="47f15-3272">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-3272">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47f15-3273">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-3273">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47f15-3274">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-3274">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47f15-3275">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="47f15-3275">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="47f15-3276">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47f15-3276">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47f15-3277">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47f15-3277">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47f15-3278">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47f15-3278">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="47f15-3279">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="47f15-3279">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="47f15-3280">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="47f15-3280">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="47f15-3281">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="47f15-3281">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="47f15-3282">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="47f15-3282">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="47f15-3283">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="47f15-3283">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="47f15-3284">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="47f15-3284">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="47f15-3285">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="47f15-3285">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="47f15-3286">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="47f15-3286">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="47f15-3287">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="47f15-3287">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="47f15-3288">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="47f15-3288">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="47f15-3289">Geral</span><span class="sxs-lookup"><span data-stu-id="47f15-3289">General</span></span>
* <span data-ttu-id="47f15-3290">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="47f15-3290">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="47f15-3291">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="47f15-3291">Az.Profile</span></span>
* <span data-ttu-id="47f15-3292">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="47f15-3292">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="47f15-3293">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="47f15-3293">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="47f15-3294">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="47f15-3294">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="47f15-3295">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="47f15-3295">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="47f15-3296">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="47f15-3296">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="47f15-3297">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="47f15-3297">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="47f15-3298">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="47f15-3298">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-3299">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-3299">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-3300">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="47f15-3300">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-3301">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-3301">Az.Compute</span></span>
* <span data-ttu-id="47f15-3302">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="47f15-3302">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="47f15-3303">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="47f15-3303">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="47f15-3304">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="47f15-3304">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-3305">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-3305">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-3306">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="47f15-3306">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="47f15-3307">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="47f15-3307">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="47f15-3308">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="47f15-3308">Az.Insights</span></span>
* <span data-ttu-id="47f15-3309">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="47f15-3309">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="47f15-3310">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="47f15-3310">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="47f15-3311">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="47f15-3311">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="47f15-3312">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="47f15-3312">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-3313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-3313">Az.Network</span></span>
* <span data-ttu-id="47f15-3314">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="47f15-3314">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="47f15-3315">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="47f15-3315">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="47f15-3316">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="47f15-3316">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="47f15-3317">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47f15-3317">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="47f15-3318">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="47f15-3318">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="47f15-3319">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="47f15-3319">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="47f15-3320">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="47f15-3320">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="47f15-3321">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="47f15-3321">Az.PolicyInsights</span></span>
* <span data-ttu-id="47f15-3322">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="47f15-3322">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-3323">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3323">Az.Resources</span></span>
* <span data-ttu-id="47f15-3324">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="47f15-3324">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="47f15-3325">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="47f15-3325">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="47f15-3326">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="47f15-3326">Az.ServiceBus</span></span>
* <span data-ttu-id="47f15-3327">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="47f15-3327">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="47f15-3328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="47f15-3328">Az.ServiceFabric</span></span>
* <span data-ttu-id="47f15-3329">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="47f15-3329">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="47f15-3330">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="47f15-3330">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="47f15-3331">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="47f15-3331">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="47f15-3332">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="47f15-3332">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="47f15-3333">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="47f15-3333">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="47f15-3334">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="47f15-3334">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="47f15-3335">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="47f15-3335">Az.Profile</span></span>
* <span data-ttu-id="47f15-3336">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="47f15-3336">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="47f15-3337">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="47f15-3337">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-3338">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-3338">Az.Compute</span></span>
* <span data-ttu-id="47f15-3339">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="47f15-3339">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="47f15-3340">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="47f15-3340">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="47f15-3341">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="47f15-3341">Az.DataLakeStore</span></span>
* <span data-ttu-id="47f15-3342">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="47f15-3342">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="47f15-3343">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47f15-3343">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="47f15-3344">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="47f15-3344">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="47f15-3345">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="47f15-3345">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="47f15-3346">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="47f15-3346">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-3347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-3347">Az.Network</span></span>
* <span data-ttu-id="47f15-3348">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="47f15-3348">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="47f15-3349">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="47f15-3349">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-3350">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3350">Az.Resources</span></span>
* <span data-ttu-id="47f15-3351">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="47f15-3351">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="47f15-3352">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="47f15-3352">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="47f15-3353">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="47f15-3353">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="47f15-3354">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="47f15-3354">Azure.Storage</span></span>
* <span data-ttu-id="47f15-3355">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="47f15-3355">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="47f15-3356">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="47f15-3356">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="47f15-3357">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="47f15-3357">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="47f15-3358">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="47f15-3358">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="47f15-3359">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="47f15-3359">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="47f15-3360">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="47f15-3360">Az.CognitiveServices</span></span>
* <span data-ttu-id="47f15-3361">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="47f15-3361">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="47f15-3362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="47f15-3362">Az.Compute</span></span>
* <span data-ttu-id="47f15-3363">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="47f15-3363">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="47f15-3364">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="47f15-3364">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="47f15-3365">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="47f15-3365">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="47f15-3366">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="47f15-3366">Az.DataFactoryV2</span></span>
* <span data-ttu-id="47f15-3367">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="47f15-3367">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="47f15-3368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="47f15-3368">Az.Network</span></span>
* <span data-ttu-id="47f15-3369">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="47f15-3369">Added NetworkProfile functionality.</span></span> <span data-ttu-id="47f15-3370">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="47f15-3370">new cmdlets added</span></span>
    - <span data-ttu-id="47f15-3371">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47f15-3371">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="47f15-3372">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47f15-3372">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="47f15-3373">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47f15-3373">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="47f15-3374">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="47f15-3374">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="47f15-3375">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-3375">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="47f15-3376">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-3376">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="47f15-3377">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="47f15-3377">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="47f15-3378">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="47f15-3378">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="47f15-3379">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="47f15-3379">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="47f15-3380">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="47f15-3380">Az.RedisCache</span></span>
* <span data-ttu-id="47f15-3381">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="47f15-3381">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="47f15-3382">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="47f15-3382">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="47f15-3383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="47f15-3383">Az.Resources</span></span>
* <span data-ttu-id="47f15-3384">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="47f15-3384">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="47f15-3385">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="47f15-3385">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="47f15-3386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="47f15-3386">Az.Sql</span></span>
* <span data-ttu-id="47f15-3387">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="47f15-3387">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="47f15-3388">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="47f15-3388">Az.Websites</span></span>
* <span data-ttu-id="47f15-3389">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="47f15-3389">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="47f15-3390">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="47f15-3390">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="47f15-3391">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="47f15-3391">0.2.0 - September 2018</span></span>
 <span data-ttu-id="47f15-3392">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="47f15-3392">Initial Release</span></span>