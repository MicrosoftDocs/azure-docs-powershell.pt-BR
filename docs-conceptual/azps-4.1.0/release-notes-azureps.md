---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 60827fe7b4f8c351655046e3711660cdf7ce0513
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83631057"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="60598-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="60598-103">Azure PowerShell release notes</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="60598-104">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-104">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="60598-105">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="60598-105">Highlights since the last release</span></span>
* <span data-ttu-id="60598-106">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="60598-106">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="60598-107">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="60598-107">General availability of Az.Functions</span></span> 
* <span data-ttu-id="60598-108">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="60598-108">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-109">Az.Accounts</span></span>
* <span data-ttu-id="60598-110">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="60598-110">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="60598-111">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="60598-111">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="60598-112">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="60598-112">Az.Aks</span></span>
* <span data-ttu-id="60598-113">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="60598-113">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="60598-114">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="60598-114">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="60598-115">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="60598-115">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="60598-116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-116">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-117">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="60598-117">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="60598-118">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="60598-118">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="60598-119">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="60598-119">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="60598-120">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="60598-120">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="60598-121">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="60598-121">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="60598-122">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="60598-122">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="60598-123">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="60598-123">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="60598-124">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="60598-124">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="60598-125">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="60598-125">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="60598-126">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="60598-126">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="60598-127">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="60598-127">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="60598-128">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="60598-128">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="60598-129">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="60598-129">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="60598-130">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="60598-130">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="60598-131">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="60598-131">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="60598-132">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="60598-132">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="60598-133">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="60598-133">Az.ApplicationInsights</span></span>
* <span data-ttu-id="60598-134">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="60598-134">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="60598-135">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="60598-135">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="60598-136">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="60598-136">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="60598-137">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="60598-137">Az.Batch</span></span>
* <span data-ttu-id="60598-138">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="60598-138">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="60598-139">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="60598-139">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="60598-140">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="60598-140">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="60598-141">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="60598-141">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="60598-142">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="60598-142">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="60598-143">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="60598-143">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="60598-144">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="60598-144">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="60598-145">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="60598-145">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="60598-146">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="60598-146">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-147">Az.Compute</span></span>
* <span data-ttu-id="60598-148">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="60598-148">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="60598-149">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="60598-149">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="60598-150">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="60598-150">Breaking changes</span></span>
    - <span data-ttu-id="60598-151">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="60598-151">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="60598-152">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="60598-152">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="60598-153">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="60598-153">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="60598-154">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="60598-154">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="60598-155">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="60598-155">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="60598-156">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="60598-156">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="60598-157">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="60598-157">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="60598-158">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-158">Az.DataFactory</span></span>
* <span data-ttu-id="60598-159">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="60598-159">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="60598-160">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-160">Az.FrontDoor</span></span>
* <span data-ttu-id="60598-161">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="60598-161">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="60598-162">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="60598-162">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="60598-163">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="60598-163">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="60598-164">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="60598-164">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="60598-165">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="60598-165">Az.Functions</span></span>
* <span data-ttu-id="60598-166">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="60598-166">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="60598-167">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-167">Az.HDInsight</span></span>
* <span data-ttu-id="60598-168">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="60598-168">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="60598-169">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="60598-169">Az.HealthcareApis</span></span>
* <span data-ttu-id="60598-170">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="60598-170">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-171">Az.IotHub</span></span>
* <span data-ttu-id="60598-172">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="60598-172">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="60598-173">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="60598-173">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="60598-174">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="60598-174">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="60598-175">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="60598-175">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="60598-176">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="60598-176">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="60598-177">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-177">New cmdlets are:</span></span>
    - <span data-ttu-id="60598-178">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-178">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="60598-179">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-179">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="60598-180">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-180">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="60598-181">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-181">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="60598-182">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="60598-182">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="60598-183">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="60598-183">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-184">Az.KeyVault</span></span>
* <span data-ttu-id="60598-185">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="60598-185">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="60598-186">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="60598-186">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="60598-187">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="60598-187">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="60598-188">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="60598-188">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="60598-189">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="60598-189">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="60598-190">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="60598-190">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="60598-191">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="60598-191">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-192">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-192">Az.Monitor</span></span>
* <span data-ttu-id="60598-193">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="60598-193">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="60598-194">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="60598-194">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="60598-195">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="60598-195">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="60598-196">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="60598-196">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="60598-197">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="60598-197">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="60598-198">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="60598-198">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="60598-199">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="60598-199">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-200">Az.Network</span></span>
* <span data-ttu-id="60598-201">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="60598-201">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="60598-202">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="60598-202">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="60598-203">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="60598-203">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="60598-204">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="60598-204">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="60598-205">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="60598-205">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="60598-206">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-206">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-207">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="60598-207">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="60598-208">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="60598-208">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="60598-209">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="60598-209">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="60598-210">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="60598-210">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="60598-211">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="60598-211">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="60598-212">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="60598-212">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="60598-213">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="60598-213">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="60598-214">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="60598-214">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="60598-215">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="60598-215">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="60598-216">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="60598-216">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="60598-217">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="60598-217">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="60598-218">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="60598-218">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="60598-219">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="60598-219">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="60598-220">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="60598-220">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="60598-221">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="60598-221">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="60598-222">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="60598-222">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="60598-223">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="60598-223">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="60598-224">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60598-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="60598-225">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="60598-225">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="60598-226">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-226">Az.OperationalInsights</span></span>
* <span data-ttu-id="60598-227">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="60598-227">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="60598-228">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="60598-228">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="60598-229">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="60598-229">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="60598-230">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="60598-230">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="60598-231">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="60598-231">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="60598-232">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="60598-232">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="60598-233">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="60598-233">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="60598-234">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="60598-234">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-235">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-235">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-236">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-236">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="60598-237">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="60598-237">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="60598-238">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="60598-238">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="60598-239">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="60598-239">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="60598-240">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="60598-240">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-241">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-241">Az.Resources</span></span>
* <span data-ttu-id="60598-242">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="60598-242">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="60598-243">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="60598-243">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="60598-244">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="60598-244">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="60598-245">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="60598-245">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="60598-246">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="60598-246">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="60598-247">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="60598-247">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="60598-248">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="60598-248">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="60598-249">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="60598-249">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="60598-250">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="60598-250">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="60598-251">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="60598-251">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="60598-252">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="60598-252">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="60598-253">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="60598-253">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="60598-254">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="60598-254">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="60598-255">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="60598-255">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="60598-256">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="60598-256">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="60598-257">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="60598-257">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="60598-258">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-258">'New-AzDeployment'</span></span>
    - <span data-ttu-id="60598-259">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-259">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="60598-260">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-260">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="60598-261">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-261">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-262">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-262">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-263">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="60598-263">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-264">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-264">Az.Sql</span></span>
* <span data-ttu-id="60598-265">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="60598-265">Enhance performance of:</span></span>
    - <span data-ttu-id="60598-266">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="60598-266">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="60598-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="60598-267">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="60598-268">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="60598-268">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="60598-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="60598-269">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="60598-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="60598-270">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="60598-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="60598-271">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="60598-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="60598-272">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="60598-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="60598-273">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="60598-274">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="60598-274">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="60598-275">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="60598-275">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-276">Az.Storage</span></span>
* <span data-ttu-id="60598-277">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-277">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="60598-278">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="60598-278">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="60598-279">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-279">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="60598-280">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="60598-280">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="60598-281">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="60598-281">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="60598-282">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="60598-282">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="60598-283">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="60598-283">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="60598-284">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="60598-284">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="60598-285">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="60598-285">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="60598-286">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="60598-286">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="60598-287">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="60598-287">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="60598-288">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="60598-288">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="60598-289">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="60598-289">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="60598-290">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-290">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="60598-291">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-291">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="60598-292">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-292">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="60598-293">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60598-293">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="60598-294">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="60598-294">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="60598-295">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="60598-295">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="60598-296">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="60598-296">Supported failover Storage account</span></span>
    - <span data-ttu-id="60598-297">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="60598-297">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="60598-298">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="60598-298">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="60598-299">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="60598-299">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="60598-300">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="60598-300">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="60598-301">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="60598-301">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="60598-302">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="60598-302">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="60598-303">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="60598-303">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="60598-304">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="60598-304">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="60598-305">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="60598-305">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="60598-306">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="60598-306">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="60598-307">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="60598-307">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="60598-308">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="60598-308">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="60598-309">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="60598-309">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="60598-310">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="60598-310">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="60598-311">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="60598-311">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="60598-312">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="60598-312">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="60598-313">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="60598-313">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="60598-314">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="60598-314">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="60598-315">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="60598-315">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="60598-316">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="60598-316">Az.TrafficManager</span></span>
* <span data-ttu-id="60598-317">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="60598-317">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-318">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-318">Az.Websites</span></span>
* <span data-ttu-id="60598-319">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="60598-319">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="60598-320">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-320">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="60598-321">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="60598-321">Highlights since the last release</span></span>
* <span data-ttu-id="60598-322">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="60598-322">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-323">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-323">Az.Accounts</span></span>
* <span data-ttu-id="60598-324">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="60598-324">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="60598-325">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-325">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-326">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="60598-326">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="60598-327">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="60598-327">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="60598-328">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-328">Az.Cdn</span></span>
* <span data-ttu-id="60598-329">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="60598-329">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-330">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-330">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-331">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="60598-331">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-332">Az.Compute</span></span>
* <span data-ttu-id="60598-333">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="60598-333">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="60598-334">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="60598-334">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-335">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-335">Az.IotHub</span></span>
* <span data-ttu-id="60598-336">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-336">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="60598-337">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="60598-337">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="60598-338">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="60598-338">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="60598-339">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="60598-339">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="60598-340">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-340">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="60598-341">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="60598-341">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="60598-342">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="60598-342">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="60598-343">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="60598-343">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="60598-344">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-344">New cmdlets are:</span></span>
    - <span data-ttu-id="60598-345">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="60598-345">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="60598-346">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="60598-346">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="60598-347">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="60598-347">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="60598-348">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="60598-348">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="60598-349">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="60598-349">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-350">Az.KeyVault</span></span>
* <span data-ttu-id="60598-351">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="60598-351">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="60598-352">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="60598-352">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="60598-353">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="60598-353">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="60598-354">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="60598-354">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="60598-355">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="60598-355">Az.Maintenance</span></span>
* <span data-ttu-id="60598-356">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="60598-356">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-357">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-357">Az.Monitor</span></span>
* <span data-ttu-id="60598-358">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="60598-358">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="60598-359">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="60598-359">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="60598-360">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="60598-360">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="60598-361">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="60598-361">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="60598-362">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="60598-362">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="60598-363">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="60598-363">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="60598-364">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="60598-364">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="60598-365">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="60598-365">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-366">Az.Network</span></span>
* <span data-ttu-id="60598-367">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="60598-367">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="60598-368">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="60598-368">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="60598-369">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="60598-369">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="60598-370">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="60598-370">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="60598-371">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="60598-371">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="60598-372">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="60598-372">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="60598-373">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="60598-373">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="60598-374">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="60598-374">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="60598-375">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="60598-375">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="60598-376">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-376">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="60598-377">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="60598-377">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="60598-378">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="60598-378">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="60598-379">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="60598-379">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="60598-380">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="60598-380">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="60598-381">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="60598-381">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="60598-382">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="60598-382">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="60598-383">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="60598-383">Az.PolicyInsights</span></span>
* <span data-ttu-id="60598-384">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="60598-384">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="60598-385">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="60598-385">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-386">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-386">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-387">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="60598-387">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-388">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-388">Az.Sql</span></span>
* <span data-ttu-id="60598-389">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-389">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="60598-390">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="60598-390">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-391">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-391">Az.Storage</span></span>
* <span data-ttu-id="60598-392">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="60598-392">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="60598-393">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60598-393">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="60598-394">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-394">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="60598-395">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-395">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="60598-396">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="60598-396">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="60598-397">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="60598-397">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="60598-398">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="60598-398">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="60598-399">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="60598-399">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="60598-400">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="60598-400">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="60598-401">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="60598-401">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="60598-402">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="60598-402">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="60598-403">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="60598-403">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="60598-404">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="60598-404">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="60598-405">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-405">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="60598-406">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-406">General</span></span>
* <span data-ttu-id="60598-407">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="60598-407">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="60598-408">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="60598-408">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="60598-409">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="60598-409">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="60598-410">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="60598-410">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="60598-411">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="60598-411">Az.Billing</span></span>
  - <span data-ttu-id="60598-412">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-412">Az.Compute</span></span>
  - <span data-ttu-id="60598-413">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="60598-413">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="60598-414">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-414">Az.EventHub</span></span>
  - <span data-ttu-id="60598-415">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-415">Az.IotHub</span></span>
  - <span data-ttu-id="60598-416">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-416">Az.KeyVault</span></span>
  - <span data-ttu-id="60598-417">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-417">Az.Monitor</span></span>
  - <span data-ttu-id="60598-418">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-418">Az.Network</span></span>
  - <span data-ttu-id="60598-419">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-419">Az.Resources</span></span>
  - <span data-ttu-id="60598-420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-420">Az.Storage</span></span>
  - <span data-ttu-id="60598-421">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-421">Az.Websites</span></span>
* <span data-ttu-id="60598-422">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-422">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="60598-423">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="60598-423">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="60598-424">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="60598-424">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="60598-425">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-425">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-426">Az.Accounts</span></span>
* <span data-ttu-id="60598-427">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="60598-427">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-428">Az.Compute</span></span>
* <span data-ttu-id="60598-429">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="60598-429">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="60598-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="60598-430">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="60598-431">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="60598-431">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="60598-432">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="60598-432">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="60598-433">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="60598-433">[#11354]</span></span>
* <span data-ttu-id="60598-434">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="60598-434">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="60598-435">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="60598-435">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="60598-436">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="60598-436">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="60598-437">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="60598-437">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="60598-438">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="60598-438">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="60598-439">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-439">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="60598-440">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="60598-440">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="60598-441">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="60598-441">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="60598-442">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="60598-442">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-443">Az.DataFactory</span></span>
* <span data-ttu-id="60598-444">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="60598-444">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="60598-445">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="60598-445">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-446">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-446">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-447">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="60598-447">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="60598-448">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="60598-448">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="60598-449">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-449">Az.HDInsight</span></span>
* <span data-ttu-id="60598-450">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="60598-450">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-451">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-451">Az.IotHub</span></span>
* <span data-ttu-id="60598-452">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60598-452">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="60598-453">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-453">New Cmdlets are:</span></span>
    - <span data-ttu-id="60598-454">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="60598-454">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="60598-455">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="60598-455">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-456">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-456">Az.KeyVault</span></span>
* <span data-ttu-id="60598-457">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="60598-457">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-458">Az.Monitor</span></span>
* <span data-ttu-id="60598-459">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="60598-459">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-460">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-460">Az.Network</span></span>
* <span data-ttu-id="60598-461">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="60598-461">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="60598-462">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="60598-462">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="60598-463">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="60598-463">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="60598-464">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="60598-464">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="60598-465">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="60598-465">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="60598-466">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="60598-466">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="60598-467">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="60598-467">Az.PolicyInsights</span></span>
* <span data-ttu-id="60598-468">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="60598-468">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-470">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="60598-470">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="60598-471">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="60598-471">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="60598-472">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="60598-472">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="60598-473">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="60598-473">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="60598-474">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="60598-474">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="60598-475">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="60598-475">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-476">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-476">Az.Resources</span></span>
* <span data-ttu-id="60598-477">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="60598-477">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="60598-478">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="60598-478">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="60598-479">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="60598-479">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="60598-480">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="60598-480">Added example.</span></span>
* <span data-ttu-id="60598-481">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="60598-481">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="60598-482">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="60598-482">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-483">Az.Sql</span></span>
* <span data-ttu-id="60598-484">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="60598-484">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="60598-485">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-485">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="60598-486">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60598-486">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="60598-487">Az.Support</span><span class="sxs-lookup"><span data-stu-id="60598-487">Az.Support</span></span>
* <span data-ttu-id="60598-488">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="60598-488">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-489">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-489">Az.Websites</span></span>
* <span data-ttu-id="60598-490">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="60598-490">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="60598-491">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="60598-491">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="60598-492">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="60598-492">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="60598-493">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="60598-493">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="60598-494">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="60598-494">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="60598-495">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-495">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-496">Az.Accounts</span></span>
* <span data-ttu-id="60598-497">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="60598-497">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="60598-498">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="60598-498">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="60598-499">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="60598-499">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="60598-500">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-500">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-501">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="60598-501">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="60598-502">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="60598-502">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="60598-503">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="60598-503">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="60598-504">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="60598-504">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-505">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-505">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-506">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="60598-506">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-507">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-507">Az.IotHub</span></span>
* <span data-ttu-id="60598-508">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="60598-508">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="60598-509">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-509">New Cmdlets are:</span></span>
    - <span data-ttu-id="60598-510">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-510">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="60598-511">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-511">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="60598-512">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-512">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="60598-513">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-513">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="60598-514">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="60598-514">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="60598-515">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-515">New Cmdlets are:</span></span>
    - <span data-ttu-id="60598-516">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="60598-516">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="60598-517">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="60598-517">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="60598-518">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="60598-518">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="60598-519">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="60598-519">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="60598-520">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="60598-520">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="60598-521">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="60598-521">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="60598-522">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="60598-522">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="60598-523">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-523">New Cmdlets are:</span></span>
    - <span data-ttu-id="60598-524">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="60598-524">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="60598-525">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="60598-525">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="60598-526">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60598-526">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-527">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-527">Az.Monitor</span></span>
* <span data-ttu-id="60598-528">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="60598-528">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-529">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-529">Az.Network</span></span>
* <span data-ttu-id="60598-530">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="60598-530">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="60598-531">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="60598-531">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="60598-532">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="60598-532">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="60598-533">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="60598-533">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-534">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-534">Az.Resources</span></span>
* <span data-ttu-id="60598-535">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="60598-535">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="60598-536">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="60598-536">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="60598-537">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="60598-537">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="60598-538">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="60598-538">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="60598-539">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="60598-539">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="60598-540">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="60598-540">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="60598-541">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="60598-541">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="60598-542">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="60598-542">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="60598-543">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="60598-543">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="60598-544">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="60598-544">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="60598-545">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="60598-545">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="60598-546">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-546">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="60598-547">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="60598-547">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="60598-548">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="60598-548">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-549">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-549">Az.Sql</span></span>
* <span data-ttu-id="60598-550">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="60598-550">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="60598-551">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="60598-551">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="60598-552">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="60598-552">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="60598-553">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="60598-553">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="60598-554">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="60598-554">Remove an LTR backup</span></span>
    - <span data-ttu-id="60598-555">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="60598-555">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="60598-556">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="60598-556">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="60598-557">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="60598-557">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="60598-558">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-558">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-559">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-559">Az.Storage</span></span>
* <span data-ttu-id="60598-560">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-560">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="60598-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="60598-561">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="60598-562">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="60598-562">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="60598-563">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="60598-563">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="60598-564">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="60598-564">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-565">Az.Websites</span></span>
* <span data-ttu-id="60598-566">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="60598-566">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="60598-567">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="60598-567">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="60598-568">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="60598-568">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="60598-569">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="60598-569">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="60598-570">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="60598-570">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="60598-571">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-571">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="60598-572">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="60598-572">Highlights since the last major release</span></span>
* <span data-ttu-id="60598-573">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="60598-573">Updated client side telemetry.</span></span>
* <span data-ttu-id="60598-574">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="60598-574">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="60598-575">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="60598-575">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-576">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-576">Az.Accounts</span></span>
* <span data-ttu-id="60598-577">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="60598-577">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-578">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-578">Az.Automation</span></span>
* <span data-ttu-id="60598-579">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="60598-579">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-580">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-580">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-581">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="60598-581">Updated SDK to 7.0</span></span>
* <span data-ttu-id="60598-582">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="60598-582">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-583">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-583">Az.Compute</span></span>
* <span data-ttu-id="60598-584">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="60598-584">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="60598-585">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-585">Az.FrontDoor</span></span>
* <span data-ttu-id="60598-586">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="60598-586">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-587">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-587">Az.IotHub</span></span>
* <span data-ttu-id="60598-588">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="60598-588">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="60598-589">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-589">New Cmdlets are:</span></span>
    - <span data-ttu-id="60598-590">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-590">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="60598-591">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-591">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="60598-592">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-592">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="60598-593">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="60598-593">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-594">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-594">Az.KeyVault</span></span>
* <span data-ttu-id="60598-595">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="60598-595">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-596">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-596">Az.Monitor</span></span>
* <span data-ttu-id="60598-597">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="60598-597">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="60598-598">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="60598-598">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="60598-599">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="60598-599">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-600">Az.Network</span></span>
* <span data-ttu-id="60598-601">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="60598-601">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="60598-602">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="60598-602">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="60598-603">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="60598-603">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="60598-604">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="60598-604">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="60598-605">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="60598-605">No new cmdlets are added.</span></span> <span data-ttu-id="60598-606">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="60598-606">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-608">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="60598-608">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-609">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-609">Az.Resources</span></span>
* <span data-ttu-id="60598-610">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="60598-610">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="60598-611">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="60598-611">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="60598-612">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="60598-612">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="60598-613">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="60598-613">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="60598-614">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="60598-614">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="60598-615">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="60598-615">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="60598-616">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="60598-616">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="60598-617">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-617">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-618">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-618">Az.Sql</span></span>
* <span data-ttu-id="60598-619">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="60598-619">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="60598-620">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="60598-620">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="60598-621">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="60598-621">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="60598-622">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60598-622">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="60598-623">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="60598-623">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="60598-624">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="60598-624">Az.StorageSync</span></span>
* <span data-ttu-id="60598-625">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="60598-625">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="60598-626">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-626">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="60598-627">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="60598-627">Highlights since the last major release</span></span>
* <span data-ttu-id="60598-628">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="60598-628">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="60598-629">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-629">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-630">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-630">Az.Accounts</span></span>
* <span data-ttu-id="60598-631">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="60598-631">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="60598-632">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="60598-632">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="60598-633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-633">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-634">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="60598-634">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="60598-635">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="60598-635">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="60598-636">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="60598-636">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="60598-637">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="60598-637">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-638">Az.Compute</span></span>
* <span data-ttu-id="60598-639">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="60598-639">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="60598-640">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="60598-640">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="60598-641">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="60598-641">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="60598-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="60598-642">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="60598-643">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="60598-643">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-644">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-644">Az.DataFactory</span></span>
* <span data-ttu-id="60598-645">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="60598-645">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="60598-646">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="60598-646">Az.DeploymentManager</span></span>
* <span data-ttu-id="60598-647">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="60598-647">Adds LIST operations for resources</span></span>
* <span data-ttu-id="60598-648">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="60598-648">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="60598-649">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-649">Az.HDInsight</span></span>
* <span data-ttu-id="60598-650">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="60598-650">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-651">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-651">Az.KeyVault</span></span>
* <span data-ttu-id="60598-652">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="60598-652">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-653">Az.Network</span></span>
* <span data-ttu-id="60598-654">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="60598-654">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="60598-655">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="60598-655">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="60598-656">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="60598-656">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="60598-657">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="60598-657">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="60598-658">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="60598-658">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="60598-659">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="60598-659">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="60598-660">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="60598-660">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="60598-661">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="60598-661">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="60598-662">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-662">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-663">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="60598-664">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-664">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="60598-665">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="60598-665">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="60598-666">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="60598-666">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="60598-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="60598-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="60598-668">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="60598-668">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="60598-669">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="60598-669">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="60598-670">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="60598-670">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="60598-671">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="60598-671">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-673">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="60598-673">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="60598-674">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="60598-674">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-675">Az.Resources</span></span>
* <span data-ttu-id="60598-676">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="60598-676">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="60598-677">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="60598-677">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-678">Az.Sql</span></span>
<span data-ttu-id="60598-679">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="60598-679">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-680">Az.Storage</span></span>
* <span data-ttu-id="60598-681">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60598-681">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="60598-682">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-682">New-AzStorageAccount</span></span>
* <span data-ttu-id="60598-683">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="60598-683">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="60598-684">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="60598-684">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-685">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-685">Az.Websites</span></span>
* <span data-ttu-id="60598-686">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="60598-686">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="60598-687">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="60598-687">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="60598-688">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="60598-688">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-689">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-689">Az.Accounts</span></span>
* <span data-ttu-id="60598-690">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="60598-690">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="60598-691">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-691">Az.Cdn</span></span>
* <span data-ttu-id="60598-692">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60598-692">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-693">Az.Compute</span></span>
* <span data-ttu-id="60598-694">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="60598-694">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="60598-695">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="60598-695">Az.ContainerInstance</span></span>
* <span data-ttu-id="60598-696">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="60598-696">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="60598-697">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="60598-697">Az.DataBoxEdge</span></span>
* <span data-ttu-id="60598-698">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="60598-698">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="60598-699">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="60598-699">Get the Edge Storage Container</span></span>
* <span data-ttu-id="60598-700">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="60598-700">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="60598-701">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="60598-701">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="60598-702">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="60598-702">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="60598-703">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="60598-703">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="60598-704">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="60598-704">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="60598-705">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="60598-705">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="60598-706">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-706">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="60598-707">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="60598-707">Get the Edge Storage Account</span></span>
* <span data-ttu-id="60598-708">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-708">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="60598-709">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="60598-709">Create new Edge Storage Account</span></span>
* <span data-ttu-id="60598-710">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="60598-710">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="60598-711">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="60598-711">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="60598-712">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="60598-712">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="60598-713">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="60598-713">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="60598-714">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="60598-714">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="60598-715">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="60598-715">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-716">Az.DataFactory</span></span>
* <span data-ttu-id="60598-717">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="60598-717">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="60598-718">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="60598-718">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="60598-719">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="60598-719">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="60598-720">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="60598-720">Az.DevTestLabs</span></span>
* <span data-ttu-id="60598-721">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="60598-721">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="60598-722">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-722">Az.EventHub</span></span>
* <span data-ttu-id="60598-723">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="60598-723">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="60598-724">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-724">Az.HDInsight</span></span>
* <span data-ttu-id="60598-725">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="60598-725">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="60598-726">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="60598-726">Az.MachineLearning</span></span>
* <span data-ttu-id="60598-727">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="60598-727">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="60598-728">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="60598-728">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="60598-729">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="60598-729">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="60598-730">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="60598-730">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="60598-731">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="60598-731">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="60598-732">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="60598-732">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="60598-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="60598-733">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="60598-734">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="60598-734">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-735">Az.Network</span></span>
* <span data-ttu-id="60598-736">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="60598-736">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-737">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-737">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-738">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-738">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="60598-739">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-739">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="60598-740">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-740">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="60598-741">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-741">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-742">Az.Resources</span></span>
* <span data-ttu-id="60598-743">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="60598-743">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-744">Az.Sql</span></span>
* <span data-ttu-id="60598-745">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="60598-745">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="60598-746">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="60598-746">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="60598-747">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60598-747">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="60598-748">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="60598-748">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-749">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-749">Az.Storage</span></span>
* <span data-ttu-id="60598-750">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="60598-750">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="60598-751">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-751">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="60598-752">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="60598-752">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="60598-753">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-753">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="60598-754">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-754">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="60598-755">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-755">General</span></span>
* <span data-ttu-id="60598-756">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="60598-756">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-757">Az.Accounts</span></span>
* <span data-ttu-id="60598-758">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="60598-758">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="60598-759">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="60598-759">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="60598-760">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="60598-760">Az.Batch</span></span>
* <span data-ttu-id="60598-761">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="60598-761">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-762">Az.DataFactory</span></span>
* <span data-ttu-id="60598-763">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="60598-763">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="60598-764">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-764">Az.FrontDoor</span></span>
* <span data-ttu-id="60598-765">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="60598-765">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="60598-766">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="60598-766">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="60598-767">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="60598-767">Az.HealthcareApis</span></span>
* <span data-ttu-id="60598-768">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="60598-768">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-769">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-769">Az.KeyVault</span></span>
* <span data-ttu-id="60598-770">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="60598-770">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="60598-771">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="60598-771">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="60598-772">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="60598-772">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-773">Az.Monitor</span></span>
* <span data-ttu-id="60598-774">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="60598-774">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="60598-775">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="60598-775">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="60598-776">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="60598-776">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-777">Az.Network</span></span>
* <span data-ttu-id="60598-778">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="60598-778">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-779">Az.Resources</span></span>
* <span data-ttu-id="60598-780">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="60598-780">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="60598-781">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="60598-781">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-782">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-782">Az.Sql</span></span>
* <span data-ttu-id="60598-783">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="60598-783">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-784">Az.Storage</span></span>
* <span data-ttu-id="60598-785">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="60598-785">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="60598-786">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="60598-786">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="60598-787">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="60598-787">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="60598-788">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="60598-788">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="60598-789">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="60598-789">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="60598-790">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="60598-790">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="60598-791">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="60598-791">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="60598-792">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60598-792">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="60598-793">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60598-793">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="60598-794">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="60598-794">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="60598-795">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="60598-795">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="60598-796">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="60598-796">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="60598-797">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="60598-797">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="60598-798">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-798">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="60598-799">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="60598-799">Highlights since the last major release</span></span>
* <span data-ttu-id="60598-800">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="60598-800">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="60598-801">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="60598-801">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-802">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-802">Az.Compute</span></span>
* <span data-ttu-id="60598-803">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="60598-803">VM Reapply feature</span></span>
    - <span data-ttu-id="60598-804">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="60598-804">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="60598-805">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="60598-805">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="60598-806">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-806">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="60598-807">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="60598-807">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="60598-808">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-808">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="60598-809">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="60598-809">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="60598-810">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="60598-810">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="60598-811">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="60598-811">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="60598-812">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="60598-812">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="60598-813">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-813">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="60598-814">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="60598-814">Az.DataBoxEdge</span></span>
* <span data-ttu-id="60598-815">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-815">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="60598-816">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="60598-816">Get the Order</span></span>
* <span data-ttu-id="60598-817">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-817">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="60598-818">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="60598-818">Create new Order</span></span>
* <span data-ttu-id="60598-819">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-819">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="60598-820">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="60598-820">Remove the Order</span></span>
* <span data-ttu-id="60598-821">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="60598-821">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="60598-822">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="60598-822">Now creates Local Share</span></span>
* <span data-ttu-id="60598-823">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-823">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="60598-824">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="60598-824">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="60598-825">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-825">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="60598-826">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="60598-826">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="60598-827">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-827">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="60598-828">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="60598-828">Gets the information about Triggers</span></span>
* <span data-ttu-id="60598-829">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-829">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="60598-830">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="60598-830">Create new Triggers</span></span>
* <span data-ttu-id="60598-831">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-831">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="60598-832">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="60598-832">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-833">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-833">Az.DataFactory</span></span>
* <span data-ttu-id="60598-834">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="60598-834">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="60598-835">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="60598-835">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-836">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-836">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-837">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="60598-837">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="60598-838">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-838">Az.EventHub</span></span>
* <span data-ttu-id="60598-839">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="60598-839">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="60598-840">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-840">Az.FrontDoor</span></span>
* <span data-ttu-id="60598-841">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="60598-841">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="60598-842">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="60598-842">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="60598-843">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="60598-843">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="60598-844">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="60598-844">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-845">Az.Network</span></span>
* <span data-ttu-id="60598-846">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="60598-846">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="60598-847">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="60598-847">Az.PrivateDns</span></span>
* <span data-ttu-id="60598-848">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="60598-848">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-849">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-849">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-850">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="60598-850">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="60598-851">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="60598-851">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="60598-852">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="60598-852">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="60598-853">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="60598-853">Az.RedisCache</span></span>
* <span data-ttu-id="60598-854">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="60598-854">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="60598-855">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="60598-855">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="60598-856">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="60598-856">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-857">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-857">Az.Resources</span></span>
- <span data-ttu-id="60598-858">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="60598-858">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="60598-859">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="60598-859">Updated create policy definition help example</span></span>
- <span data-ttu-id="60598-860">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="60598-860">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="60598-861">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="60598-861">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="60598-862">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="60598-862">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-863">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-863">Az.Sql</span></span>
* <span data-ttu-id="60598-864">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="60598-864">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="60598-865">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="60598-865">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="60598-866">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-866">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="60598-867">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-867">General</span></span>
* <span data-ttu-id="60598-868">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="60598-868">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-869">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-869">Az.Accounts</span></span>
* <span data-ttu-id="60598-870">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="60598-870">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="60598-871">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="60598-871">Az.Advisor</span></span>
* <span data-ttu-id="60598-872">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60598-872">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="60598-873">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="60598-873">Az.Batch</span></span>
* <span data-ttu-id="60598-874">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="60598-874">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="60598-875">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="60598-875">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="60598-876">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="60598-876">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="60598-877">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="60598-877">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="60598-878">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="60598-878">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="60598-879">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="60598-879">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="60598-880">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="60598-880">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="60598-881">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="60598-881">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="60598-882">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="60598-882">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="60598-883">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="60598-883">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="60598-884">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="60598-884">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="60598-885">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="60598-885">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="60598-886">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="60598-886">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="60598-887">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="60598-887">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="60598-888">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="60598-888">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="60598-889">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="60598-889">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="60598-890">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="60598-890">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="60598-891">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="60598-891">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="60598-892">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="60598-892">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="60598-893">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="60598-893">This operation is no longer supported.</span></span>
* <span data-ttu-id="60598-894">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="60598-894">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="60598-895">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="60598-895">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="60598-896">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="60598-896">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="60598-897">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="60598-897">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="60598-898">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="60598-898">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="60598-899">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="60598-899">New non-verified images are also now returned.</span></span> <span data-ttu-id="60598-900">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="60598-900">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="60598-901">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="60598-901">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="60598-902">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="60598-902">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="60598-903">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="60598-903">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="60598-904">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="60598-904">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="60598-905">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="60598-905">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="60598-906">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="60598-906">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="60598-907">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="60598-907">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="60598-908">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="60598-908">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="60598-909">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="60598-909">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="60598-910">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-910">Az.Cdn</span></span>
* <span data-ttu-id="60598-911">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="60598-911">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="60598-912">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="60598-912">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-913">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-913">Az.Compute</span></span>
* <span data-ttu-id="60598-914">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="60598-914">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="60598-915">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="60598-915">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="60598-916">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="60598-916">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="60598-917">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="60598-917">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="60598-918">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="60598-918">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="60598-919">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="60598-919">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="60598-920">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-920">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="60598-921">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="60598-921">Breaking changes</span></span>
    - <span data-ttu-id="60598-922">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="60598-922">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="60598-923">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="60598-923">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-924">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-924">Az.DataFactory</span></span>
* <span data-ttu-id="60598-925">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="60598-925">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-927">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="60598-927">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="60598-928">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="60598-928">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="60598-929">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="60598-929">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="60598-930">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="60598-930">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="60598-931">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="60598-931">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="60598-932">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="60598-932">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="60598-933">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-933">Az.FrontDoor</span></span>
* <span data-ttu-id="60598-934">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="60598-934">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="60598-935">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-935">Az.HDInsight</span></span>
* <span data-ttu-id="60598-936">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="60598-936">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="60598-937">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="60598-937">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="60598-938">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="60598-938">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="60598-939">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="60598-939">Removed five cmdlets:</span></span>
    - <span data-ttu-id="60598-940">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="60598-940">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="60598-941">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="60598-941">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="60598-942">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="60598-942">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="60598-943">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="60598-943">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="60598-944">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="60598-944">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="60598-945">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-945">Added three cmdlets:</span></span>
    - <span data-ttu-id="60598-946">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="60598-946">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="60598-947">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="60598-947">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="60598-948">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="60598-948">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="60598-949">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="60598-949">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="60598-950">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="60598-950">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="60598-951">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="60598-951">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="60598-952">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="60598-952">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="60598-953">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="60598-953">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="60598-954">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="60598-954">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="60598-955">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="60598-955">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="60598-956">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="60598-956">Added some scenario test cases.</span></span>
* <span data-ttu-id="60598-957">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="60598-957">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-958">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-958">Az.IotHub</span></span>
* <span data-ttu-id="60598-959">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="60598-959">Breaking changes:</span></span>
    - <span data-ttu-id="60598-960">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="60598-960">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="60598-961">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="60598-961">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="60598-962">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="60598-962">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="60598-963">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="60598-963">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="60598-964">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="60598-964">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="60598-965">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="60598-965">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="60598-966">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="60598-966">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="60598-967">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="60598-967">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="60598-968">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="60598-968">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="60598-969">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="60598-969">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="60598-970">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="60598-970">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="60598-971">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="60598-971">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-972">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-972">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-973">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-973">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="60598-974">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-974">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="60598-975">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-975">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="60598-976">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-976">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="60598-977">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-977">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="60598-978">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-978">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="60598-979">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-979">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="60598-980">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-980">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="60598-981">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="60598-981">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-982">Az.Resources</span></span>
* <span data-ttu-id="60598-983">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="60598-983">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-984">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-984">Az.Network</span></span>
* <span data-ttu-id="60598-985">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="60598-985">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="60598-986">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60598-986">Updated cmdlet:</span></span>
        - <span data-ttu-id="60598-987">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-987">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-988">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-988">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-989">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-989">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-990">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-990">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-991">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-991">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="60598-992">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="60598-992">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="60598-993">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60598-993">New cmdlet:</span></span>
        - <span data-ttu-id="60598-994">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="60598-994">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="60598-995">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="60598-995">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="60598-996">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="60598-996">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="60598-997">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-997">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="60598-998">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="60598-998">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="60598-999">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="60598-999">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="60598-1000">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1000">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="60598-1001">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="60598-1001">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="60598-1002">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-1002">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-1003">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="60598-1003">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="60598-1004">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60598-1004">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="60598-1005">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60598-1005">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="60598-1006">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="60598-1006">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="60598-1007">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="60598-1007">Set-AzVirtualHub</span></span>
* <span data-ttu-id="60598-1008">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="60598-1008">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="60598-1009">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="60598-1009">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="60598-1010">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1010">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="60598-1011">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1011">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="60598-1012">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1012">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="60598-1013">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1013">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="60598-1014">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1014">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="60598-1015">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-1015">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-1016">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1016">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="60598-1017">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="60598-1017">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="60598-1018">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1018">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="60598-1019">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1019">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="60598-1020">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1020">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="60598-1021">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1021">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="60598-1022">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-1022">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="60598-1023">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="60598-1023">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="60598-1024">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-1024">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-1025">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="60598-1025">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="60598-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="60598-1026">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="60598-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="60598-1027">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="60598-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="60598-1028">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="60598-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="60598-1029">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="60598-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-1030">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="60598-1031">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="60598-1031">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="60598-1032">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-1032">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="60598-1033">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="60598-1033">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="60598-1034">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="60598-1034">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="60598-1035">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="60598-1035">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="60598-1036">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="60598-1036">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="60598-1037">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-1037">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="60598-1038">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-1038">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="60598-1039">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="60598-1039">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="60598-1040">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1040">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="60598-1041">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1041">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="60598-1042">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-1042">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-1043">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1043">New-AzIpGroup</span></span>
        - <span data-ttu-id="60598-1044">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1044">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="60598-1045">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1045">Get-AzIpGroup</span></span>
        - <span data-ttu-id="60598-1046">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1046">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-1047">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-1047">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-1048">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="60598-1048">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1049">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1049">Az.Sql</span></span>
* <span data-ttu-id="60598-1050">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="60598-1050">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="60598-1051">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="60598-1051">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="60598-1052">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="60598-1052">Removed deprecated aliases:</span></span>
* <span data-ttu-id="60598-1053">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="60598-1053">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="60598-1054">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="60598-1054">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="60598-1055">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1055">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="60598-1056">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="60598-1056">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="60598-1057">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="60598-1057">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="60598-1058">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60598-1058">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1059">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1059">Az.Storage</span></span>
* <span data-ttu-id="60598-1060">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60598-1060">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="60598-1061">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1061">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="60598-1062">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1062">Set-AzStorageAccount</span></span>
* <span data-ttu-id="60598-1063">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="60598-1063">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="60598-1064">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="60598-1064">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="60598-1065">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="60598-1065">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="60598-1066">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1066">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="60598-1067">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-1067">General</span></span>
* <span data-ttu-id="60598-1068">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="60598-1068">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-1069">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1069">Az.Accounts</span></span>
* <span data-ttu-id="60598-1070">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="60598-1070">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="60598-1071">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-1071">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-1072">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="60598-1072">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="60598-1073">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="60598-1073">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-1074">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1074">Az.Automation</span></span>
* <span data-ttu-id="60598-1075">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="60598-1075">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="60598-1076">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="60598-1076">Az.Batch</span></span>
* <span data-ttu-id="60598-1077">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="60598-1077">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1078">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1078">Az.Compute</span></span>
* <span data-ttu-id="60598-1079">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-1079">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="60598-1080">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="60598-1080">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="60598-1081">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="60598-1081">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="60598-1082">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="60598-1082">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-1083">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-1083">Az.DataFactory</span></span>
* <span data-ttu-id="60598-1084">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="60598-1084">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="60598-1085">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="60598-1085">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="60598-1086">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="60598-1086">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-1088">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="60598-1088">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="60598-1089">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="60598-1089">Az.HealthcareApis</span></span>
* <span data-ttu-id="60598-1090">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="60598-1090">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="60598-1091">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="60598-1091">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="60598-1092">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="60598-1092">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="60598-1093">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="60598-1093">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-1094">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-1094">Az.IotHub</span></span>
* <span data-ttu-id="60598-1095">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="60598-1095">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="60598-1096">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="60598-1096">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-1097">Az.Monitor</span></span>
* <span data-ttu-id="60598-1098">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="60598-1098">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="60598-1099">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="60598-1099">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="60598-1100">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="60598-1100">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="60598-1101">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="60598-1101">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1102">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1102">Az.Network</span></span>
* <span data-ttu-id="60598-1103">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="60598-1103">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="60598-1104">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="60598-1104">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="60598-1105">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-1105">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-1106">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1106">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="60598-1107">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1107">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="60598-1108">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="60598-1108">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="60598-1109">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="60598-1109">Updated cmdlets:</span></span>
        - <span data-ttu-id="60598-1110">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1110">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="60598-1111">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1111">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="60598-1112">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1112">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="60598-1113">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="60598-1113">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="60598-1114">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="60598-1114">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="60598-1115">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="60598-1115">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="60598-1116">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="60598-1116">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="60598-1117">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="60598-1117">Az.RedisCache</span></span>
* <span data-ttu-id="60598-1118">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="60598-1118">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1119">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1119">Az.Sql</span></span>
* <span data-ttu-id="60598-1120">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="60598-1120">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1121">Az.Storage</span></span>
* <span data-ttu-id="60598-1122">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="60598-1122">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="60598-1123">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="60598-1123">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="60598-1124">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="60598-1124">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="60598-1125">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="60598-1125">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="60598-1126">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1126">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="60598-1127">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="60598-1127">Az.StorageSync</span></span>
* <span data-ttu-id="60598-1128">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="60598-1128">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1129">Az.Websites</span></span>
* <span data-ttu-id="60598-1130">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="60598-1130">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="60598-1131">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1131">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="60598-1132">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-1132">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-1133">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="60598-1133">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="60598-1134">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="60598-1134">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="60598-1135">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="60598-1135">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-1136">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1136">Az.Automation</span></span>
* <span data-ttu-id="60598-1137">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="60598-1137">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="60598-1138">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="60598-1138">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="60598-1139">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="60598-1139">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1140">Az.Compute</span></span>
* <span data-ttu-id="60598-1141">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1141">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="60598-1142">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1142">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="60598-1143">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="60598-1143">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="60598-1144">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="60598-1144">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="60598-1145">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="60598-1145">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="60598-1146">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="60598-1146">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="60598-1147">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="60598-1147">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="60598-1148">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="60598-1148">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="60598-1149">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="60598-1149">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-1150">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-1150">Az.DataFactory</span></span>
* <span data-ttu-id="60598-1151">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="60598-1151">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="60598-1152">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="60598-1152">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="60598-1153">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-1153">Az.HDInsight</span></span>
* <span data-ttu-id="60598-1154">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="60598-1154">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-1155">Az.IotHub</span></span>
* <span data-ttu-id="60598-1156">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="60598-1156">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="60598-1157">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="60598-1157">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="60598-1158">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="60598-1158">New cmdlets are:</span></span>
    - <span data-ttu-id="60598-1159">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="60598-1159">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="60598-1160">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="60598-1160">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="60598-1161">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="60598-1161">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="60598-1162">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="60598-1162">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-1163">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-1163">Az.Monitor</span></span>
* <span data-ttu-id="60598-1164">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="60598-1164">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="60598-1165">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="60598-1165">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="60598-1166">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="60598-1166">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="60598-1167">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="60598-1167">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="60598-1168">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="60598-1168">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="60598-1169">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="60598-1169">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="60598-1170">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="60598-1170">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="60598-1171">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="60598-1171">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="60598-1172">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="60598-1172">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="60598-1173">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="60598-1173">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="60598-1174">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="60598-1174">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="60598-1175">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="60598-1175">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="60598-1176">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="60598-1176">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="60598-1177">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="60598-1177">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="60598-1178">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="60598-1178">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="60598-1179">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="60598-1179">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="60598-1180">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="60598-1180">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="60598-1181">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-1181">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="60598-1182">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="60598-1182">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="60598-1183">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-1183">Overall improved help files</span></span>
* <span data-ttu-id="60598-1184">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="60598-1184">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1185">Az.Network</span></span>
* <span data-ttu-id="60598-1186">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="60598-1186">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="60598-1187">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="60598-1187">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="60598-1188">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="60598-1188">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="60598-1189">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="60598-1189">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="60598-1190">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="60598-1190">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="60598-1191">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="60598-1191">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="60598-1192">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="60598-1192">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="60598-1193">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="60598-1193">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="60598-1194">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-1194">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="60598-1195">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="60598-1195">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="60598-1196">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1196">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="60598-1197">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="60598-1197">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="60598-1198">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="60598-1198">New cmdlets</span></span>
        - <span data-ttu-id="60598-1199">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="60598-1199">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="60598-1200">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1200">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="60598-1201">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60598-1201">Updated cmdlet:</span></span>
        - <span data-ttu-id="60598-1202">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="60598-1202">New-VpnSite</span></span>
        - <span data-ttu-id="60598-1203">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="60598-1203">Update-VpnSite</span></span>
        - <span data-ttu-id="60598-1204">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1204">New-VpnConnection</span></span>
        - <span data-ttu-id="60598-1205">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1205">Update-VpnConnection</span></span>
* <span data-ttu-id="60598-1206">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="60598-1206">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1207">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1207">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1208">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="60598-1208">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="60598-1209">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="60598-1209">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1210">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1210">Az.Resources</span></span>
* <span data-ttu-id="60598-1211">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="60598-1211">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-1212">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-1212">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-1213">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="60598-1213">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="60598-1214">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="60598-1214">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="60598-1215">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="60598-1215">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="60598-1216">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="60598-1216">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="60598-1217">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="60598-1217">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="60598-1218">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="60598-1218">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="60598-1219">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="60598-1219">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="60598-1220">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="60598-1220">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="60598-1221">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="60598-1221">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="60598-1222">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="60598-1222">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="60598-1223">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="60598-1223">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="60598-1224">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="60598-1224">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="60598-1225">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="60598-1225">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="60598-1226">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="60598-1226">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="60598-1227">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="60598-1227">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="60598-1228">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="60598-1228">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="60598-1229">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="60598-1229">Az.SignalR</span></span>
* <span data-ttu-id="60598-1230">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="60598-1230">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1231">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1231">Az.Sql</span></span>
* <span data-ttu-id="60598-1232">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="60598-1232">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="60598-1233">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="60598-1233">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="60598-1234">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1234">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="60598-1235">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="60598-1235">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="60598-1236">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="60598-1236">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1237">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1237">Az.Storage</span></span>
* <span data-ttu-id="60598-1238">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="60598-1238">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="60598-1239">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="60598-1239">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="60598-1240">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="60598-1240">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="60598-1241">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="60598-1241">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="60598-1242">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="60598-1242">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="60598-1243">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="60598-1243">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="60598-1244">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="60598-1244">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="60598-1245">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60598-1245">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="60598-1246">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60598-1246">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="60598-1247">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60598-1247">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="60598-1248">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="60598-1248">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1249">Az.Websites</span></span>
* <span data-ttu-id="60598-1250">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="60598-1250">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="60598-1251">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="60598-1251">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="60598-1252">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="60598-1252">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="60598-1253">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1253">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="60598-1254">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-1254">General</span></span>
* <span data-ttu-id="60598-1255">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="60598-1255">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-1256">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1256">Az.Accounts</span></span>
* <span data-ttu-id="60598-1257">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="60598-1257">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="60598-1258">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="60598-1258">Az.Aks</span></span>
* <span data-ttu-id="60598-1259">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="60598-1259">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="60598-1260">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="60598-1260">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="60598-1261">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-1261">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-1262">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="60598-1262">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="60598-1263">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="60598-1263">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="60598-1264">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="60598-1264">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="60598-1265">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="60598-1265">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="60598-1266">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="60598-1266">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="60598-1267">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="60598-1267">Az.Batch</span></span>
* <span data-ttu-id="60598-1268">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="60598-1268">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="60598-1269">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-1269">Az.Cdn</span></span>
* <span data-ttu-id="60598-1270">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="60598-1270">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1271">Az.Compute</span></span>
* <span data-ttu-id="60598-1272">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1272">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="60598-1273">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-1273">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="60598-1274">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="60598-1274">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="60598-1275">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1275">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="60598-1276">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="60598-1276">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="60598-1277">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="60598-1277">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="60598-1278">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="60598-1278">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="60598-1279">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="60598-1279">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-1280">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-1280">Az.DataFactory</span></span>
* <span data-ttu-id="60598-1281">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="60598-1281">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="60598-1282">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="60598-1282">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="60598-1283">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="60598-1283">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="60598-1284">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="60598-1284">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-1285">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-1285">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-1286">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="60598-1286">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="60598-1287">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-1287">Az.EventHub</span></span>
* <span data-ttu-id="60598-1288">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-1288">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="60598-1289">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="60598-1289">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="60598-1290">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="60598-1290">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="60598-1291">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="60598-1291">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="60598-1292">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="60598-1292">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="60598-1293">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="60598-1293">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-1294">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-1294">Az.Monitor</span></span>
* <span data-ttu-id="60598-1295">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-1295">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1296">Az.Network</span></span>
* <span data-ttu-id="60598-1297">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1297">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="60598-1298">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="60598-1298">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="60598-1299">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="60598-1299">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="60598-1300">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="60598-1300">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="60598-1301">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="60598-1301">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="60598-1302">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="60598-1302">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="60598-1303">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="60598-1303">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="60598-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="60598-1305">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="60598-1305">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="60598-1306">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="60598-1306">Added example</span></span>
    - <span data-ttu-id="60598-1307">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="60598-1307">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="60598-1308">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="60598-1308">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="60598-1309">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="60598-1309">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1310">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1310">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1311">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1311">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1312">Az.Resources</span></span>
* <span data-ttu-id="60598-1313">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="60598-1313">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="60598-1314">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="60598-1314">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="60598-1315">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="60598-1315">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="60598-1316">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-1316">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="60598-1317">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="60598-1317">Az.ServiceBus</span></span>
* <span data-ttu-id="60598-1318">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-1318">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="60598-1319">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="60598-1319">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="60598-1320">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="60598-1320">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-1321">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-1321">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-1322">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="60598-1322">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="60598-1323">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="60598-1323">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="60598-1324">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="60598-1324">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="60598-1325">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="60598-1325">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="60598-1326">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="60598-1326">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="60598-1327">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="60598-1327">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1328">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1328">Az.Sql</span></span>
* <span data-ttu-id="60598-1329">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="60598-1329">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1330">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1330">Az.Storage</span></span>
* <span data-ttu-id="60598-1331">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="60598-1331">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="60598-1332">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="60598-1332">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="60598-1333">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="60598-1333">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="60598-1334">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="60598-1334">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="60598-1335">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="60598-1335">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="60598-1336">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="60598-1336">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1337">Az.Websites</span></span>
* <span data-ttu-id="60598-1338">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60598-1338">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="60598-1339">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1339">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1340">Az.Accounts</span></span>
* <span data-ttu-id="60598-1341">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="60598-1341">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="60598-1342">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1342">Az.ApplicationInsights</span></span>
* <span data-ttu-id="60598-1343">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="60598-1343">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1344">Az.Automation</span></span>
* <span data-ttu-id="60598-1345">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="60598-1345">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-1346">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-1346">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-1347">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="60598-1347">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1348">Az.Compute</span></span>
* <span data-ttu-id="60598-1349">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="60598-1349">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="60598-1350">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="60598-1350">Az.ContainerRegistry</span></span>
* <span data-ttu-id="60598-1351">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="60598-1351">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="60598-1352">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="60598-1352">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-1353">Az.DataFactory</span></span>
* <span data-ttu-id="60598-1354">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="60598-1354">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="60598-1355">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="60598-1355">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="60598-1356">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-1356">Az.EventHub</span></span>
* <span data-ttu-id="60598-1357">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="60598-1357">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="60598-1358">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="60598-1358">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-1359">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-1359">Az.KeyVault</span></span>
* <span data-ttu-id="60598-1360">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="60598-1360">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="60598-1361">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="60598-1361">Az.LogicApp</span></span>
* <span data-ttu-id="60598-1362">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="60598-1362">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="60598-1363">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="60598-1363">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="60598-1364">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="60598-1364">Az.ManagedServices</span></span>
* <span data-ttu-id="60598-1365">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="60598-1365">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1366">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1366">Az.Network</span></span>
* <span data-ttu-id="60598-1367">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="60598-1367">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="60598-1368">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="60598-1368">New cmdlets</span></span>
        - <span data-ttu-id="60598-1369">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60598-1369">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="60598-1370">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="60598-1370">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="60598-1371">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1371">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-1372">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1372">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-1373">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1373">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-1374">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1374">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="60598-1375">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="60598-1375">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="60598-1376">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="60598-1376">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="60598-1377">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="60598-1377">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="60598-1378">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="60598-1378">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="60598-1379">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="60598-1379">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="60598-1380">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="60598-1380">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="60598-1381">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="60598-1381">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="60598-1382">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="60598-1382">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="60598-1383">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="60598-1383">Updated cmdlets</span></span>
        - <span data-ttu-id="60598-1384">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1384">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="60598-1385">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1385">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="60598-1386">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1386">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="60598-1387">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1387">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="60598-1388">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-1388">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="60598-1389">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60598-1389">Updated cmdlet:</span></span>
        - <span data-ttu-id="60598-1390">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1390">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="60598-1391">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1391">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="60598-1392">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1392">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="60598-1393">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="60598-1393">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="60598-1394">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="60598-1394">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="60598-1395">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="60598-1395">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="60598-1396">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1396">Az.OperationalInsights</span></span>
* <span data-ttu-id="60598-1397">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="60598-1397">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="60598-1398">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="60598-1398">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1399">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1400">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1400">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="60598-1401">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1401">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="60598-1402">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1402">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="60598-1403">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1403">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="60598-1404">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1404">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="60598-1405">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1405">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="60598-1406">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1406">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="60598-1407">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1407">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="60598-1408">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1408">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="60598-1409">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="60598-1409">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1410">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1410">Az.Resources</span></span>
- <span data-ttu-id="60598-1411">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-1411">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="60598-1412">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="60598-1412">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="60598-1413">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="60598-1413">Az.ServiceBus</span></span>
* <span data-ttu-id="60598-1414">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="60598-1414">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="60598-1415">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="60598-1415">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1416">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1416">Az.Sql</span></span>
* <span data-ttu-id="60598-1417">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="60598-1417">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="60598-1418">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="60598-1418">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="60598-1419">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="60598-1419">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1420">Az.Storage</span></span>
* <span data-ttu-id="60598-1421">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="60598-1421">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="60598-1422">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="60598-1422">Az.StorageSync</span></span>
* <span data-ttu-id="60598-1423">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="60598-1423">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="60598-1424">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="60598-1424">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1425">Az.Websites</span></span>
* <span data-ttu-id="60598-1426">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60598-1426">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="60598-1427">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="60598-1427">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="60598-1428">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="60598-1428">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="60598-1429">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1429">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-1430">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1430">Az.Accounts</span></span>
* <span data-ttu-id="60598-1431">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="60598-1431">Add support for profile cmdlets</span></span>
* <span data-ttu-id="60598-1432">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="60598-1432">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="60598-1433">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="60598-1433">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="60598-1434">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="60598-1434">Az.Advisor</span></span>
* <span data-ttu-id="60598-1435">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="60598-1435">GA release of Az.Advisor</span></span>
* <span data-ttu-id="60598-1436">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="60598-1436">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="60598-1437">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-1437">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-1438">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="60598-1438">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="60598-1439">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="60598-1439">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="60598-1440">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="60598-1440">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="60598-1441">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="60598-1441">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="60598-1442">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="60598-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="60598-1443">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="60598-1443">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="60598-1444">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="60598-1444">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-1445">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1445">Az.Automation</span></span>
* <span data-ttu-id="60598-1446">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="60598-1446">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1447">Az.Compute</span></span>
* <span data-ttu-id="60598-1448">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1448">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-1449">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-1449">Az.DataFactory</span></span>
* <span data-ttu-id="60598-1450">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="60598-1450">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="60598-1451">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="60598-1451">Az.EventGrid</span></span>
* <span data-ttu-id="60598-1452">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="60598-1452">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-1453">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-1453">Az.IotHub</span></span>
* <span data-ttu-id="60598-1454">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="60598-1454">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1455">Az.Network</span></span>
* <span data-ttu-id="60598-1456">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="60598-1456">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="60598-1457">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="60598-1457">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="60598-1458">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1458">Az.PolicyInsights</span></span>
* <span data-ttu-id="60598-1459">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="60598-1459">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="60598-1460">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="60598-1460">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="60598-1461">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1461">Az.OperationalInsights</span></span>
* <span data-ttu-id="60598-1462">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="60598-1462">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1464">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="60598-1464">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1465">Az.Resources</span></span>
    - <span data-ttu-id="60598-1466">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="60598-1466">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="60598-1467">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="60598-1467">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="60598-1468">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="60598-1468">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="60598-1469">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="60598-1469">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="60598-1470">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="60598-1470">Az.ServiceBus</span></span>
* <span data-ttu-id="60598-1471">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="60598-1471">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1472">Az.Sql</span></span>
* <span data-ttu-id="60598-1473">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="60598-1473">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="60598-1474">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="60598-1474">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="60598-1475">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="60598-1475">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="60598-1476">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="60598-1476">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="60598-1477">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="60598-1477">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="60598-1478">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="60598-1478">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="60598-1479">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="60598-1479">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="60598-1480">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="60598-1480">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="60598-1481">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="60598-1481">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1482">Az.Storage</span></span>
* <span data-ttu-id="60598-1483">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60598-1483">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="60598-1484">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="60598-1484">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="60598-1485">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="60598-1485">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="60598-1486">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="60598-1486">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="60598-1487">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1487">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="60598-1488">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1488">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="60598-1489">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1489">Set-AzStorageAccount</span></span>
* <span data-ttu-id="60598-1490">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="60598-1490">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="60598-1491">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="60598-1491">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="60598-1492">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="60598-1492">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="60598-1493">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="60598-1493">Az.StorageSync</span></span>
* <span data-ttu-id="60598-1494">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="60598-1494">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="60598-1495">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1495">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1496">Az.Accounts</span></span>
* <span data-ttu-id="60598-1497">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="60598-1497">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="60598-1498">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="60598-1498">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="60598-1499">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="60598-1499">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="60598-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="60598-1500">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="60598-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="60598-1501">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1502">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1502">Az.Compute</span></span>
* <span data-ttu-id="60598-1503">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="60598-1503">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="60598-1504">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="60598-1504">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="60598-1505">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="60598-1505">Az.Dns</span></span>
* <span data-ttu-id="60598-1506">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="60598-1506">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="60598-1507">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="60598-1507">Az.EventGrid</span></span>
* <span data-ttu-id="60598-1508">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="60598-1508">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="60598-1509">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="60598-1509">New cmdlets:</span></span>
    - <span data-ttu-id="60598-1510">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="60598-1510">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="60598-1511">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-1511">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="60598-1512">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="60598-1512">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="60598-1513">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-1513">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="60598-1514">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="60598-1514">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="60598-1515">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-1515">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="60598-1516">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="60598-1516">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="60598-1517">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-1517">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="60598-1518">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="60598-1518">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="60598-1519">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="60598-1519">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="60598-1520">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="60598-1520">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="60598-1521">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-1521">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="60598-1522">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="60598-1522">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="60598-1523">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="60598-1523">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="60598-1524">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="60598-1524">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="60598-1525">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="60598-1525">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="60598-1526">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="60598-1526">Updated cmdlets:</span></span>
    - <span data-ttu-id="60598-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="60598-1527">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="60598-1528">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="60598-1528">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="60598-1529">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="60598-1529">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="60598-1530">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="60598-1530">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="60598-1531">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="60598-1531">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="60598-1532">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="60598-1532">Event subscription expiration date,</span></span>
            - <span data-ttu-id="60598-1533">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="60598-1533">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="60598-1534">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="60598-1534">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="60598-1535">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="60598-1535">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="60598-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="60598-1536">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="60598-1537">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="60598-1537">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="60598-1538">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="60598-1538">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="60598-1539">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="60598-1539">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="60598-1540">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="60598-1540">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="60598-1541">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-1541">Az.FrontDoor</span></span>
* <span data-ttu-id="60598-1542">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="60598-1542">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="60598-1543">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="60598-1543">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="60598-1544">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="60598-1544">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="60598-1545">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="60598-1545">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1546">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1546">Az.Network</span></span>
* <span data-ttu-id="60598-1547">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="60598-1547">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="60598-1548">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="60598-1548">New cmdlets</span></span>
        - <span data-ttu-id="60598-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="60598-1549">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="60598-1550">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="60598-1550">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="60598-1551">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="60598-1551">New cmdlets</span></span>
        - <span data-ttu-id="60598-1552">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="60598-1552">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="60598-1553">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="60598-1553">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="60598-1554">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="60598-1554">New cmdlets</span></span>
        - <span data-ttu-id="60598-1555">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="60598-1555">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="60598-1556">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="60598-1556">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="60598-1557">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="60598-1557">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="60598-1558">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1558">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="60598-1559">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1559">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="60598-1560">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60598-1560">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="60598-1561">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="60598-1561">New cmdlets</span></span>
        - <span data-ttu-id="60598-1562">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60598-1562">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="60598-1563">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60598-1563">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="60598-1564">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="60598-1564">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="60598-1565">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1565">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="60598-1566">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="60598-1566">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="60598-1567">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="60598-1567">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="60598-1568">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="60598-1568">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="60598-1569">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60598-1569">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="60598-1570">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60598-1570">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="60598-1571">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="60598-1571">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="60598-1572">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-1572">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="60598-1573">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="60598-1573">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="60598-1574">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-1574">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="60598-1575">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="60598-1575">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="60598-1576">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="60598-1576">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="60598-1577">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="60598-1577">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="60598-1578">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="60598-1578">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="60598-1579">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1579">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="60598-1580">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="60598-1580">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="60598-1581">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="60598-1581">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="60598-1582">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="60598-1582">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="60598-1583">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="60598-1583">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="60598-1584">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="60598-1584">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="60598-1585">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="60598-1585">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="60598-1586">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="60598-1586">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="60598-1587">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="60598-1587">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="60598-1588">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="60598-1588">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="60598-1589">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1589">Az.OperationalInsights</span></span>
* <span data-ttu-id="60598-1590">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="60598-1590">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1591">Az.Resources</span></span>
* <span data-ttu-id="60598-1592">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="60598-1592">Support for additional Template Export options</span></span>
    - <span data-ttu-id="60598-1593">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1593">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="60598-1594">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1594">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="60598-1595">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="60598-1595">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-1596">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-1596">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-1597">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="60598-1597">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1598">Az.Sql</span></span>
* <span data-ttu-id="60598-1599">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="60598-1599">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="60598-1600">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="60598-1600">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="60598-1601">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="60598-1601">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="60598-1602">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60598-1602">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="60598-1603">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60598-1603">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="60598-1604">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="60598-1604">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="60598-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="60598-1605">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="60598-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="60598-1606">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1607">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1607">Az.Storage</span></span>
* <span data-ttu-id="60598-1608">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60598-1608">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="60598-1609">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1609">New-AzStorageAccount</span></span>
* <span data-ttu-id="60598-1610">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="60598-1610">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="60598-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1611">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1612">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1612">Az.Websites</span></span>
* <span data-ttu-id="60598-1613">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="60598-1613">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="60598-1614">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="60598-1614">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="60598-1615">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1615">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="60598-1616">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-1616">Az.Cdn</span></span>
* <span data-ttu-id="60598-1617">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="60598-1617">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1618">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1618">Az.Compute</span></span>
* <span data-ttu-id="60598-1619">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="60598-1619">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="60598-1620">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="60598-1620">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="60598-1621">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-1621">Az.EventHub</span></span>
* <span data-ttu-id="60598-1622">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="60598-1622">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="60598-1623">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60598-1623">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1624">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1624">Az.Network</span></span>
* <span data-ttu-id="60598-1625">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="60598-1625">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="60598-1626">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="60598-1626">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="60598-1627">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1627">Az.PolicyInsights</span></span>
* <span data-ttu-id="60598-1628">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="60598-1628">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1630">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="60598-1630">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="60598-1631">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="60598-1631">Az.ServiceBus</span></span>
* <span data-ttu-id="60598-1632">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60598-1632">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-1633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-1633">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-1634">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="60598-1634">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="60598-1635">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="60598-1635">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1636">Az.Sql</span></span>
* <span data-ttu-id="60598-1637">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="60598-1637">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="60598-1638">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1638">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="60598-1639">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="60598-1639">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="60598-1640">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="60598-1640">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1641">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1641">Az.Websites</span></span>
* <span data-ttu-id="60598-1642">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="60598-1642">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="60598-1643">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1643">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="60598-1644">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-1644">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-1645">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="60598-1645">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="60598-1646">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="60598-1646">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="60598-1647">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="60598-1647">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="60598-1648">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="60598-1648">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="60598-1649">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="60598-1649">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="60598-1650">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="60598-1650">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="60598-1651">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="60598-1651">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="60598-1652">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="60598-1652">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="60598-1653">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-1653">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="60598-1654">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="60598-1654">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="60598-1655">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1655">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="60598-1656">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="60598-1656">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="60598-1657">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="60598-1657">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="60598-1658">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="60598-1658">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="60598-1659">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="60598-1659">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="60598-1660">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="60598-1660">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="60598-1661">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="60598-1661">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="60598-1662">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="60598-1662">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="60598-1663">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="60598-1663">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="60598-1664">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="60598-1664">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="60598-1665">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="60598-1665">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="60598-1666">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="60598-1666">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="60598-1667">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="60598-1667">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="60598-1668">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-1668">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="60598-1669">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="60598-1669">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="60598-1670">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="60598-1670">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="60598-1671">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="60598-1671">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="60598-1672">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="60598-1672">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="60598-1673">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="60598-1673">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="60598-1674">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="60598-1674">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="60598-1675">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="60598-1675">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="60598-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="60598-1676">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="60598-1677">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="60598-1677">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="60598-1678">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="60598-1678">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="60598-1679">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="60598-1679">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="60598-1680">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="60598-1680">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="60598-1681">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="60598-1681">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="60598-1682">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="60598-1682">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="60598-1683">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="60598-1683">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="60598-1684">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="60598-1684">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="60598-1685">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="60598-1685">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="60598-1686">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="60598-1686">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="60598-1687">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="60598-1687">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="60598-1688">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="60598-1688">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="60598-1689">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="60598-1689">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="60598-1690">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="60598-1690">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="60598-1691">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="60598-1691">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="60598-1692">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="60598-1692">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="60598-1693">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="60598-1693">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="60598-1694">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="60598-1694">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="60598-1695">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="60598-1695">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="60598-1696">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="60598-1696">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="60598-1697">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="60598-1697">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="60598-1698">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="60598-1698">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="60598-1699">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="60598-1699">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="60598-1700">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="60598-1700">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="60598-1701">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="60598-1701">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="60598-1702">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="60598-1702">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="60598-1703">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="60598-1703">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="60598-1704">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="60598-1704">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="60598-1705">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="60598-1705">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="60598-1706">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="60598-1706">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="60598-1707">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="60598-1707">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="60598-1708">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="60598-1708">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="60598-1709">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="60598-1709">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="60598-1710">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="60598-1710">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="60598-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="60598-1711">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="60598-1712">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="60598-1712">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="60598-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="60598-1713">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="60598-1714">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="60598-1714">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="60598-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="60598-1715">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="60598-1716">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="60598-1716">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="60598-1717">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="60598-1717">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="60598-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="60598-1718">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="60598-1719">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="60598-1719">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="60598-1720">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="60598-1720">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="60598-1721">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="60598-1721">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-1722">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1722">Az.Automation</span></span>
* <span data-ttu-id="60598-1723">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="60598-1723">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="60598-1724">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="60598-1724">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="60598-1725">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="60598-1725">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="60598-1726">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="60598-1726">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="60598-1727">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="60598-1727">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="60598-1728">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="60598-1728">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="60598-1729">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="60598-1729">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1730">Az.Compute</span></span>
* <span data-ttu-id="60598-1731">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="60598-1731">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="60598-1732">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="60598-1732">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-1733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-1733">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-1734">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1734">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-1735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-1735">Az.Monitor</span></span>
* <span data-ttu-id="60598-1736">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-1736">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1737">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1737">Az.Network</span></span>
* <span data-ttu-id="60598-1738">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="60598-1738">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="60598-1739">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="60598-1739">Updated cmdlet:</span></span>
        - <span data-ttu-id="60598-1740">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="60598-1740">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="60598-1741">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="60598-1741">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1742">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1742">Az.Resources</span></span>
* <span data-ttu-id="60598-1743">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="60598-1743">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1744">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1744">Az.Sql</span></span>
* <span data-ttu-id="60598-1745">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="60598-1745">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="60598-1746">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1746">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-1747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1747">Az.Accounts</span></span>
* <span data-ttu-id="60598-1748">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="60598-1748">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-1749">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-1749">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-1750">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="60598-1750">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="60598-1751">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="60598-1751">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1752">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1752">Az.Compute</span></span>
* <span data-ttu-id="60598-1753">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="60598-1753">Proximity placement group feature.</span></span>
    - <span data-ttu-id="60598-1754">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1754">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="60598-1755">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1755">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="60598-1756">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="60598-1756">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="60598-1757">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="60598-1757">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="60598-1758">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-1758">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="60598-1759">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="60598-1759">Breaking changes</span></span>
    - <span data-ttu-id="60598-1760">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="60598-1760">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="60598-1761">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="60598-1761">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="60598-1762">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="60598-1762">Az.DeploymentManager</span></span>
* <span data-ttu-id="60598-1763">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1763">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="60598-1764">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="60598-1764">Az.Dns</span></span>
* <span data-ttu-id="60598-1765">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="60598-1765">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="60598-1766">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="60598-1766">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="60598-1767">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="60598-1767">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="60598-1768">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-1768">Az.FrontDoor</span></span>
* <span data-ttu-id="60598-1769">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1769">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="60598-1770">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="60598-1770">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="60598-1771">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-1771">Az.HDInsight</span></span>
* <span data-ttu-id="60598-1772">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="60598-1772">Removed two cmdlets:</span></span>
    - <span data-ttu-id="60598-1773">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="60598-1773">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="60598-1774">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="60598-1774">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="60598-1775">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="60598-1775">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="60598-1776">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="60598-1776">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="60598-1777">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="60598-1777">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="60598-1778">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="60598-1778">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-1779">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-1779">Az.Monitor</span></span>
* <span data-ttu-id="60598-1780">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="60598-1780">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="60598-1781">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="60598-1781">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="60598-1782">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1782">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="60598-1783">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="60598-1783">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="60598-1784">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="60598-1784">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="60598-1785">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="60598-1785">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="60598-1786">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="60598-1786">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="60598-1787">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="60598-1787">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="60598-1788">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="60598-1788">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="60598-1789">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="60598-1789">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="60598-1790">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="60598-1790">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="60598-1791">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="60598-1791">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="60598-1792">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="60598-1792">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="60598-1793">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="60598-1793">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1794">Az.Network</span></span>
* <span data-ttu-id="60598-1795">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="60598-1795">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="60598-1796">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="60598-1796">New cmdlets</span></span>
        - <span data-ttu-id="60598-1797">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="60598-1797">New-AzNatGateway</span></span>
        - <span data-ttu-id="60598-1798">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="60598-1798">Get-AzNatGateway</span></span>
        - <span data-ttu-id="60598-1799">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="60598-1799">Set-AzNatGateway</span></span>
        - <span data-ttu-id="60598-1800">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="60598-1800">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="60598-1801">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="60598-1801">Updated cmdlets</span></span>
        - <span data-ttu-id="60598-1802">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="60598-1802">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="60598-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="60598-1803">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="60598-1804">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="60598-1804">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="60598-1805">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="60598-1805">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="60598-1806">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="60598-1806">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="60598-1807">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1807">Az.PolicyInsights</span></span>
* <span data-ttu-id="60598-1808">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="60598-1808">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="60598-1809">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="60598-1809">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="60598-1810">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="60598-1810">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1811">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1811">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1812">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="60598-1812">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="60598-1813">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="60598-1813">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="60598-1814">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="60598-1814">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="60598-1815">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-1815">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="60598-1816">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="60598-1816">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="60598-1817">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="60598-1817">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="60598-1818">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="60598-1818">Az.Relay</span></span>
* <span data-ttu-id="60598-1819">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="60598-1819">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="60598-1820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="60598-1820">Az.ServiceBus</span></span>
* <span data-ttu-id="60598-1821">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="60598-1821">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1822">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1822">Az.Storage</span></span>
* <span data-ttu-id="60598-1823">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="60598-1823">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="60598-1824">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="60598-1824">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="60598-1825">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="60598-1825">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="60598-1826">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1826">New-AzStorageAccount</span></span>
* <span data-ttu-id="60598-1827">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="60598-1827">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="60598-1828">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1828">New-AzStorageAccount</span></span>
    - <span data-ttu-id="60598-1829">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1829">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="60598-1830">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-1830">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1831">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1831">Az.Websites</span></span>
* <span data-ttu-id="60598-1832">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="60598-1832">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="60598-1833">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="60598-1833">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="60598-1834">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1834">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="60598-1835">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="60598-1835">Highlights since the last major release</span></span>
* <span data-ttu-id="60598-1836">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="60598-1836">General availability of `Az` module</span></span>
* <span data-ttu-id="60598-1837">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="60598-1837">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="60598-1838">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="60598-1838">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="60598-1839">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1839">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="60598-1840">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="60598-1840">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="60598-1841">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1841">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="60598-1842">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="60598-1842">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-1843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1843">Az.Accounts</span></span>
* <span data-ttu-id="60598-1844">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="60598-1844">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="60598-1845">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="60598-1845">Az.Batch</span></span>
* <span data-ttu-id="60598-1846">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1846">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="60598-1847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-1847">Az.Cdn</span></span>
* <span data-ttu-id="60598-1848">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1848">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-1849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-1849">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-1850">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1850">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1851">Az.Compute</span></span>
* <span data-ttu-id="60598-1852">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="60598-1852">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="60598-1853">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1853">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="60598-1854">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="60598-1854">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-1855">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-1855">Az.DataFactory</span></span>
* <span data-ttu-id="60598-1856">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="60598-1856">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-1858">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1858">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="60598-1859">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="60598-1859">Az.EventGrid</span></span>
* <span data-ttu-id="60598-1860">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="60598-1860">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="60598-1861">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-1861">Az.EventHub</span></span>
* <span data-ttu-id="60598-1862">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="60598-1862">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="60598-1863">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="60598-1863">Az.HDInsight</span></span>
* <span data-ttu-id="60598-1864">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1864">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-1865">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-1865">Az.IotHub</span></span>
* <span data-ttu-id="60598-1866">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1866">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-1867">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-1867">Az.KeyVault</span></span>
* <span data-ttu-id="60598-1868">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1868">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="60598-1869">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="60598-1869">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="60598-1870">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="60598-1870">Az.MachineLearning</span></span>
* <span data-ttu-id="60598-1871">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1871">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="60598-1872">Az.Media</span><span class="sxs-lookup"><span data-stu-id="60598-1872">Az.Media</span></span>
* <span data-ttu-id="60598-1873">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1873">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-1874">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-1874">Az.Monitor</span></span>
  * <span data-ttu-id="60598-1875">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="60598-1875">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="60598-1876">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="60598-1876">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="60598-1877">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="60598-1877">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="60598-1878">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="60598-1878">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="60598-1879">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="60598-1879">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="60598-1880">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="60598-1880">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="60598-1881">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="60598-1881">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1882">Az.Network</span></span>
* <span data-ttu-id="60598-1883">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="60598-1884">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="60598-1884">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="60598-1885">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="60598-1885">Az.NotificationHubs</span></span>
* <span data-ttu-id="60598-1886">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="60598-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="60598-1888">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="60598-1889">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="60598-1889">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="60598-1890">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1891">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1891">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1892">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="60598-1893">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1893">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="60598-1894">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="60598-1894">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="60598-1895">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="60598-1895">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="60598-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="60598-1896">Az.RedisCache</span></span>
* <span data-ttu-id="60598-1897">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1898">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1898">Az.Resources</span></span>
* <span data-ttu-id="60598-1899">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="60598-1899">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1900">Az.Sql</span></span>
* <span data-ttu-id="60598-1901">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="60598-1901">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="60598-1902">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1902">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="60598-1903">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="60598-1903">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="60598-1904">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="60598-1904">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="60598-1905">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="60598-1905">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="60598-1906">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="60598-1906">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="60598-1907">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="60598-1907">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1908">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1908">Az.Websites</span></span>
* <span data-ttu-id="60598-1909">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="60598-1909">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="60598-1910">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="60598-1910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="60598-1911">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="60598-1911">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="60598-1912">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="60598-1912">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="60598-1913">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1913">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="60598-1914">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="60598-1914">Highlights since the last major release</span></span>
* <span data-ttu-id="60598-1915">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="60598-1915">General availability of `Az` module</span></span>
* <span data-ttu-id="60598-1916">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="60598-1916">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="60598-1917">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="60598-1917">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="60598-1918">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1918">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="60598-1919">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="60598-1919">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="60598-1920">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1920">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="60598-1921">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="60598-1921">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="60598-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-1922">Az.Accounts</span></span>
* <span data-ttu-id="60598-1923">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="60598-1923">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="60598-1924">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="60598-1924">Az.AnalysisServices</span></span>
* <span data-ttu-id="60598-1925">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="60598-1925">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="60598-1926">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="60598-1926">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1927">Az.Automation</span></span>
* <span data-ttu-id="60598-1928">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="60598-1928">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="60598-1929">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="60598-1929">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="60598-1930">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1930">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1931">Az.Compute</span></span>
* <span data-ttu-id="60598-1932">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="60598-1932">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="60598-1933">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="60598-1933">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="60598-1934">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="60598-1934">Az.ContainerInstance</span></span>
* <span data-ttu-id="60598-1935">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="60598-1935">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-1936">Az.DataFactory</span></span>
* <span data-ttu-id="60598-1937">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="60598-1937">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="60598-1938">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="60598-1938">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1939">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1939">Az.Resources</span></span>
* <span data-ttu-id="60598-1940">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="60598-1940">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="60598-1941">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-1941">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="60598-1942">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="60598-1942">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="60598-1943">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="60598-1943">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="60598-1944">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="60598-1944">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="60598-1945">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="60598-1945">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1946">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1946">Az.Sql</span></span>
* <span data-ttu-id="60598-1947">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="60598-1947">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1948">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1948">Az.Storage</span></span>
* <span data-ttu-id="60598-1949">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1949">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="60598-1950">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="60598-1950">New-AzStorageContext</span></span>
* <span data-ttu-id="60598-1951">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="60598-1951">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="60598-1952">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="60598-1952">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="60598-1953">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="60598-1953">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="60598-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1954">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="60598-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1955">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="60598-1956">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="60598-1956">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="60598-1957">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="60598-1957">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="60598-1958">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="60598-1958">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="60598-1959">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="60598-1959">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="60598-1960">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="60598-1960">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="60598-1961">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-1961">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="60598-1962">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="60598-1962">Highlights since the last major release</span></span>
* <span data-ttu-id="60598-1963">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="60598-1963">General availability of `Az` module</span></span>
* <span data-ttu-id="60598-1964">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="60598-1964">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="60598-1965">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="60598-1965">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="60598-1966">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1966">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="60598-1967">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="60598-1967">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="60598-1968">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1968">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="60598-1969">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="60598-1969">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-1970">Az.Automation</span></span>
* <span data-ttu-id="60598-1971">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="60598-1971">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="60598-1972">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="60598-1972">Dynamic grouping</span></span>
    * <span data-ttu-id="60598-1973">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="60598-1973">Pre-Post script</span></span>
    * <span data-ttu-id="60598-1974">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="60598-1974">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-1975">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-1975">Az.Compute</span></span>
* <span data-ttu-id="60598-1976">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="60598-1976">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="60598-1977">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="60598-1977">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-1978">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-1978">Az.KeyVault</span></span>
* <span data-ttu-id="60598-1979">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-1979">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-1980">Az.Network</span></span>
* <span data-ttu-id="60598-1981">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-1981">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="60598-1982">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="60598-1982">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-1983">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-1983">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-1984">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="60598-1984">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="60598-1985">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="60598-1985">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-1986">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-1986">Az.Resources</span></span>
* <span data-ttu-id="60598-1987">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60598-1987">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="60598-1988">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="60598-1988">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-1989">Az.Sql</span></span>
* <span data-ttu-id="60598-1990">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="60598-1990">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-1991">Az.Storage</span></span>
* <span data-ttu-id="60598-1992">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="60598-1992">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="60598-1993">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1993">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="60598-1994">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1994">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="60598-1995">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-1995">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="60598-1996">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="60598-1996">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="60598-1997">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="60598-1997">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="60598-1998">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="60598-1998">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-1999">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-1999">Az.Websites</span></span>
* <span data-ttu-id="60598-2000">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="60598-2000">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="60598-2001">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-2001">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-2002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2002">Az.Accounts</span></span>
* <span data-ttu-id="60598-2003">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="60598-2003">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="60598-2004">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="60598-2004">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-2005">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-2005">Az.Automation</span></span>
* <span data-ttu-id="60598-2006">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-2006">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="60598-2007">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="60598-2007">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="60598-2008">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="60598-2008">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="60598-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-2009">Az.Cdn</span></span>
* <span data-ttu-id="60598-2010">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="60598-2010">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2011">Az.Compute</span></span>
* <span data-ttu-id="60598-2012">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="60598-2012">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-2013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-2013">Az.DataFactory</span></span>
* <span data-ttu-id="60598-2014">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="60598-2014">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="60598-2015">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="60598-2015">Az.LogicApp</span></span>
* <span data-ttu-id="60598-2016">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="60598-2016">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-2017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2017">Az.Network</span></span>
* <span data-ttu-id="60598-2018">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="60598-2018">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-2019">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-2019">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-2020">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-2020">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="60598-2021">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="60598-2021">SDK Update</span></span>
* <span data-ttu-id="60598-2022">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="60598-2022">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="60598-2023">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="60598-2023">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2024">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2024">Az.Resources</span></span>
* <span data-ttu-id="60598-2025">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="60598-2025">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="60598-2026">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="60598-2026">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="60598-2027">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="60598-2027">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="60598-2028">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="60598-2028">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="60598-2029">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="60598-2029">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="60598-2030">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="60598-2030">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-2031">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2031">Az.Sql</span></span>
* <span data-ttu-id="60598-2032">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="60598-2032">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="60598-2033">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="60598-2033">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-2034">Az.Storage</span></span>
* <span data-ttu-id="60598-2035">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-2035">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="60598-2036">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-2036">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="60598-2037">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="60598-2037">Az.AnalysisServices</span></span>
* <span data-ttu-id="60598-2038">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="60598-2038">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-2039">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-2039">Az.Automation</span></span>
* <span data-ttu-id="60598-2040">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2040">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="60598-2041">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2041">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="60598-2042">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2042">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-2043">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-2043">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-2044">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="60598-2044">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2045">Az.Compute</span></span>
* <span data-ttu-id="60598-2046">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="60598-2046">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="60598-2047">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="60598-2047">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="60598-2048">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="60598-2048">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="60598-2049">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="60598-2049">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-2051">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="60598-2051">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="60598-2052">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-2052">Az.EventHub</span></span>
* <span data-ttu-id="60598-2053">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="60598-2053">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-2054">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-2054">Az.KeyVault</span></span>
* <span data-ttu-id="60598-2055">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="60598-2055">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="60598-2056">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="60598-2056">Az.LogicApp</span></span>
* <span data-ttu-id="60598-2057">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="60598-2057">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="60598-2058">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="60598-2058">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="60598-2059">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="60598-2059">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="60598-2060">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="60598-2060">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="60598-2061">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="60598-2061">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="60598-2062">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="60598-2062">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="60598-2063">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="60598-2063">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="60598-2064">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="60598-2064">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="60598-2065">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2065">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="60598-2066">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2066">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="60598-2067">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2067">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="60598-2068">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2068">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="60598-2069">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="60598-2069">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="60598-2070">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-2070">Az.Monitor</span></span>
* <span data-ttu-id="60598-2071">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="60598-2071">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-2072">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2072">Az.Network</span></span>
* <span data-ttu-id="60598-2073">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="60598-2073">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="60598-2074">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-2074">Az.OperationalInsights</span></span>
* <span data-ttu-id="60598-2075">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="60598-2075">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="60598-2076">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="60598-2076">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="60598-2077">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="60598-2077">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2078">Az.Resources</span></span>
* <span data-ttu-id="60598-2079">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="60598-2079">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="60598-2080">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="60598-2080">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="60598-2081">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="60598-2081">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="60598-2082">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="60598-2082">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-2083">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2083">Az.Sql</span></span>
* <span data-ttu-id="60598-2084">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="60598-2084">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="60598-2085">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="60598-2085">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-2086">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-2086">Az.Websites</span></span>
* <span data-ttu-id="60598-2087">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="60598-2087">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="60598-2088">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-2088">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-2089">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2089">Az.Accounts</span></span>
* <span data-ttu-id="60598-2090">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="60598-2090">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="60598-2091">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="60598-2091">Az.AnalysisServices</span></span>
<span data-ttu-id="60598-2092">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="60598-2092">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2093">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2093">Az.Compute</span></span>
* <span data-ttu-id="60598-2094">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="60598-2094">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="60598-2095">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="60598-2095">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="60598-2096">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="60598-2096">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-2097">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-2097">Az.RecoveryServices</span></span>
<span data-ttu-id="60598-2098">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="60598-2098">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2099">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2099">Az.Resources</span></span>
* <span data-ttu-id="60598-2100">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="60598-2100">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="60598-2101">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="60598-2101">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="60598-2102">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="60598-2102">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="60598-2103">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="60598-2103">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-2104">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2104">Az.Sql</span></span>
* <span data-ttu-id="60598-2105">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="60598-2105">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="60598-2106">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="60598-2106">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="60598-2107">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="60598-2107">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="60598-2108">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-2108">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-2109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2109">Az.Accounts</span></span>
* <span data-ttu-id="60598-2110">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="60598-2110">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="60598-2111">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="60598-2111">Az.AnalysisServices</span></span>
* <span data-ttu-id="60598-2112">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="60598-2112">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="60598-2113">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-2113">Az.RecoveryServices</span></span>
* <span data-ttu-id="60598-2114">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="60598-2114">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="60598-2115">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-2115">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2116">Az.Accounts</span></span>
* <span data-ttu-id="60598-2117">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="60598-2117">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="60598-2118">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2118">Update incorrect online help URLs</span></span>
* <span data-ttu-id="60598-2119">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="60598-2119">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="60598-2120">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="60598-2120">Az.Aks</span></span>
* <span data-ttu-id="60598-2121">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2121">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="60598-2122">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-2122">Az.Automation</span></span>
* <span data-ttu-id="60598-2123">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="60598-2123">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="60598-2124">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2124">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="60598-2125">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="60598-2125">Az.Cdn</span></span>
* <span data-ttu-id="60598-2126">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2126">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2127">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2127">Az.Compute</span></span>
* <span data-ttu-id="60598-2128">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="60598-2128">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="60598-2129">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="60598-2129">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="60598-2130">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="60598-2130">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="60598-2131">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="60598-2131">Az.ContainerRegistry</span></span>
* <span data-ttu-id="60598-2132">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2132">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="60598-2133">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="60598-2133">Az.DataFactory</span></span>
* <span data-ttu-id="60598-2134">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="60598-2134">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-2135">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-2135">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-2136">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="60598-2136">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="60598-2137">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="60598-2137">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="60598-2138">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2138">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-2139">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-2139">Az.IotHub</span></span>
* <span data-ttu-id="60598-2140">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="60598-2140">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="60598-2141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-2141">Az.KeyVault</span></span>
* <span data-ttu-id="60598-2142">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2142">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2143">Az.Network</span></span>
* <span data-ttu-id="60598-2144">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2144">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2145">Az.Resources</span></span>
* <span data-ttu-id="60598-2146">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="60598-2146">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="60598-2147">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="60598-2147">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="60598-2148">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="60598-2148">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="60598-2149">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="60598-2149">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="60598-2150">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="60598-2150">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="60598-2151">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="60598-2151">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="60598-2152">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="60598-2152">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-2153">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-2153">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-2154">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="60598-2154">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="60598-2155">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="60598-2155">Fix some error messages.</span></span>
* <span data-ttu-id="60598-2156">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="60598-2156">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="60598-2157">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="60598-2157">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="60598-2158">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="60598-2158">Az.SignalR</span></span>
* <span data-ttu-id="60598-2159">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2159">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-2160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2160">Az.Sql</span></span>
* <span data-ttu-id="60598-2161">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="60598-2162">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="60598-2162">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="60598-2163">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="60598-2163">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="60598-2164">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="60598-2164">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-2165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-2165">Az.Storage</span></span>
* <span data-ttu-id="60598-2166">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2166">Update incorrect online help URLs</span></span>
* <span data-ttu-id="60598-2167">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="60598-2167">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="60598-2168">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="60598-2168">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="60598-2169">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="60598-2169">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="60598-2170">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="60598-2170">Az.TrafficManager</span></span>
* <span data-ttu-id="60598-2171">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2171">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-2172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-2172">Az.Websites</span></span>
* <span data-ttu-id="60598-2173">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="60598-2173">Update incorrect online help URLs</span></span>
* <span data-ttu-id="60598-2174">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="60598-2174">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="60598-2175">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="60598-2175">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="60598-2176">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="60598-2176">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="60598-2177">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2177">Az.Accounts</span></span>
* <span data-ttu-id="60598-2178">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="60598-2178">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2179">Az.Compute</span></span>
* <span data-ttu-id="60598-2180">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="60598-2180">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="60598-2181">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="60598-2181">Updated the description of ID in help files</span></span>
* <span data-ttu-id="60598-2182">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2182">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-2183">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-2183">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-2184">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="60598-2184">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="60598-2185">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="60598-2185">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="60598-2186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="60598-2186">Az.EventGrid</span></span>
* <span data-ttu-id="60598-2187">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="60598-2187">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="60598-2188">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="60598-2188">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="60598-2189">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="60598-2189">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="60598-2190">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="60598-2190">Event Time-To-Live,</span></span>
        - <span data-ttu-id="60598-2191">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="60598-2191">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="60598-2192">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="60598-2192">Dead letter endpoint.</span></span>
    - <span data-ttu-id="60598-2193">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="60598-2193">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="60598-2194">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="60598-2194">Event Time-To-Live,</span></span>
        - <span data-ttu-id="60598-2195">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="60598-2195">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="60598-2196">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="60598-2196">Dead letter endpoint.</span></span>
* <span data-ttu-id="60598-2197">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="60598-2197">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="60598-2198">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="60598-2198">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="60598-2199">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-2199">Az.IotHub</span></span>
* <span data-ttu-id="60598-2200">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="60598-2200">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="60598-2201">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="60598-2201">Az.LogicApp</span></span>
* <span data-ttu-id="60598-2202">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="60598-2202">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2203">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2203">Az.Resources</span></span>
* <span data-ttu-id="60598-2204">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="60598-2204">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="60598-2205">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="60598-2205">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="60598-2206">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="60598-2206">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="60598-2207">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="60598-2207">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="60598-2208">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="60598-2208">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="60598-2209">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="60598-2209">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="60598-2210">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="60598-2210">Az.SignalR</span></span>
* <span data-ttu-id="60598-2211">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2211">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2212">Az.Sql</span></span>
* <span data-ttu-id="60598-2213">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="60598-2213">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="60598-2214">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-2214">Az.Storage</span></span>
* <span data-ttu-id="60598-2215">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="60598-2215">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="60598-2216">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="60598-2216">New-AzStorageContext</span></span>
* <span data-ttu-id="60598-2217">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="60598-2217">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="60598-2218">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="60598-2218">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-2219">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-2219">Az.Websites</span></span>
* <span data-ttu-id="60598-2220">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="60598-2220">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="60598-2221">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2221">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="60598-2222">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="60598-2222">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="60598-2223">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-2223">General</span></span>

- <span data-ttu-id="60598-2224">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="60598-2224">General Availability of Az Module</span></span>
- <span data-ttu-id="60598-2225">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="60598-2225">Online help for each module</span></span>
- <span data-ttu-id="60598-2226">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="60598-2226">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="60598-2227">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="60598-2227">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="60598-2228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2228">Az.Accounts</span></span>
- <span data-ttu-id="60598-2229">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="60598-2229">Changed from Az.Profile</span></span>
- <span data-ttu-id="60598-2230">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="60598-2230">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="60598-2231">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-2231">Az.ApiManagement</span></span>
- <span data-ttu-id="60598-2232">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="60598-2232">Fixes for #7002</span></span>
- <span data-ttu-id="60598-2233">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2233">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="60598-2234">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="60598-2234">Az.Batch</span></span>
- <span data-ttu-id="60598-2235">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="60598-2235">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="60598-2236">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="60598-2236">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="60598-2237">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2237">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="60598-2238">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="60598-2238">Az.Billing</span></span>
- <span data-ttu-id="60598-2239">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2239">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="60598-2240">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="60598-2240">Az.CognitivServices</span></span>
- <span data-ttu-id="60598-2241">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="60598-2241">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="60598-2242">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="60598-2242">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="60598-2243">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="60598-2243">Az.ContainerInstance</span></span>
- <span data-ttu-id="60598-2244">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="60598-2244">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="60598-2245">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="60598-2245">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="60598-2246">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2246">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="60598-2247">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-2247">Az.DataLakeStore</span></span>
- <span data-ttu-id="60598-2248">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2248">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="60598-2249">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="60598-2249">Az.Monitor</span></span>
- <span data-ttu-id="60598-2250">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2250">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="60598-2251">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="60598-2251">Az.KeyVault</span></span>
- <span data-ttu-id="60598-2252">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="60598-2252">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="60598-2253">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="60598-2253">Az.MachineLearning</span></span>
- <span data-ttu-id="60598-2254">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="60598-2254">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="60598-2255">Az.Media</span><span class="sxs-lookup"><span data-stu-id="60598-2255">Az.Media</span></span>
- <span data-ttu-id="60598-2256">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="60598-2256">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="60598-2257">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2257">Az.Network</span></span>
<span data-ttu-id="60598-2258">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="60598-2258">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="60598-2259">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="60598-2259">New cmdlets added:</span></span>
        - <span data-ttu-id="60598-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-2260">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="60598-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-2261">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="60598-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-2262">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="60598-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-2263">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="60598-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-2264">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="60598-2265">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="60598-2265">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="60598-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="60598-2266">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="60598-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="60598-2267">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="60598-2268">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="60598-2268">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="60598-2269">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60598-2269">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="60598-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60598-2270">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="60598-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="60598-2271">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="60598-2272">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="60598-2272">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="60598-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="60598-2273">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="60598-2274">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="60598-2274">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="60598-2275">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="60598-2275">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="60598-2276">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60598-2276">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="60598-2277">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60598-2277">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="60598-2278">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="60598-2278">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="60598-2279">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="60598-2279">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="60598-2280">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="60598-2281">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="60598-2281">Az.OperationalInsights</span></span>
- <span data-ttu-id="60598-2282">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2282">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="60598-2283">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="60598-2283">Az.Profile</span></span>
- <span data-ttu-id="60598-2284">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="60598-2284">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="60598-2285">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-2285">Az.RecoveryServices</span></span>
- <span data-ttu-id="60598-2286">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="60598-2287">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2287">Az.Resources</span></span>
- <span data-ttu-id="60598-2288">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="60598-2289">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-2289">Az.ServiceFabric</span></span>
- <span data-ttu-id="60598-2290">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="60598-2290">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="60598-2291">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2291">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="60598-2292">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="60598-2292">Az.SIgnalR</span></span>
- <span data-ttu-id="60598-2293">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="60598-2293">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="60598-2294">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2294">Az.Sql</span></span>
- <span data-ttu-id="60598-2295">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="60598-2295">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="60598-2296">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="60598-2296">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="60598-2297">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2297">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="60598-2298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-2298">Az.Storage</span></span>
- <span data-ttu-id="60598-2299">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="60598-2300">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-2300">Az.Websites</span></span>
- <span data-ttu-id="60598-2301">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="60598-2301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="60598-2302">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="60598-2302">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="60598-2303">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-2303">General</span></span>

* <span data-ttu-id="60598-2304">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="60598-2304">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="60598-2305">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2305">Az.Compute</span></span>

* <span data-ttu-id="60598-2306">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="60598-2306">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="60598-2307">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-2307">Az.DataLakeStore</span></span>

* <span data-ttu-id="60598-2308">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="60598-2308">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="60598-2309">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="60598-2309">Az.FrontDoor</span></span>

* <span data-ttu-id="60598-2310">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="60598-2310">Fixed some broken links</span></span>
    - <span data-ttu-id="60598-2311">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="60598-2311">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="60598-2312">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="60598-2312">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="60598-2313">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="60598-2313">Az.RecoveryServices</span></span>

* <span data-ttu-id="60598-2314">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="60598-2314">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="60598-2315">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="60598-2315">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="60598-2316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2316">Az.Resources</span></span>

* <span data-ttu-id="60598-2317">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="60598-2317">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="60598-2318">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="60598-2318">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="60598-2319">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2319">Az.Sql</span></span>

* <span data-ttu-id="60598-2320">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="60598-2320">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="60598-2321">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="60598-2321">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="60598-2322">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="60598-2322">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="60598-2323">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-2323">Az.Storage</span></span>

* <span data-ttu-id="60598-2324">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="60598-2324">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="60598-2325">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="60598-2325">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="60598-2326">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="60598-2326">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="60598-2327">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="60598-2327">Support Static Website configuration</span></span>
    - <span data-ttu-id="60598-2328">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="60598-2328">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="60598-2329">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="60598-2329">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="60598-2330">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-2330">Az.Websites</span></span>

* <span data-ttu-id="60598-2331">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="60598-2331">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="60598-2332">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="60598-2332">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="60598-2333">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="60598-2333">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="60598-2334">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="60598-2334">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="60598-2335">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="60598-2335">Az.ApiManagement</span></span>
* <span data-ttu-id="60598-2336">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="60598-2336">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="60598-2337">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="60598-2337">Az.Automation</span></span>
* <span data-ttu-id="60598-2338">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="60598-2338">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="60598-2339">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-2339">Added Update Management cmdlets</span></span>
* <span data-ttu-id="60598-2340">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-2340">Added Source Control cmdlets</span></span>
* <span data-ttu-id="60598-2341">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="60598-2341">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="60598-2342">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="60598-2342">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="60598-2343">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2343">Az.Compute</span></span>
* <span data-ttu-id="60598-2344">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="60598-2344">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="60598-2345">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="60598-2345">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="60598-2346">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="60598-2346">Az.ContainerInstance</span></span>
* <span data-ttu-id="60598-2347">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="60598-2347">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="60598-2348">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="60598-2348">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="60598-2349">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="60598-2349">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="60598-2350">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2350">Az.Network</span></span>
* <span data-ttu-id="60598-2351">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-2351">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="60598-2352">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="60598-2352">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="60598-2353">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="60598-2353">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="60598-2354">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="60598-2354">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="60598-2355">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="60598-2355">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="60598-2356">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="60598-2356">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="60598-2357">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="60598-2357">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="60598-2358">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="60598-2358">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="60598-2359">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="60598-2359">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="60598-2360">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="60598-2360">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="60598-2361">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="60598-2361">Az.Relay</span></span>
* <span data-ttu-id="60598-2362">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="60598-2362">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="60598-2363">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2363">Az.Resources</span></span>
* <span data-ttu-id="60598-2364">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="60598-2364">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="60598-2365">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="60598-2365">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="60598-2366">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="60598-2366">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="60598-2367">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-2367">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-2368">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="60598-2368">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="60598-2369">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2369">Az.Sql</span></span>
* <span data-ttu-id="60598-2370">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="60598-2370">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="60598-2371">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="60598-2371">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="60598-2372">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="60598-2372">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="60598-2373">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="60598-2373">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="60598-2374">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="60598-2374">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="60598-2375">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="60598-2375">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="60598-2376">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="60598-2376">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="60598-2377">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="60598-2377">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="60598-2378">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="60598-2378">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="60598-2379">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="60598-2379">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="60598-2380">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="60598-2380">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="60598-2381">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="60598-2381">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="60598-2382">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="60598-2382">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="60598-2383">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="60598-2383">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="60598-2384">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="60598-2384">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="60598-2385">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="60598-2385">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="60598-2386">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="60598-2386">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="60598-2387">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="60598-2387">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="60598-2388">Geral</span><span class="sxs-lookup"><span data-stu-id="60598-2388">General</span></span>
* <span data-ttu-id="60598-2389">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="60598-2389">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="60598-2390">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="60598-2390">Az.Profile</span></span>
* <span data-ttu-id="60598-2391">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="60598-2391">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="60598-2392">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="60598-2392">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="60598-2393">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="60598-2393">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="60598-2394">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="60598-2394">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="60598-2395">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="60598-2395">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="60598-2396">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="60598-2396">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="60598-2397">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="60598-2397">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-2398">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-2398">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-2399">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="60598-2399">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2400">Az.Compute</span></span>
* <span data-ttu-id="60598-2401">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="60598-2401">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="60598-2402">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="60598-2402">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="60598-2403">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="60598-2403">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-2404">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-2404">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-2405">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="60598-2405">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="60598-2406">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="60598-2406">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="60598-2407">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="60598-2407">Az.Insights</span></span>
* <span data-ttu-id="60598-2408">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="60598-2408">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="60598-2409">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="60598-2409">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="60598-2410">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="60598-2410">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="60598-2411">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="60598-2411">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-2412">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2412">Az.Network</span></span>
* <span data-ttu-id="60598-2413">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="60598-2413">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="60598-2414">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="60598-2414">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="60598-2415">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="60598-2415">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="60598-2416">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="60598-2416">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="60598-2417">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="60598-2417">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="60598-2418">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="60598-2418">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="60598-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="60598-2419">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="60598-2420">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="60598-2420">Az.PolicyInsights</span></span>
* <span data-ttu-id="60598-2421">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="60598-2421">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2422">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2422">Az.Resources</span></span>
* <span data-ttu-id="60598-2423">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="60598-2423">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="60598-2424">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="60598-2424">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="60598-2425">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="60598-2425">Az.ServiceBus</span></span>
* <span data-ttu-id="60598-2426">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="60598-2426">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="60598-2427">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="60598-2427">Az.ServiceFabric</span></span>
* <span data-ttu-id="60598-2428">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="60598-2428">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="60598-2429">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="60598-2429">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="60598-2430">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="60598-2430">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="60598-2431">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="60598-2431">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="60598-2432">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="60598-2432">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="60598-2433">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="60598-2433">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="60598-2434">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="60598-2434">Az.Profile</span></span>
* <span data-ttu-id="60598-2435">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="60598-2435">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="60598-2436">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="60598-2436">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2437">Az.Compute</span></span>
* <span data-ttu-id="60598-2438">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="60598-2438">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="60598-2439">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="60598-2439">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="60598-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60598-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="60598-2441">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="60598-2441">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="60598-2442">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="60598-2442">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="60598-2443">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="60598-2443">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="60598-2444">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="60598-2444">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="60598-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="60598-2445">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-2446">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2446">Az.Network</span></span>
* <span data-ttu-id="60598-2447">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="60598-2447">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="60598-2448">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="60598-2448">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2449">Az.Resources</span></span>
* <span data-ttu-id="60598-2450">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="60598-2450">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="60598-2451">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="60598-2451">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="60598-2452">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="60598-2452">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="60598-2453">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="60598-2453">Azure.Storage</span></span>
* <span data-ttu-id="60598-2454">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="60598-2454">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="60598-2455">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="60598-2455">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="60598-2456">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="60598-2456">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="60598-2457">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="60598-2457">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="60598-2458">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="60598-2458">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="60598-2459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="60598-2459">Az.CognitiveServices</span></span>
* <span data-ttu-id="60598-2460">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="60598-2460">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="60598-2461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="60598-2461">Az.Compute</span></span>
* <span data-ttu-id="60598-2462">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="60598-2462">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="60598-2463">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="60598-2463">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="60598-2464">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="60598-2464">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="60598-2465">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="60598-2465">Az.DataFactoryV2</span></span>
* <span data-ttu-id="60598-2466">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="60598-2466">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="60598-2467">Az.Network</span><span class="sxs-lookup"><span data-stu-id="60598-2467">Az.Network</span></span>
* <span data-ttu-id="60598-2468">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="60598-2468">Added NetworkProfile functionality.</span></span> <span data-ttu-id="60598-2469">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="60598-2469">new cmdlets added</span></span>
    - <span data-ttu-id="60598-2470">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="60598-2470">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="60598-2471">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="60598-2471">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="60598-2472">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="60598-2472">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="60598-2473">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="60598-2473">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="60598-2474">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="60598-2474">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="60598-2475">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="60598-2475">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="60598-2476">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="60598-2476">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="60598-2477">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="60598-2477">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="60598-2478">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="60598-2478">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="60598-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="60598-2479">Az.RedisCache</span></span>
* <span data-ttu-id="60598-2480">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="60598-2480">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="60598-2481">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="60598-2481">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="60598-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="60598-2482">Az.Resources</span></span>
* <span data-ttu-id="60598-2483">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="60598-2483">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="60598-2484">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="60598-2484">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="60598-2485">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="60598-2485">Az.Sql</span></span>
* <span data-ttu-id="60598-2486">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="60598-2486">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="60598-2487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="60598-2487">Az.Websites</span></span>
* <span data-ttu-id="60598-2488">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="60598-2488">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="60598-2489">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="60598-2489">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="60598-2490">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="60598-2490">0.2.0 - September 2018</span></span>
 <span data-ttu-id="60598-2491">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="60598-2491">Initial Release</span></span>
