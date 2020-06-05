---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 8d53923f76506469cdc2c111faf7c4568b54f7de
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84294786"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="e726f-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e726f-103">Azure PowerShell release notes</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="e726f-104">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-104">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-105">Az.Accounts</span></span>
* <span data-ttu-id="e726f-106">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="e726f-106">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e726f-107">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e726f-107">Az.AnalysisServices</span></span>
* <span data-ttu-id="e726f-108">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-108">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-109">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-110">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-110">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="e726f-111">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e726f-111">Az.Billing</span></span>
* <span data-ttu-id="e726f-112">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-112">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-114">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="e726f-114">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-115">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-116">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-116">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="e726f-117">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="e726f-117">Az.DataShare</span></span>
* <span data-ttu-id="e726f-118">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="e726f-118">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="e726f-119">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="e726f-119">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="e726f-120">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="e726f-120">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-121">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-121">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-122">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="e726f-122">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="e726f-123">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="e726f-123">Added optional parameters to</span></span> 
    - <span data-ttu-id="e726f-124">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e726f-124">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="e726f-125">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="e726f-125">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-126">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-126">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-127">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="e726f-127">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e726f-128">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e726f-128">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e726f-129">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-129">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="e726f-130">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="e726f-130">Az.PrivateDns</span></span>
* <span data-ttu-id="e726f-131">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e726f-131">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-132">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-132">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-133">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="e726f-133">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="e726f-134">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e726f-134">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-135">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-135">Az.Resources</span></span>
* <span data-ttu-id="e726f-136">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="e726f-136">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="e726f-137">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="e726f-137">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="e726f-138">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="e726f-138">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="e726f-139">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e726f-139">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="e726f-140">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-140">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-141">Az.Sql</span></span>
* <span data-ttu-id="e726f-142">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="e726f-142">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="e726f-143">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="e726f-143">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="e726f-144">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="e726f-144">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-145">Az.Storage</span></span>
* <span data-ttu-id="e726f-146">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-146">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="e726f-147">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-147">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="e726f-148">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="e726f-148">Highlights since the last release</span></span>
* <span data-ttu-id="e726f-149">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="e726f-149">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="e726f-150">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e726f-150">General availability of Az.Functions</span></span> 
* <span data-ttu-id="e726f-151">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="e726f-151">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-152">Az.Accounts</span></span>
* <span data-ttu-id="e726f-153">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="e726f-153">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="e726f-154">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="e726f-154">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="e726f-155">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e726f-155">Az.Aks</span></span>
* <span data-ttu-id="e726f-156">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="e726f-156">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="e726f-157">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="e726f-157">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="e726f-158">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="e726f-158">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-159">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-159">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-160">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="e726f-160">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="e726f-161">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="e726f-161">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="e726f-162">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e726f-162">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e726f-163">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e726f-163">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e726f-164">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e726f-164">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e726f-165">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e726f-165">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="e726f-166">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e726f-166">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e726f-167">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e726f-167">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e726f-168">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="e726f-168">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="e726f-169">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="e726f-169">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="e726f-170">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="e726f-170">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="e726f-171">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="e726f-171">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="e726f-172">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="e726f-172">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="e726f-173">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="e726f-173">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="e726f-174">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="e726f-174">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="e726f-175">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="e726f-175">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e726f-176">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-176">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e726f-177">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="e726f-177">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="e726f-178">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="e726f-178">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="e726f-179">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="e726f-179">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e726f-180">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e726f-180">Az.Batch</span></span>
* <span data-ttu-id="e726f-181">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="e726f-181">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="e726f-182">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="e726f-182">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="e726f-183">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="e726f-183">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="e726f-184">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="e726f-184">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="e726f-185">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="e726f-185">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="e726f-186">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="e726f-186">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="e726f-187">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="e726f-187">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="e726f-188">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="e726f-188">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="e726f-189">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="e726f-189">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-190">Az.Compute</span></span>
* <span data-ttu-id="e726f-191">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="e726f-191">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="e726f-192">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="e726f-192">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="e726f-193">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="e726f-193">Breaking changes</span></span>
    - <span data-ttu-id="e726f-194">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="e726f-194">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="e726f-195">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="e726f-195">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="e726f-196">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="e726f-196">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="e726f-197">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="e726f-197">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="e726f-198">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="e726f-198">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="e726f-199">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="e726f-199">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="e726f-200">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="e726f-200">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-201">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-201">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-202">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e726f-202">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e726f-203">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-203">Az.FrontDoor</span></span>
* <span data-ttu-id="e726f-204">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="e726f-204">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="e726f-205">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="e726f-205">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="e726f-206">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="e726f-206">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="e726f-207">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="e726f-207">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="e726f-208">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="e726f-208">Az.Functions</span></span>
* <span data-ttu-id="e726f-209">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="e726f-209">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e726f-210">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-210">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-211">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="e726f-211">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e726f-212">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e726f-212">Az.HealthcareApis</span></span>
* <span data-ttu-id="e726f-213">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="e726f-213">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-214">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-214">Az.IotHub</span></span>
* <span data-ttu-id="e726f-215">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="e726f-215">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="e726f-216">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="e726f-216">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="e726f-217">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="e726f-217">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="e726f-218">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="e726f-218">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="e726f-219">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="e726f-219">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="e726f-220">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-220">New cmdlets are:</span></span>
    - <span data-ttu-id="e726f-221">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-221">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e726f-222">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-222">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e726f-223">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-223">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="e726f-224">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-224">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="e726f-225">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="e726f-225">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="e726f-226">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="e726f-226">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-227">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-227">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-228">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="e726f-228">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="e726f-229">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="e726f-229">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="e726f-230">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="e726f-230">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="e726f-231">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="e726f-231">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="e726f-232">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="e726f-232">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="e726f-233">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="e726f-233">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="e726f-234">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="e726f-234">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-235">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-235">Az.Monitor</span></span>
* <span data-ttu-id="e726f-236">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="e726f-236">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="e726f-237">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="e726f-237">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="e726f-238">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="e726f-238">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="e726f-239">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="e726f-239">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="e726f-240">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="e726f-240">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="e726f-241">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="e726f-241">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="e726f-242">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="e726f-242">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-243">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-243">Az.Network</span></span>
* <span data-ttu-id="e726f-244">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="e726f-244">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="e726f-245">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="e726f-245">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="e726f-246">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="e726f-246">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="e726f-247">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="e726f-247">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="e726f-248">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e726f-248">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="e726f-249">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-249">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-250">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e726f-250">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e726f-251">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e726f-251">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e726f-252">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e726f-252">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="e726f-253">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="e726f-253">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="e726f-254">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="e726f-254">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="e726f-255">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="e726f-255">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="e726f-256">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="e726f-256">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="e726f-257">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="e726f-257">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="e726f-258">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="e726f-258">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="e726f-259">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="e726f-259">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="e726f-260">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="e726f-260">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="e726f-261">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e726f-261">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e726f-262">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e726f-262">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e726f-263">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e726f-263">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="e726f-264">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="e726f-264">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="e726f-265">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="e726f-265">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="e726f-266">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="e726f-266">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="e726f-267">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e726f-267">Updated cmdlet:</span></span>
        - <span data-ttu-id="e726f-268">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e726f-268">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-269">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-269">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-270">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="e726f-270">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="e726f-271">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="e726f-271">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="e726f-272">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="e726f-272">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="e726f-273">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="e726f-273">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="e726f-274">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="e726f-274">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="e726f-275">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="e726f-275">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="e726f-276">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="e726f-276">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="e726f-277">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="e726f-277">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-279">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-279">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="e726f-280">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="e726f-280">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="e726f-281">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="e726f-281">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="e726f-282">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="e726f-282">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="e726f-283">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="e726f-283">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-284">Az.Resources</span></span>
* <span data-ttu-id="e726f-285">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="e726f-285">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="e726f-286">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="e726f-286">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="e726f-287">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="e726f-287">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="e726f-288">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="e726f-288">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="e726f-289">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e726f-289">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="e726f-290">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="e726f-290">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="e726f-291">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="e726f-291">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="e726f-292">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="e726f-292">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="e726f-293">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="e726f-293">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="e726f-294">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="e726f-294">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="e726f-295">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="e726f-295">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="e726f-296">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="e726f-296">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="e726f-297">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="e726f-297">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="e726f-298">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="e726f-298">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="e726f-299">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="e726f-299">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="e726f-300">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="e726f-300">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="e726f-301">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-301">'New-AzDeployment'</span></span>
    - <span data-ttu-id="e726f-302">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-302">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="e726f-303">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-303">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e726f-304">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-304">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-305">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-305">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-306">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="e726f-306">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-307">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-307">Az.Sql</span></span>
* <span data-ttu-id="e726f-308">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="e726f-308">Enhance performance of:</span></span>
    - <span data-ttu-id="e726f-309">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e726f-309">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e726f-310">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e726f-310">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e726f-311">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e726f-311">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e726f-312">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="e726f-312">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="e726f-313">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e726f-313">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e726f-314">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e726f-314">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e726f-315">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e726f-315">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="e726f-316">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="e726f-316">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="e726f-317">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="e726f-317">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="e726f-318">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="e726f-318">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-319">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-319">Az.Storage</span></span>
* <span data-ttu-id="e726f-320">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-320">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="e726f-321">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="e726f-321">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="e726f-322">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-322">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e726f-323">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="e726f-323">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="e726f-324">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e726f-324">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="e726f-325">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="e726f-325">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="e726f-326">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="e726f-326">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="e726f-327">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="e726f-327">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="e726f-328">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="e726f-328">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="e726f-329">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="e726f-329">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="e726f-330">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="e726f-330">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="e726f-331">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="e726f-331">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="e726f-332">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="e726f-332">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="e726f-333">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-333">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="e726f-334">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-334">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="e726f-335">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-335">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e726f-336">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e726f-336">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="e726f-337">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e726f-337">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="e726f-338">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e726f-338">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e726f-339">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="e726f-339">Supported failover Storage account</span></span>
    - <span data-ttu-id="e726f-340">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="e726f-340">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="e726f-341">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-341">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="e726f-342">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-342">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="e726f-343">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="e726f-343">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="e726f-344">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e726f-344">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e726f-345">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="e726f-345">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="e726f-346">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="e726f-346">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="e726f-347">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="e726f-347">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="e726f-348">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="e726f-348">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="e726f-349">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="e726f-349">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="e726f-350">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e726f-350">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e726f-351">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e726f-351">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="e726f-352">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="e726f-352">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="e726f-353">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e726f-353">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="e726f-354">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e726f-354">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="e726f-355">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e726f-355">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="e726f-356">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="e726f-356">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="e726f-357">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="e726f-357">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="e726f-358">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="e726f-358">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e726f-359">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e726f-359">Az.TrafficManager</span></span>
* <span data-ttu-id="e726f-360">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="e726f-360">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-361">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-361">Az.Websites</span></span>
* <span data-ttu-id="e726f-362">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="e726f-362">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="e726f-363">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-363">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="e726f-364">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="e726f-364">Highlights since the last release</span></span>
* <span data-ttu-id="e726f-365">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="e726f-365">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-366">Az.Accounts</span></span>
* <span data-ttu-id="e726f-367">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="e726f-367">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-368">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-368">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-369">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e726f-369">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="e726f-370">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="e726f-370">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e726f-371">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-371">Az.Cdn</span></span>
* <span data-ttu-id="e726f-372">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="e726f-372">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-373">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-373">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-374">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="e726f-374">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-375">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-375">Az.Compute</span></span>
* <span data-ttu-id="e726f-376">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="e726f-376">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="e726f-377">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="e726f-377">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-378">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-378">Az.IotHub</span></span>
* <span data-ttu-id="e726f-379">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-379">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="e726f-380">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="e726f-380">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="e726f-381">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="e726f-381">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="e726f-382">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="e726f-382">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="e726f-383">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-383">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="e726f-384">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="e726f-384">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="e726f-385">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="e726f-385">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="e726f-386">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="e726f-386">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="e726f-387">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-387">New cmdlets are:</span></span>
    - <span data-ttu-id="e726f-388">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e726f-388">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e726f-389">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e726f-389">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e726f-390">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e726f-390">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="e726f-391">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e726f-391">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="e726f-392">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="e726f-392">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-393">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-393">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-394">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="e726f-394">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="e726f-395">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="e726f-395">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="e726f-396">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="e726f-396">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="e726f-397">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="e726f-397">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="e726f-398">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="e726f-398">Az.Maintenance</span></span>
* <span data-ttu-id="e726f-399">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="e726f-399">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-400">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-400">Az.Monitor</span></span>
* <span data-ttu-id="e726f-401">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="e726f-401">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="e726f-402">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e726f-402">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e726f-403">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e726f-403">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e726f-404">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e726f-404">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e726f-405">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="e726f-405">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="e726f-406">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e726f-406">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="e726f-407">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e726f-407">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="e726f-408">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="e726f-408">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-409">Az.Network</span></span>
* <span data-ttu-id="e726f-410">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="e726f-410">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="e726f-411">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e726f-411">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="e726f-412">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e726f-412">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="e726f-413">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="e726f-413">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="e726f-414">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="e726f-414">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="e726f-415">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="e726f-415">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="e726f-416">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="e726f-416">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="e726f-417">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="e726f-417">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="e726f-418">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="e726f-418">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="e726f-419">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-419">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="e726f-420">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="e726f-420">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="e726f-421">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="e726f-421">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="e726f-422">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="e726f-422">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="e726f-423">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="e726f-423">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="e726f-424">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-424">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="e726f-425">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-425">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-426">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-426">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-427">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="e726f-427">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="e726f-428">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="e726f-428">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-429">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-429">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-430">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="e726f-430">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-431">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-431">Az.Sql</span></span>
* <span data-ttu-id="e726f-432">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-432">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="e726f-433">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="e726f-433">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-434">Az.Storage</span></span>
* <span data-ttu-id="e726f-435">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e726f-435">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="e726f-436">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e726f-436">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="e726f-437">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-437">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="e726f-438">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-438">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="e726f-439">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="e726f-439">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="e726f-440">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e726f-440">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e726f-441">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e726f-441">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e726f-442">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="e726f-442">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="e726f-443">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e726f-443">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e726f-444">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="e726f-444">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="e726f-445">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e726f-445">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="e726f-446">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="e726f-446">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="e726f-447">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="e726f-447">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="e726f-448">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-448">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="e726f-449">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-449">General</span></span>
* <span data-ttu-id="e726f-450">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="e726f-450">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="e726f-451">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="e726f-451">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="e726f-452">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="e726f-452">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="e726f-453">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="e726f-453">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="e726f-454">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e726f-454">Az.Billing</span></span>
  - <span data-ttu-id="e726f-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-455">Az.Compute</span></span>
  - <span data-ttu-id="e726f-456">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e726f-456">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="e726f-457">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-457">Az.EventHub</span></span>
  - <span data-ttu-id="e726f-458">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-458">Az.IotHub</span></span>
  - <span data-ttu-id="e726f-459">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-459">Az.KeyVault</span></span>
  - <span data-ttu-id="e726f-460">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-460">Az.Monitor</span></span>
  - <span data-ttu-id="e726f-461">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-461">Az.Network</span></span>
  - <span data-ttu-id="e726f-462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-462">Az.Resources</span></span>
  - <span data-ttu-id="e726f-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-463">Az.Storage</span></span>
  - <span data-ttu-id="e726f-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-464">Az.Websites</span></span>
* <span data-ttu-id="e726f-465">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-465">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="e726f-466">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="e726f-466">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="e726f-467">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="e726f-467">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="e726f-468">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-468">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-469">Az.Accounts</span></span>
* <span data-ttu-id="e726f-470">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="e726f-470">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-471">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-471">Az.Compute</span></span>
* <span data-ttu-id="e726f-472">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="e726f-472">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="e726f-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="e726f-473">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="e726f-474">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="e726f-474">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="e726f-475">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="e726f-475">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="e726f-476">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="e726f-476">[#11354]</span></span>
* <span data-ttu-id="e726f-477">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="e726f-477">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="e726f-478">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e726f-478">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e726f-479">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e726f-479">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e726f-480">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e726f-480">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="e726f-481">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="e726f-481">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="e726f-482">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-482">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="e726f-483">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="e726f-483">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="e726f-484">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="e726f-484">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="e726f-485">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="e726f-485">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-486">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-487">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="e726f-487">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="e726f-488">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="e726f-488">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-489">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-490">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="e726f-490">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="e726f-491">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="e726f-491">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e726f-492">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-492">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-493">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="e726f-493">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-494">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-494">Az.IotHub</span></span>
* <span data-ttu-id="e726f-495">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e726f-495">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="e726f-496">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-496">New Cmdlets are:</span></span>
    - <span data-ttu-id="e726f-497">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="e726f-497">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="e726f-498">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="e726f-498">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-499">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-499">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-500">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="e726f-500">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-501">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-501">Az.Monitor</span></span>
* <span data-ttu-id="e726f-502">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="e726f-502">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-503">Az.Network</span></span>
* <span data-ttu-id="e726f-504">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="e726f-504">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="e726f-505">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e726f-505">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e726f-506">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="e726f-506">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="e726f-507">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="e726f-507">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="e726f-508">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="e726f-508">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="e726f-509">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="e726f-509">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-510">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-510">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-511">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="e726f-511">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-512">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-512">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-513">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="e726f-513">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="e726f-514">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="e726f-514">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="e726f-515">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="e726f-515">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="e726f-516">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="e726f-516">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="e726f-517">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="e726f-517">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="e726f-518">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="e726f-518">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-519">Az.Resources</span></span>
* <span data-ttu-id="e726f-520">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="e726f-520">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="e726f-521">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="e726f-521">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="e726f-522">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="e726f-522">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="e726f-523">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="e726f-523">Added example.</span></span>
* <span data-ttu-id="e726f-524">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="e726f-524">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="e726f-525">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="e726f-525">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-526">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-526">Az.Sql</span></span>
* <span data-ttu-id="e726f-527">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="e726f-527">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="e726f-528">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-528">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="e726f-529">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e726f-529">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="e726f-530">Az.Support</span><span class="sxs-lookup"><span data-stu-id="e726f-530">Az.Support</span></span>
* <span data-ttu-id="e726f-531">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="e726f-531">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-532">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-532">Az.Websites</span></span>
* <span data-ttu-id="e726f-533">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="e726f-533">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="e726f-534">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e726f-534">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e726f-535">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e726f-535">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e726f-536">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e726f-536">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="e726f-537">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="e726f-537">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="e726f-538">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-538">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-539">Az.Accounts</span></span>
* <span data-ttu-id="e726f-540">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="e726f-540">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="e726f-541">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="e726f-541">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="e726f-542">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="e726f-542">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-543">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-543">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-544">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="e726f-544">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="e726f-545">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="e726f-545">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="e726f-546">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="e726f-546">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="e726f-547">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="e726f-547">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-548">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-548">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-549">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="e726f-549">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-550">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-550">Az.IotHub</span></span>
* <span data-ttu-id="e726f-551">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e726f-551">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="e726f-552">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-552">New Cmdlets are:</span></span>
    - <span data-ttu-id="e726f-553">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-553">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e726f-554">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-554">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e726f-555">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-555">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e726f-556">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-556">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="e726f-557">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e726f-557">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="e726f-558">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-558">New Cmdlets are:</span></span>
    - <span data-ttu-id="e726f-559">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e726f-559">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="e726f-560">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e726f-560">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="e726f-561">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e726f-561">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="e726f-562">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="e726f-562">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="e726f-563">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e726f-563">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="e726f-564">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e726f-564">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="e726f-565">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="e726f-565">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="e726f-566">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-566">New Cmdlets are:</span></span>
    - <span data-ttu-id="e726f-567">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="e726f-567">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="e726f-568">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="e726f-568">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="e726f-569">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e726f-569">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-570">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-570">Az.Monitor</span></span>
* <span data-ttu-id="e726f-571">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="e726f-571">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-572">Az.Network</span></span>
* <span data-ttu-id="e726f-573">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="e726f-573">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="e726f-574">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="e726f-574">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="e726f-575">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="e726f-575">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="e726f-576">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="e726f-576">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-577">Az.Resources</span></span>
* <span data-ttu-id="e726f-578">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="e726f-578">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="e726f-579">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="e726f-579">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="e726f-580">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="e726f-580">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="e726f-581">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="e726f-581">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="e726f-582">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="e726f-582">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="e726f-583">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="e726f-583">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="e726f-584">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="e726f-584">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="e726f-585">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e726f-585">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="e726f-586">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e726f-586">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="e726f-587">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e726f-587">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="e726f-588">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e726f-588">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="e726f-589">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-589">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="e726f-590">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="e726f-590">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="e726f-591">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="e726f-591">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-592">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-592">Az.Sql</span></span>
* <span data-ttu-id="e726f-593">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="e726f-593">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="e726f-594">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="e726f-594">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="e726f-595">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="e726f-595">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="e726f-596">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="e726f-596">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="e726f-597">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="e726f-597">Remove an LTR backup</span></span>
    - <span data-ttu-id="e726f-598">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="e726f-598">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="e726f-599">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e726f-599">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="e726f-600">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-600">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="e726f-601">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-601">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-602">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-602">Az.Storage</span></span>
* <span data-ttu-id="e726f-603">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-603">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="e726f-604">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="e726f-604">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="e726f-605">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e726f-605">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="e726f-606">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="e726f-606">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="e726f-607">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="e726f-607">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-608">Az.Websites</span></span>
* <span data-ttu-id="e726f-609">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="e726f-609">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="e726f-610">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="e726f-610">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="e726f-611">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e726f-611">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="e726f-612">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="e726f-612">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="e726f-613">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e726f-613">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="e726f-614">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-614">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e726f-615">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e726f-615">Highlights since the last major release</span></span>
* <span data-ttu-id="e726f-616">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="e726f-616">Updated client side telemetry.</span></span>
* <span data-ttu-id="e726f-617">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e726f-617">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="e726f-618">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e726f-618">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-619">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-619">Az.Accounts</span></span>
* <span data-ttu-id="e726f-620">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="e726f-620">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-621">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-621">Az.Automation</span></span>
* <span data-ttu-id="e726f-622">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="e726f-622">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-623">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-623">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-624">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="e726f-624">Updated SDK to 7.0</span></span>
* <span data-ttu-id="e726f-625">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="e726f-625">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-626">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-626">Az.Compute</span></span>
* <span data-ttu-id="e726f-627">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="e726f-627">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e726f-628">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-628">Az.FrontDoor</span></span>
* <span data-ttu-id="e726f-629">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="e726f-629">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-630">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-630">Az.IotHub</span></span>
* <span data-ttu-id="e726f-631">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="e726f-631">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="e726f-632">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-632">New Cmdlets are:</span></span>
    - <span data-ttu-id="e726f-633">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-633">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e726f-634">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-634">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e726f-635">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-635">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="e726f-636">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="e726f-636">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-637">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-638">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="e726f-638">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-639">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-639">Az.Monitor</span></span>
* <span data-ttu-id="e726f-640">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="e726f-640">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="e726f-641">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="e726f-641">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="e726f-642">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="e726f-642">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-643">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-643">Az.Network</span></span>
* <span data-ttu-id="e726f-644">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="e726f-644">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="e726f-645">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="e726f-645">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="e726f-646">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="e726f-646">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="e726f-647">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="e726f-647">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="e726f-648">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="e726f-648">No new cmdlets are added.</span></span> <span data-ttu-id="e726f-649">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="e726f-649">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-651">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="e726f-651">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-652">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-652">Az.Resources</span></span>
* <span data-ttu-id="e726f-653">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="e726f-653">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="e726f-654">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e726f-654">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="e726f-655">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e726f-655">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="e726f-656">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="e726f-656">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="e726f-657">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e726f-657">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="e726f-658">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="e726f-658">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="e726f-659">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="e726f-659">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="e726f-660">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-660">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-661">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-661">Az.Sql</span></span>
* <span data-ttu-id="e726f-662">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="e726f-662">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="e726f-663">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="e726f-663">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="e726f-664">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e726f-664">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="e726f-665">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e726f-665">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="e726f-666">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="e726f-666">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e726f-667">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e726f-667">Az.StorageSync</span></span>
* <span data-ttu-id="e726f-668">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="e726f-668">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="e726f-669">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-669">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e726f-670">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e726f-670">Highlights since the last major release</span></span>
* <span data-ttu-id="e726f-671">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e726f-671">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="e726f-672">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-672">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-673">Az.Accounts</span></span>
* <span data-ttu-id="e726f-674">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="e726f-674">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="e726f-675">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="e726f-675">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-676">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-676">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-677">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="e726f-677">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="e726f-678">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="e726f-678">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="e726f-679">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="e726f-679">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="e726f-680">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="e726f-680">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-681">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-681">Az.Compute</span></span>
* <span data-ttu-id="e726f-682">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="e726f-682">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="e726f-683">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e726f-683">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="e726f-684">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e726f-684">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="e726f-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-685">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="e726f-686">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="e726f-686">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-687">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-688">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="e726f-688">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e726f-689">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e726f-689">Az.DeploymentManager</span></span>
* <span data-ttu-id="e726f-690">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="e726f-690">Adds LIST operations for resources</span></span>
* <span data-ttu-id="e726f-691">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="e726f-691">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e726f-692">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-692">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-693">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="e726f-693">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-694">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-694">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-695">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="e726f-695">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-696">Az.Network</span></span>
* <span data-ttu-id="e726f-697">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="e726f-697">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="e726f-698">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e726f-698">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="e726f-699">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="e726f-699">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e726f-700">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="e726f-700">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="e726f-701">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="e726f-701">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="e726f-702">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="e726f-702">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="e726f-703">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="e726f-703">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="e726f-704">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e726f-704">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="e726f-705">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-705">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-706">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="e726f-707">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-707">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="e726f-708">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e726f-708">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="e726f-709">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="e726f-709">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-710">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-710">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-711">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="e726f-711">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="e726f-712">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="e726f-712">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="e726f-713">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="e726f-713">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="e726f-714">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="e726f-714">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-715">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-715">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-716">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="e726f-716">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="e726f-717">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="e726f-717">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-718">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-718">Az.Resources</span></span>
* <span data-ttu-id="e726f-719">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="e726f-719">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="e726f-720">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="e726f-720">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-721">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-721">Az.Sql</span></span>
<span data-ttu-id="e726f-722">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="e726f-722">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-723">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-723">Az.Storage</span></span>
* <span data-ttu-id="e726f-724">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e726f-724">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="e726f-725">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-725">New-AzStorageAccount</span></span>
* <span data-ttu-id="e726f-726">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="e726f-726">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="e726f-727">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e726f-727">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-728">Az.Websites</span></span>
* <span data-ttu-id="e726f-729">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="e726f-729">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="e726f-730">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="e726f-730">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="e726f-731">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e726f-731">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-732">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-732">Az.Accounts</span></span>
* <span data-ttu-id="e726f-733">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e726f-733">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e726f-734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-734">Az.Cdn</span></span>
* <span data-ttu-id="e726f-735">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e726f-735">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-736">Az.Compute</span></span>
* <span data-ttu-id="e726f-737">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="e726f-737">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e726f-738">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-738">Az.ContainerInstance</span></span>
* <span data-ttu-id="e726f-739">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-739">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e726f-740">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e726f-740">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e726f-741">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e726f-741">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e726f-742">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e726f-742">Get the Edge Storage Container</span></span>
* <span data-ttu-id="e726f-743">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e726f-743">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e726f-744">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e726f-744">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="e726f-745">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e726f-745">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e726f-746">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e726f-746">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="e726f-747">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="e726f-747">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="e726f-748">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e726f-748">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="e726f-749">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-749">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e726f-750">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e726f-750">Get the Edge Storage Account</span></span>
* <span data-ttu-id="e726f-751">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-751">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e726f-752">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e726f-752">Create new Edge Storage Account</span></span>
* <span data-ttu-id="e726f-753">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="e726f-753">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="e726f-754">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="e726f-754">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="e726f-755">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="e726f-755">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="e726f-756">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="e726f-756">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="e726f-757">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="e726f-757">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="e726f-758">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="e726f-758">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-759">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-760">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e726f-760">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="e726f-761">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="e726f-761">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="e726f-762">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="e726f-762">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="e726f-763">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="e726f-763">Az.DevTestLabs</span></span>
* <span data-ttu-id="e726f-764">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="e726f-764">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e726f-765">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-765">Az.EventHub</span></span>
* <span data-ttu-id="e726f-766">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="e726f-766">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e726f-767">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-767">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-768">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="e726f-768">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e726f-769">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e726f-769">Az.MachineLearning</span></span>
* <span data-ttu-id="e726f-770">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="e726f-770">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="e726f-771">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e726f-771">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="e726f-772">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="e726f-772">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="e726f-773">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e726f-773">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="e726f-774">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e726f-774">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="e726f-775">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e726f-775">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="e726f-776">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="e726f-776">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="e726f-777">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="e726f-777">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-778">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-778">Az.Network</span></span>
* <span data-ttu-id="e726f-779">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="e726f-779">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-780">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-780">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-781">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-781">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="e726f-782">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-782">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e726f-783">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-783">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="e726f-784">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-784">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-785">Az.Resources</span></span>
* <span data-ttu-id="e726f-786">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="e726f-786">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-787">Az.Sql</span></span>
* <span data-ttu-id="e726f-788">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="e726f-788">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="e726f-789">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="e726f-789">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="e726f-790">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e726f-790">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="e726f-791">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="e726f-791">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-792">Az.Storage</span></span>
* <span data-ttu-id="e726f-793">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="e726f-793">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="e726f-794">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-794">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="e726f-795">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="e726f-795">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="e726f-796">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-796">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="e726f-797">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-797">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="e726f-798">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-798">General</span></span>
* <span data-ttu-id="e726f-799">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="e726f-799">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-800">Az.Accounts</span></span>
* <span data-ttu-id="e726f-801">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="e726f-801">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="e726f-802">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="e726f-802">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e726f-803">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e726f-803">Az.Batch</span></span>
* <span data-ttu-id="e726f-804">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="e726f-804">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-805">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-805">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-806">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="e726f-806">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e726f-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-807">Az.FrontDoor</span></span>
* <span data-ttu-id="e726f-808">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="e726f-808">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="e726f-809">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="e726f-809">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e726f-810">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e726f-810">Az.HealthcareApis</span></span>
* <span data-ttu-id="e726f-811">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="e726f-811">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-812">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-812">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-813">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="e726f-813">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="e726f-814">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="e726f-814">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="e726f-815">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="e726f-815">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-816">Az.Monitor</span></span>
* <span data-ttu-id="e726f-817">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e726f-817">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="e726f-818">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="e726f-818">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="e726f-819">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="e726f-819">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-820">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-820">Az.Network</span></span>
* <span data-ttu-id="e726f-821">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="e726f-821">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-822">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-822">Az.Resources</span></span>
* <span data-ttu-id="e726f-823">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="e726f-823">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="e726f-824">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="e726f-824">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-825">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-825">Az.Sql</span></span>
* <span data-ttu-id="e726f-826">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="e726f-826">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-827">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-827">Az.Storage</span></span>
* <span data-ttu-id="e726f-828">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="e726f-828">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="e726f-829">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="e726f-829">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="e726f-830">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e726f-830">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="e726f-831">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="e726f-831">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="e726f-832">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="e726f-832">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="e726f-833">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="e726f-833">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="e726f-834">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="e726f-834">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="e726f-835">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e726f-835">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="e726f-836">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e726f-836">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="e726f-837">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="e726f-837">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="e726f-838">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e726f-838">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="e726f-839">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="e726f-839">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="e726f-840">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="e726f-840">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="e726f-841">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-841">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e726f-842">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e726f-842">Highlights since the last major release</span></span>
* <span data-ttu-id="e726f-843">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="e726f-843">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="e726f-844">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="e726f-844">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-845">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-845">Az.Compute</span></span>
* <span data-ttu-id="e726f-846">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="e726f-846">VM Reapply feature</span></span>
    - <span data-ttu-id="e726f-847">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="e726f-847">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="e726f-848">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="e726f-848">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="e726f-849">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-849">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="e726f-850">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e726f-850">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="e726f-851">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-851">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e726f-852">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="e726f-852">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="e726f-853">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="e726f-853">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="e726f-854">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e726f-854">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="e726f-855">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e726f-855">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="e726f-856">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-856">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="e726f-857">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="e726f-857">Az.DataBoxEdge</span></span>
* <span data-ttu-id="e726f-858">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-858">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e726f-859">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="e726f-859">Get the Order</span></span>
* <span data-ttu-id="e726f-860">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-860">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e726f-861">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="e726f-861">Create new Order</span></span>
* <span data-ttu-id="e726f-862">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-862">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="e726f-863">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="e726f-863">Remove the Order</span></span>
* <span data-ttu-id="e726f-864">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="e726f-864">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="e726f-865">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="e726f-865">Now creates Local Share</span></span>
* <span data-ttu-id="e726f-866">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-866">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="e726f-867">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="e726f-867">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="e726f-868">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-868">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="e726f-869">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="e726f-869">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="e726f-870">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-870">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e726f-871">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="e726f-871">Gets the information about Triggers</span></span>
* <span data-ttu-id="e726f-872">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-872">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e726f-873">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="e726f-873">Create new Triggers</span></span>
* <span data-ttu-id="e726f-874">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-874">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="e726f-875">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="e726f-875">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-876">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-876">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-877">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="e726f-877">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="e726f-878">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="e726f-878">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-879">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-879">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-880">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="e726f-880">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e726f-881">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-881">Az.EventHub</span></span>
* <span data-ttu-id="e726f-882">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="e726f-882">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e726f-883">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-883">Az.FrontDoor</span></span>
* <span data-ttu-id="e726f-884">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e726f-884">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="e726f-885">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="e726f-885">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="e726f-886">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="e726f-886">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="e726f-887">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="e726f-887">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-888">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-888">Az.Network</span></span>
* <span data-ttu-id="e726f-889">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="e726f-889">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="e726f-890">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="e726f-890">Az.PrivateDns</span></span>
* <span data-ttu-id="e726f-891">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e726f-891">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-892">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-892">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-893">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="e726f-893">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="e726f-894">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="e726f-894">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="e726f-895">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="e726f-895">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e726f-896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e726f-896">Az.RedisCache</span></span>
* <span data-ttu-id="e726f-897">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="e726f-897">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="e726f-898">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="e726f-898">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="e726f-899">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="e726f-899">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-900">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-900">Az.Resources</span></span>
- <span data-ttu-id="e726f-901">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="e726f-901">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="e726f-902">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="e726f-902">Updated create policy definition help example</span></span>
- <span data-ttu-id="e726f-903">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="e726f-903">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="e726f-904">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e726f-904">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="e726f-905">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="e726f-905">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-906">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-906">Az.Sql</span></span>
* <span data-ttu-id="e726f-907">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="e726f-907">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="e726f-908">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="e726f-908">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="e726f-909">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-909">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="e726f-910">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-910">General</span></span>
* <span data-ttu-id="e726f-911">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="e726f-911">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-912">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-912">Az.Accounts</span></span>
* <span data-ttu-id="e726f-913">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="e726f-913">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e726f-914">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e726f-914">Az.Advisor</span></span>
* <span data-ttu-id="e726f-915">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e726f-915">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e726f-916">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e726f-916">Az.Batch</span></span>
* <span data-ttu-id="e726f-917">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="e726f-917">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="e726f-918">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="e726f-918">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="e726f-919">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="e726f-919">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="e726f-920">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="e726f-920">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="e726f-921">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="e726f-921">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="e726f-922">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="e726f-922">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="e726f-923">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="e726f-923">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="e726f-924">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="e726f-924">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="e726f-925">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="e726f-925">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="e726f-926">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="e726f-926">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e726f-927">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="e726f-927">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="e726f-928">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="e726f-928">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="e726f-929">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="e726f-929">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="e726f-930">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="e726f-930">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="e726f-931">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="e726f-931">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="e726f-932">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="e726f-932">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="e726f-933">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="e726f-933">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="e726f-934">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="e726f-934">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="e726f-935">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="e726f-935">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="e726f-936">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="e726f-936">This operation is no longer supported.</span></span>
* <span data-ttu-id="e726f-937">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="e726f-937">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e726f-938">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="e726f-938">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="e726f-939">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="e726f-939">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="e726f-940">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="e726f-940">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="e726f-941">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="e726f-941">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="e726f-942">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="e726f-942">New non-verified images are also now returned.</span></span> <span data-ttu-id="e726f-943">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="e726f-943">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="e726f-944">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="e726f-944">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="e726f-945">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="e726f-945">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="e726f-946">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="e726f-946">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="e726f-947">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="e726f-947">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="e726f-948">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="e726f-948">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="e726f-949">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="e726f-949">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="e726f-950">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e726f-950">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="e726f-951">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="e726f-951">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="e726f-952">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="e726f-952">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e726f-953">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-953">Az.Cdn</span></span>
* <span data-ttu-id="e726f-954">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="e726f-954">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="e726f-955">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="e726f-955">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-956">Az.Compute</span></span>
* <span data-ttu-id="e726f-957">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="e726f-957">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="e726f-958">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e726f-958">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="e726f-959">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e726f-959">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="e726f-960">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-960">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e726f-961">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-961">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="e726f-962">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="e726f-962">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="e726f-963">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-963">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="e726f-964">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="e726f-964">Breaking changes</span></span>
    - <span data-ttu-id="e726f-965">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="e726f-965">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="e726f-966">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="e726f-966">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-967">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-967">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-968">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="e726f-968">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-969">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-969">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-970">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="e726f-970">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="e726f-971">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="e726f-971">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="e726f-972">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="e726f-972">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="e726f-973">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="e726f-973">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="e726f-974">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="e726f-974">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="e726f-975">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="e726f-975">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e726f-976">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-976">Az.FrontDoor</span></span>
* <span data-ttu-id="e726f-977">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="e726f-977">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e726f-978">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-978">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-979">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="e726f-979">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="e726f-980">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e726f-980">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="e726f-981">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="e726f-981">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="e726f-982">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="e726f-982">Removed five cmdlets:</span></span>
    - <span data-ttu-id="e726f-983">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e726f-983">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e726f-984">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e726f-984">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e726f-985">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="e726f-985">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="e726f-986">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e726f-986">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="e726f-987">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e726f-987">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="e726f-988">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-988">Added three cmdlets:</span></span>
    - <span data-ttu-id="e726f-989">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="e726f-989">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e726f-990">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="e726f-990">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="e726f-991">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="e726f-991">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="e726f-992">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="e726f-992">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="e726f-993">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="e726f-993">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="e726f-994">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="e726f-994">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="e726f-995">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="e726f-995">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="e726f-996">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e726f-996">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="e726f-997">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="e726f-997">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="e726f-998">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="e726f-998">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="e726f-999">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="e726f-999">Added some scenario test cases.</span></span>
* <span data-ttu-id="e726f-1000">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1000">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-1001">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1001">Az.IotHub</span></span>
* <span data-ttu-id="e726f-1002">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="e726f-1002">Breaking changes:</span></span>
    - <span data-ttu-id="e726f-1003">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e726f-1003">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e726f-1004">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e726f-1004">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e726f-1005">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e726f-1005">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e726f-1006">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e726f-1006">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e726f-1007">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="e726f-1007">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="e726f-1008">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="e726f-1008">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="e726f-1009">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1009">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="e726f-1010">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1010">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="e726f-1011">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e726f-1011">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e726f-1012">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e726f-1012">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="e726f-1013">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="e726f-1013">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="e726f-1014">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="e726f-1014">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1015">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1015">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1016">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1016">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="e726f-1017">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1017">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="e726f-1018">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1018">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="e726f-1019">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1019">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="e726f-1020">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1020">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="e726f-1021">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1021">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="e726f-1022">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1022">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="e726f-1023">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1023">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="e726f-1024">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="e726f-1024">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1025">Az.Resources</span></span>
* <span data-ttu-id="e726f-1026">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="e726f-1026">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1027">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1027">Az.Network</span></span>
* <span data-ttu-id="e726f-1028">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="e726f-1028">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="e726f-1029">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e726f-1029">Updated cmdlet:</span></span>
        - <span data-ttu-id="e726f-1030">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1030">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1031">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1031">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1032">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1032">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1033">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1033">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1034">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1034">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e726f-1035">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="e726f-1035">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="e726f-1036">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e726f-1036">New cmdlet:</span></span>
        - <span data-ttu-id="e726f-1037">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="e726f-1037">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="e726f-1038">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="e726f-1038">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="e726f-1039">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e726f-1039">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="e726f-1040">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1040">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="e726f-1041">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="e726f-1041">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="e726f-1042">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="e726f-1042">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="e726f-1043">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1043">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="e726f-1044">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1044">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="e726f-1045">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-1045">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-1046">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="e726f-1046">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="e726f-1047">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e726f-1047">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e726f-1048">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e726f-1048">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e726f-1049">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="e726f-1049">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="e726f-1050">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1050">Set-AzVirtualHub</span></span>
* <span data-ttu-id="e726f-1051">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="e726f-1051">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="e726f-1052">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e726f-1052">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e726f-1053">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1053">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e726f-1054">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1054">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="e726f-1055">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1055">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="e726f-1056">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1056">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="e726f-1057">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1057">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="e726f-1058">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-1058">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-1059">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1059">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="e726f-1060">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e726f-1060">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e726f-1061">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1061">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e726f-1062">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1062">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e726f-1063">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1063">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e726f-1064">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1064">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="e726f-1065">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-1065">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="e726f-1066">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="e726f-1066">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="e726f-1067">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-1067">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-1068">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="e726f-1068">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="e726f-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="e726f-1069">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="e726f-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e726f-1070">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="e726f-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e726f-1071">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="e726f-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="e726f-1072">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="e726f-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-1073">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="e726f-1074">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e726f-1074">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e726f-1075">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-1075">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="e726f-1076">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="e726f-1076">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="e726f-1077">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="e726f-1077">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="e726f-1078">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="e726f-1078">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="e726f-1079">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="e726f-1079">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="e726f-1080">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-1080">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="e726f-1081">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-1081">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="e726f-1082">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="e726f-1082">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="e726f-1083">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1083">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="e726f-1084">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1084">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="e726f-1085">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-1085">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-1086">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1086">New-AzIpGroup</span></span>
        - <span data-ttu-id="e726f-1087">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1087">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="e726f-1088">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1088">Get-AzIpGroup</span></span>
        - <span data-ttu-id="e726f-1089">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1089">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-1090">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-1090">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-1091">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="e726f-1091">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1092">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1092">Az.Sql</span></span>
* <span data-ttu-id="e726f-1093">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="e726f-1093">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="e726f-1094">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="e726f-1094">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="e726f-1095">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="e726f-1095">Removed deprecated aliases:</span></span>
* <span data-ttu-id="e726f-1096">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="e726f-1096">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="e726f-1097">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="e726f-1097">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="e726f-1098">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-1098">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e726f-1099">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="e726f-1099">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="e726f-1100">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="e726f-1100">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="e726f-1101">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e726f-1101">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1102">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1102">Az.Storage</span></span>
* <span data-ttu-id="e726f-1103">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e726f-1103">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="e726f-1104">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1104">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e726f-1105">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1105">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e726f-1106">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="e726f-1106">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="e726f-1107">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e726f-1107">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="e726f-1108">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e726f-1108">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="e726f-1109">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1109">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="e726f-1110">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-1110">General</span></span>
* <span data-ttu-id="e726f-1111">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e726f-1111">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-1112">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1112">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1113">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="e726f-1113">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-1114">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-1114">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-1115">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e726f-1115">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="e726f-1116">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="e726f-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-1117">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1117">Az.Automation</span></span>
* <span data-ttu-id="e726f-1118">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="e726f-1118">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e726f-1119">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e726f-1119">Az.Batch</span></span>
* <span data-ttu-id="e726f-1120">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="e726f-1120">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1121">Az.Compute</span></span>
* <span data-ttu-id="e726f-1122">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-1122">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="e726f-1123">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e726f-1123">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="e726f-1124">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="e726f-1124">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="e726f-1125">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="e726f-1125">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-1126">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-1126">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-1127">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="e726f-1127">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="e726f-1128">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="e726f-1128">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="e726f-1129">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="e726f-1129">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-1130">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-1130">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-1131">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="e726f-1131">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="e726f-1132">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="e726f-1132">Az.HealthcareApis</span></span>
* <span data-ttu-id="e726f-1133">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="e726f-1133">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="e726f-1134">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="e726f-1134">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="e726f-1135">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="e726f-1135">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="e726f-1136">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="e726f-1136">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-1137">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1137">Az.IotHub</span></span>
* <span data-ttu-id="e726f-1138">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="e726f-1138">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="e726f-1139">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="e726f-1139">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-1140">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-1140">Az.Monitor</span></span>
* <span data-ttu-id="e726f-1141">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="e726f-1141">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="e726f-1142">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="e726f-1142">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="e726f-1143">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="e726f-1143">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="e726f-1144">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e726f-1144">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1145">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1145">Az.Network</span></span>
* <span data-ttu-id="e726f-1146">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="e726f-1146">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="e726f-1147">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="e726f-1147">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="e726f-1148">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-1148">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-1149">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-1149">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="e726f-1150">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1150">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e726f-1151">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="e726f-1151">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="e726f-1152">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="e726f-1152">Updated cmdlets:</span></span>
        - <span data-ttu-id="e726f-1153">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1153">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e726f-1154">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1154">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e726f-1155">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1155">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e726f-1156">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="e726f-1156">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="e726f-1157">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="e726f-1157">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="e726f-1158">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="e726f-1158">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="e726f-1159">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="e726f-1159">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e726f-1160">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e726f-1160">Az.RedisCache</span></span>
* <span data-ttu-id="e726f-1161">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="e726f-1161">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1162">Az.Sql</span></span>
* <span data-ttu-id="e726f-1163">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="e726f-1163">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1164">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1164">Az.Storage</span></span>
* <span data-ttu-id="e726f-1165">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="e726f-1165">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="e726f-1166">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="e726f-1166">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e726f-1167">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e726f-1167">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="e726f-1168">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="e726f-1168">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="e726f-1169">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1169">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e726f-1170">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e726f-1170">Az.StorageSync</span></span>
* <span data-ttu-id="e726f-1171">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="e726f-1171">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1172">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1172">Az.Websites</span></span>
* <span data-ttu-id="e726f-1173">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="e726f-1173">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="e726f-1174">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1174">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e726f-1175">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-1175">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-1176">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="e726f-1176">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="e726f-1177">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="e726f-1177">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="e726f-1178">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1178">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-1179">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1179">Az.Automation</span></span>
* <span data-ttu-id="e726f-1180">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="e726f-1180">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="e726f-1181">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="e726f-1181">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="e726f-1182">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="e726f-1182">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1183">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1183">Az.Compute</span></span>
* <span data-ttu-id="e726f-1184">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1184">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="e726f-1185">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1185">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e726f-1186">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="e726f-1186">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="e726f-1187">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="e726f-1187">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="e726f-1188">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e726f-1188">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="e726f-1189">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="e726f-1189">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="e726f-1190">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="e726f-1190">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="e726f-1191">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="e726f-1191">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="e726f-1192">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e726f-1192">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-1193">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-1193">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-1194">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="e726f-1194">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="e726f-1195">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="e726f-1195">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e726f-1196">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-1196">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-1197">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="e726f-1197">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-1198">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1198">Az.IotHub</span></span>
* <span data-ttu-id="e726f-1199">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="e726f-1199">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="e726f-1200">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="e726f-1200">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="e726f-1201">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="e726f-1201">New cmdlets are:</span></span>
    - <span data-ttu-id="e726f-1202">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e726f-1202">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e726f-1203">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e726f-1203">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e726f-1204">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e726f-1204">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="e726f-1205">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="e726f-1205">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-1206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-1206">Az.Monitor</span></span>
* <span data-ttu-id="e726f-1207">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="e726f-1207">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="e726f-1208">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="e726f-1208">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="e726f-1209">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="e726f-1209">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="e726f-1210">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="e726f-1210">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="e726f-1211">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="e726f-1211">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="e726f-1212">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="e726f-1212">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="e726f-1213">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e726f-1213">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="e726f-1214">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="e726f-1214">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="e726f-1215">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="e726f-1215">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e726f-1216">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="e726f-1216">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="e726f-1217">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="e726f-1217">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="e726f-1218">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="e726f-1218">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="e726f-1219">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="e726f-1219">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="e726f-1220">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="e726f-1220">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="e726f-1221">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="e726f-1221">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="e726f-1222">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="e726f-1222">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="e726f-1223">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="e726f-1223">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="e726f-1224">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-1224">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="e726f-1225">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="e726f-1225">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="e726f-1226">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-1226">Overall improved help files</span></span>
* <span data-ttu-id="e726f-1227">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="e726f-1227">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1228">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1228">Az.Network</span></span>
* <span data-ttu-id="e726f-1229">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="e726f-1229">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="e726f-1230">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="e726f-1230">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="e726f-1231">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="e726f-1231">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="e726f-1232">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="e726f-1232">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="e726f-1233">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="e726f-1233">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="e726f-1234">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="e726f-1234">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="e726f-1235">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="e726f-1235">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="e726f-1236">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e726f-1236">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="e726f-1237">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-1237">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="e726f-1238">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="e726f-1238">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="e726f-1239">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1239">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="e726f-1240">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="e726f-1240">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="e726f-1241">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e726f-1241">New cmdlets</span></span>
        - <span data-ttu-id="e726f-1242">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="e726f-1242">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="e726f-1243">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1243">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="e726f-1244">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e726f-1244">Updated cmdlet:</span></span>
        - <span data-ttu-id="e726f-1245">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e726f-1245">New-VpnSite</span></span>
        - <span data-ttu-id="e726f-1246">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="e726f-1246">Update-VpnSite</span></span>
        - <span data-ttu-id="e726f-1247">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1247">New-VpnConnection</span></span>
        - <span data-ttu-id="e726f-1248">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1248">Update-VpnConnection</span></span>
* <span data-ttu-id="e726f-1249">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="e726f-1249">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1250">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1250">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1251">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="e726f-1251">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="e726f-1252">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="e726f-1252">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1253">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1253">Az.Resources</span></span>
* <span data-ttu-id="e726f-1254">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="e726f-1254">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-1255">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-1255">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-1256">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="e726f-1256">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="e726f-1257">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="e726f-1257">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="e726f-1258">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e726f-1258">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e726f-1259">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e726f-1259">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e726f-1260">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e726f-1260">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e726f-1261">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e726f-1261">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="e726f-1262">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e726f-1262">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e726f-1263">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e726f-1263">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e726f-1264">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e726f-1264">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e726f-1265">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e726f-1265">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e726f-1266">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e726f-1266">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="e726f-1267">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e726f-1267">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="e726f-1268">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e726f-1268">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="e726f-1269">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e726f-1269">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="e726f-1270">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="e726f-1270">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="e726f-1271">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e726f-1271">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e726f-1272">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e726f-1272">Az.SignalR</span></span>
* <span data-ttu-id="e726f-1273">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="e726f-1273">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1274">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1274">Az.Sql</span></span>
* <span data-ttu-id="e726f-1275">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="e726f-1275">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="e726f-1276">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="e726f-1276">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="e726f-1277">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-1277">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="e726f-1278">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e726f-1278">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="e726f-1279">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="e726f-1279">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1280">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1280">Az.Storage</span></span>
* <span data-ttu-id="e726f-1281">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="e726f-1281">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="e726f-1282">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="e726f-1282">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="e726f-1283">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e726f-1283">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="e726f-1284">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e726f-1284">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="e726f-1285">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="e726f-1285">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="e726f-1286">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e726f-1286">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="e726f-1287">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e726f-1287">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="e726f-1288">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e726f-1288">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e726f-1289">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e726f-1289">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e726f-1290">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e726f-1290">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="e726f-1291">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e726f-1291">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1292">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1292">Az.Websites</span></span>
* <span data-ttu-id="e726f-1293">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="e726f-1293">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="e726f-1294">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="e726f-1294">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="e726f-1295">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="e726f-1295">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="e726f-1296">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1296">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="e726f-1297">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-1297">General</span></span>
* <span data-ttu-id="e726f-1298">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="e726f-1298">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-1299">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1299">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1300">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="e726f-1300">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="e726f-1301">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e726f-1301">Az.Aks</span></span>
* <span data-ttu-id="e726f-1302">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="e726f-1302">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="e726f-1303">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="e726f-1303">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-1304">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-1304">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-1305">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="e726f-1305">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="e726f-1306">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="e726f-1306">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="e726f-1307">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="e726f-1307">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="e726f-1308">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="e726f-1308">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="e726f-1309">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e726f-1309">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e726f-1310">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e726f-1310">Az.Batch</span></span>
* <span data-ttu-id="e726f-1311">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="e726f-1311">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e726f-1312">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-1312">Az.Cdn</span></span>
* <span data-ttu-id="e726f-1313">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="e726f-1313">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1314">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1314">Az.Compute</span></span>
* <span data-ttu-id="e726f-1315">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1315">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="e726f-1316">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-1316">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="e726f-1317">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="e726f-1317">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="e726f-1318">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1318">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="e726f-1319">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="e726f-1319">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="e726f-1320">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e726f-1320">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="e726f-1321">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="e726f-1321">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="e726f-1322">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="e726f-1322">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-1323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-1323">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-1324">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="e726f-1324">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="e726f-1325">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="e726f-1325">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="e726f-1326">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="e726f-1326">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="e726f-1327">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="e726f-1327">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-1328">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-1328">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-1329">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="e726f-1329">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e726f-1330">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1330">Az.EventHub</span></span>
* <span data-ttu-id="e726f-1331">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-1331">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="e726f-1332">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="e726f-1332">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="e726f-1333">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e726f-1333">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="e726f-1334">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="e726f-1334">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="e726f-1335">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e726f-1335">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e726f-1336">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="e726f-1336">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-1337">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-1337">Az.Monitor</span></span>
* <span data-ttu-id="e726f-1338">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-1338">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1339">Az.Network</span></span>
* <span data-ttu-id="e726f-1340">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1340">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="e726f-1341">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="e726f-1341">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="e726f-1342">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="e726f-1342">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="e726f-1343">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="e726f-1343">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="e726f-1344">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="e726f-1344">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="e726f-1345">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e726f-1345">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="e726f-1346">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e726f-1346">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-1347">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1347">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-1348">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="e726f-1348">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="e726f-1349">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="e726f-1349">Added example</span></span>
    - <span data-ttu-id="e726f-1350">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="e726f-1350">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="e726f-1351">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e726f-1351">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="e726f-1352">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="e726f-1352">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1353">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1354">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1354">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1355">Az.Resources</span></span>
* <span data-ttu-id="e726f-1356">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="e726f-1356">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="e726f-1357">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="e726f-1357">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="e726f-1358">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="e726f-1358">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="e726f-1359">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-1359">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e726f-1360">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e726f-1360">Az.ServiceBus</span></span>
* <span data-ttu-id="e726f-1361">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-1361">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="e726f-1362">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="e726f-1362">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="e726f-1363">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="e726f-1363">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-1364">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-1364">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-1365">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="e726f-1365">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="e726f-1366">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="e726f-1366">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="e726f-1367">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="e726f-1367">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="e726f-1368">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="e726f-1368">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="e726f-1369">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="e726f-1369">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="e726f-1370">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="e726f-1370">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1371">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1371">Az.Sql</span></span>
* <span data-ttu-id="e726f-1372">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="e726f-1372">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1373">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1373">Az.Storage</span></span>
* <span data-ttu-id="e726f-1374">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="e726f-1374">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="e726f-1375">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="e726f-1375">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="e726f-1376">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e726f-1376">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="e726f-1377">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e726f-1377">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="e726f-1378">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="e726f-1378">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="e726f-1379">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e726f-1379">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1380">Az.Websites</span></span>
* <span data-ttu-id="e726f-1381">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e726f-1381">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="e726f-1382">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1382">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-1383">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1383">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1384">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e726f-1384">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="e726f-1385">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1385">Az.ApplicationInsights</span></span>
* <span data-ttu-id="e726f-1386">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="e726f-1386">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1387">Az.Automation</span></span>
* <span data-ttu-id="e726f-1388">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="e726f-1388">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-1389">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1389">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-1390">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="e726f-1390">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1391">Az.Compute</span></span>
* <span data-ttu-id="e726f-1392">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="e726f-1392">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e726f-1393">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e726f-1393">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e726f-1394">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="e726f-1394">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="e726f-1395">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="e726f-1395">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-1396">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-1396">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-1397">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-1397">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="e726f-1398">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="e726f-1398">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e726f-1399">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1399">Az.EventHub</span></span>
* <span data-ttu-id="e726f-1400">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e726f-1400">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e726f-1401">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="e726f-1401">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-1402">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-1402">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-1403">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="e726f-1403">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e726f-1404">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e726f-1404">Az.LogicApp</span></span>
* <span data-ttu-id="e726f-1405">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="e726f-1405">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="e726f-1406">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="e726f-1406">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="e726f-1407">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1407">Az.ManagedServices</span></span>
* <span data-ttu-id="e726f-1408">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="e726f-1408">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1409">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1409">Az.Network</span></span>
* <span data-ttu-id="e726f-1410">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="e726f-1410">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="e726f-1411">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e726f-1411">New cmdlets</span></span>
        - <span data-ttu-id="e726f-1412">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e726f-1412">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e726f-1413">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e726f-1413">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e726f-1414">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1414">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1415">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1415">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1416">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1416">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1417">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1417">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="e726f-1418">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="e726f-1418">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="e726f-1419">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e726f-1419">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="e726f-1420">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="e726f-1420">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="e726f-1421">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="e726f-1421">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="e726f-1422">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e726f-1422">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="e726f-1423">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e726f-1423">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="e726f-1424">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="e726f-1424">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="e726f-1425">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="e726f-1425">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="e726f-1426">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="e726f-1426">Updated cmdlets</span></span>
        - <span data-ttu-id="e726f-1427">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1427">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e726f-1428">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1428">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="e726f-1429">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1429">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="e726f-1430">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1430">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="e726f-1431">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-1431">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="e726f-1432">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e726f-1432">Updated cmdlet:</span></span>
        - <span data-ttu-id="e726f-1433">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1433">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e726f-1434">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1434">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="e726f-1435">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1435">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="e726f-1436">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="e726f-1436">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="e726f-1437">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="e726f-1437">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="e726f-1438">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="e726f-1438">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-1439">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1439">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-1440">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="e726f-1440">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="e726f-1441">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="e726f-1441">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1442">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1442">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1443">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1443">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e726f-1444">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1444">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="e726f-1445">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1445">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="e726f-1446">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1446">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="e726f-1447">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1447">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="e726f-1448">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1448">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e726f-1449">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1449">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="e726f-1450">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1450">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="e726f-1451">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1451">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="e726f-1452">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="e726f-1452">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1453">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1453">Az.Resources</span></span>
- <span data-ttu-id="e726f-1454">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-1454">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="e726f-1455">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e726f-1455">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e726f-1456">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e726f-1456">Az.ServiceBus</span></span>
* <span data-ttu-id="e726f-1457">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="e726f-1457">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="e726f-1458">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="e726f-1458">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1459">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1459">Az.Sql</span></span>
* <span data-ttu-id="e726f-1460">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e726f-1460">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="e726f-1461">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="e726f-1461">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="e726f-1462">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="e726f-1462">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1463">Az.Storage</span></span>
* <span data-ttu-id="e726f-1464">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="e726f-1464">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e726f-1465">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e726f-1465">Az.StorageSync</span></span>
* <span data-ttu-id="e726f-1466">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="e726f-1466">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="e726f-1467">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="e726f-1467">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1468">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1468">Az.Websites</span></span>
* <span data-ttu-id="e726f-1469">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e726f-1469">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="e726f-1470">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e726f-1470">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="e726f-1471">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="e726f-1471">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="e726f-1472">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1472">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-1473">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1473">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1474">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="e726f-1474">Add support for profile cmdlets</span></span>
* <span data-ttu-id="e726f-1475">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="e726f-1475">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="e726f-1476">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="e726f-1476">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="e726f-1477">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e726f-1477">Az.Advisor</span></span>
* <span data-ttu-id="e726f-1478">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="e726f-1478">GA release of Az.Advisor</span></span>
* <span data-ttu-id="e726f-1479">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="e726f-1479">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="e726f-1480">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-1480">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-1481">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="e726f-1481">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="e726f-1482">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e726f-1482">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="e726f-1483">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="e726f-1483">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="e726f-1484">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="e726f-1484">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="e726f-1485">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="e726f-1485">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="e726f-1486">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e726f-1486">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="e726f-1487">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="e726f-1487">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-1488">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1488">Az.Automation</span></span>
* <span data-ttu-id="e726f-1489">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e726f-1489">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1490">Az.Compute</span></span>
* <span data-ttu-id="e726f-1491">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1491">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-1492">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-1493">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="e726f-1493">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e726f-1494">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e726f-1494">Az.EventGrid</span></span>
* <span data-ttu-id="e726f-1495">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="e726f-1495">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-1496">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1496">Az.IotHub</span></span>
* <span data-ttu-id="e726f-1497">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="e726f-1497">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1498">Az.Network</span></span>
* <span data-ttu-id="e726f-1499">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="e726f-1499">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="e726f-1500">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="e726f-1500">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-1501">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1501">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-1502">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="e726f-1502">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="e726f-1503">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="e726f-1503">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-1504">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1504">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-1505">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e726f-1505">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1506">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1507">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="e726f-1507">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1508">Az.Resources</span></span>
    - <span data-ttu-id="e726f-1509">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="e726f-1509">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="e726f-1510">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="e726f-1510">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="e726f-1511">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="e726f-1511">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="e726f-1512">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="e726f-1512">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e726f-1513">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e726f-1513">Az.ServiceBus</span></span>
* <span data-ttu-id="e726f-1514">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="e726f-1514">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1515">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1515">Az.Sql</span></span>
* <span data-ttu-id="e726f-1516">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="e726f-1516">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="e726f-1517">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e726f-1517">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="e726f-1518">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e726f-1518">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e726f-1519">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e726f-1519">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e726f-1520">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="e726f-1520">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="e726f-1521">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e726f-1521">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e726f-1522">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e726f-1522">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="e726f-1523">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e726f-1523">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="e726f-1524">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="e726f-1524">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1525">Az.Storage</span></span>
* <span data-ttu-id="e726f-1526">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e726f-1526">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="e726f-1527">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e726f-1527">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="e726f-1528">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="e726f-1528">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="e726f-1529">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="e726f-1529">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="e726f-1530">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1530">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="e726f-1531">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1531">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="e726f-1532">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1532">Set-AzStorageAccount</span></span>
* <span data-ttu-id="e726f-1533">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="e726f-1533">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="e726f-1534">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e726f-1534">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="e726f-1535">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="e726f-1535">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="e726f-1536">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="e726f-1536">Az.StorageSync</span></span>
* <span data-ttu-id="e726f-1537">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="e726f-1537">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="e726f-1538">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1538">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-1539">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1539">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1540">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="e726f-1540">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="e726f-1541">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="e726f-1541">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="e726f-1542">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="e726f-1542">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="e726f-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e726f-1543">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="e726f-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="e726f-1544">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1545">Az.Compute</span></span>
* <span data-ttu-id="e726f-1546">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1546">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="e726f-1547">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="e726f-1547">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="e726f-1548">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e726f-1548">Az.Dns</span></span>
* <span data-ttu-id="e726f-1549">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1549">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e726f-1550">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e726f-1550">Az.EventGrid</span></span>
* <span data-ttu-id="e726f-1551">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="e726f-1551">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="e726f-1552">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e726f-1552">New cmdlets:</span></span>
    - <span data-ttu-id="e726f-1553">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e726f-1553">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e726f-1554">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1554">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e726f-1555">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e726f-1555">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e726f-1556">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1556">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="e726f-1557">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="e726f-1557">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="e726f-1558">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1558">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e726f-1559">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e726f-1559">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e726f-1560">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1560">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="e726f-1561">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="e726f-1561">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="e726f-1562">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1562">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="e726f-1563">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e726f-1563">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e726f-1564">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1564">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="e726f-1565">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="e726f-1565">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="e726f-1566">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="e726f-1566">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="e726f-1567">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="e726f-1567">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="e726f-1568">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="e726f-1568">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="e726f-1569">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="e726f-1569">Updated cmdlets:</span></span>
    - <span data-ttu-id="e726f-1570">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e726f-1570">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="e726f-1571">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1571">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e726f-1572">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1572">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="e726f-1573">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="e726f-1573">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="e726f-1574">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="e726f-1574">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="e726f-1575">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="e726f-1575">Event subscription expiration date,</span></span>
            - <span data-ttu-id="e726f-1576">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="e726f-1576">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="e726f-1577">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="e726f-1577">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="e726f-1578">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="e726f-1578">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="e726f-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="e726f-1579">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="e726f-1580">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="e726f-1580">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="e726f-1581">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="e726f-1581">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="e726f-1582">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1582">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="e726f-1583">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1583">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e726f-1584">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-1584">Az.FrontDoor</span></span>
* <span data-ttu-id="e726f-1585">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="e726f-1585">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="e726f-1586">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="e726f-1586">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="e726f-1587">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e726f-1587">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="e726f-1588">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="e726f-1588">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1589">Az.Network</span></span>
* <span data-ttu-id="e726f-1590">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e726f-1590">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="e726f-1591">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e726f-1591">New cmdlets</span></span>
        - <span data-ttu-id="e726f-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e726f-1592">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="e726f-1593">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e726f-1593">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="e726f-1594">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e726f-1594">New cmdlets</span></span>
        - <span data-ttu-id="e726f-1595">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="e726f-1595">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="e726f-1596">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e726f-1596">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="e726f-1597">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e726f-1597">New cmdlets</span></span>
        - <span data-ttu-id="e726f-1598">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e726f-1598">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e726f-1599">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e726f-1599">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e726f-1600">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="e726f-1600">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="e726f-1601">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1601">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="e726f-1602">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1602">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="e726f-1603">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e726f-1603">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="e726f-1604">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e726f-1604">New cmdlets</span></span>
        - <span data-ttu-id="e726f-1605">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e726f-1605">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e726f-1606">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e726f-1606">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e726f-1607">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="e726f-1607">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="e726f-1608">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1608">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="e726f-1609">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="e726f-1609">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="e726f-1610">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="e726f-1610">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="e726f-1611">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="e726f-1611">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="e726f-1612">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e726f-1612">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="e726f-1613">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e726f-1613">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="e726f-1614">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e726f-1614">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="e726f-1615">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-1615">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="e726f-1616">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="e726f-1616">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="e726f-1617">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-1617">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="e726f-1618">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="e726f-1618">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="e726f-1619">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="e726f-1619">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="e726f-1620">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="e726f-1620">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="e726f-1621">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="e726f-1621">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="e726f-1622">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1622">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="e726f-1623">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="e726f-1623">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="e726f-1624">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="e726f-1624">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="e726f-1625">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="e726f-1625">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="e726f-1626">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="e726f-1626">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="e726f-1627">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e726f-1627">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="e726f-1628">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e726f-1628">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="e726f-1629">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e726f-1629">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e726f-1630">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e726f-1630">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="e726f-1631">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="e726f-1631">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-1632">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1632">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-1633">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="e726f-1633">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1634">Az.Resources</span></span>
* <span data-ttu-id="e726f-1635">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="e726f-1635">Support for additional Template Export options</span></span>
    - <span data-ttu-id="e726f-1636">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1636">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e726f-1637">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1637">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="e726f-1638">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="e726f-1638">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-1639">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-1640">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="e726f-1640">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1641">Az.Sql</span></span>
* <span data-ttu-id="e726f-1642">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="e726f-1642">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="e726f-1643">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="e726f-1643">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="e726f-1644">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="e726f-1644">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="e726f-1645">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e726f-1645">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e726f-1646">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e726f-1646">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e726f-1647">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e726f-1647">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="e726f-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e726f-1648">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="e726f-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e726f-1649">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1650">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1650">Az.Storage</span></span>
* <span data-ttu-id="e726f-1651">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e726f-1651">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="e726f-1652">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1652">New-AzStorageAccount</span></span>
* <span data-ttu-id="e726f-1653">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="e726f-1653">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="e726f-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-1654">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1655">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1655">Az.Websites</span></span>
* <span data-ttu-id="e726f-1656">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="e726f-1656">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="e726f-1657">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="e726f-1657">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="e726f-1658">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1658">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e726f-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-1659">Az.Cdn</span></span>
* <span data-ttu-id="e726f-1660">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="e726f-1660">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1661">Az.Compute</span></span>
* <span data-ttu-id="e726f-1662">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="e726f-1662">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e726f-1663">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e726f-1663">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e726f-1664">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1664">Az.EventHub</span></span>
* <span data-ttu-id="e726f-1665">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="e726f-1665">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e726f-1666">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e726f-1666">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1667">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1667">Az.Network</span></span>
* <span data-ttu-id="e726f-1668">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="e726f-1668">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e726f-1669">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="e726f-1669">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-1670">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1670">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-1671">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="e726f-1671">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1672">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1673">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="e726f-1673">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e726f-1674">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e726f-1674">Az.ServiceBus</span></span>
* <span data-ttu-id="e726f-1675">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e726f-1675">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-1676">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-1676">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-1677">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="e726f-1677">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e726f-1678">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e726f-1678">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1679">Az.Sql</span></span>
* <span data-ttu-id="e726f-1680">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e726f-1680">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e726f-1681">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-1681">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e726f-1682">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="e726f-1682">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e726f-1683">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="e726f-1683">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1684">Az.Websites</span></span>
* <span data-ttu-id="e726f-1685">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="e726f-1685">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e726f-1686">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1686">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e726f-1687">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-1687">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-1688">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="e726f-1688">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e726f-1689">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e726f-1689">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e726f-1690">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e726f-1690">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e726f-1691">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="e726f-1691">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e726f-1692">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="e726f-1692">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e726f-1693">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="e726f-1693">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e726f-1694">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e726f-1694">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e726f-1695">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="e726f-1695">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e726f-1696">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-1696">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e726f-1697">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="e726f-1697">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e726f-1698">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1698">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e726f-1699">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="e726f-1699">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e726f-1700">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="e726f-1700">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e726f-1701">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="e726f-1701">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e726f-1702">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="e726f-1702">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e726f-1703">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="e726f-1703">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e726f-1704">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="e726f-1704">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e726f-1705">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="e726f-1705">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e726f-1706">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="e726f-1706">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="e726f-1707">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="e726f-1707">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e726f-1708">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="e726f-1708">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e726f-1709">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="e726f-1709">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e726f-1710">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="e726f-1710">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e726f-1711">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-1711">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="e726f-1712">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="e726f-1712">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e726f-1713">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="e726f-1713">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e726f-1714">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1714">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e726f-1715">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e726f-1715">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e726f-1716">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e726f-1716">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e726f-1717">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="e726f-1717">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e726f-1718">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="e726f-1718">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="e726f-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e726f-1719">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e726f-1720">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="e726f-1720">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e726f-1721">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e726f-1721">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e726f-1722">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="e726f-1722">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e726f-1723">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="e726f-1723">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e726f-1724">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="e726f-1724">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e726f-1725">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="e726f-1725">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e726f-1726">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="e726f-1726">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e726f-1727">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e726f-1727">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e726f-1728">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1728">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e726f-1729">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e726f-1729">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e726f-1730">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1730">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e726f-1731">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="e726f-1731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="e726f-1732">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="e726f-1732">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e726f-1733">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1733">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e726f-1734">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e726f-1734">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e726f-1735">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="e726f-1735">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="e726f-1736">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="e726f-1736">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e726f-1737">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1737">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e726f-1738">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="e726f-1738">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e726f-1739">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="e726f-1739">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e726f-1740">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="e726f-1740">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e726f-1741">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e726f-1741">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e726f-1742">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="e726f-1742">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e726f-1743">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="e726f-1743">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e726f-1744">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e726f-1744">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e726f-1745">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e726f-1745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e726f-1746">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e726f-1746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e726f-1747">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e726f-1747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e726f-1748">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="e726f-1748">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e726f-1749">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e726f-1749">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e726f-1750">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="e726f-1750">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e726f-1751">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e726f-1751">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e726f-1752">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="e726f-1752">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e726f-1753">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="e726f-1753">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e726f-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e726f-1754">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e726f-1755">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="e726f-1755">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e726f-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e726f-1756">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e726f-1757">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e726f-1757">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e726f-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e726f-1758">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e726f-1759">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="e726f-1759">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e726f-1760">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="e726f-1760">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e726f-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e726f-1761">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e726f-1762">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="e726f-1762">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="e726f-1763">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="e726f-1763">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e726f-1764">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="e726f-1764">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-1765">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1765">Az.Automation</span></span>
* <span data-ttu-id="e726f-1766">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="e726f-1766">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e726f-1767">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="e726f-1767">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e726f-1768">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="e726f-1768">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e726f-1769">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="e726f-1769">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e726f-1770">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="e726f-1770">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e726f-1771">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="e726f-1771">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e726f-1772">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="e726f-1772">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1773">Az.Compute</span></span>
* <span data-ttu-id="e726f-1774">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="e726f-1774">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e726f-1775">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="e726f-1775">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-1776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-1776">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-1777">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1777">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-1778">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-1778">Az.Monitor</span></span>
* <span data-ttu-id="e726f-1779">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-1779">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1780">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1780">Az.Network</span></span>
* <span data-ttu-id="e726f-1781">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="e726f-1781">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e726f-1782">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e726f-1782">Updated cmdlet:</span></span>
        - <span data-ttu-id="e726f-1783">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e726f-1783">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e726f-1784">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e726f-1784">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1785">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1785">Az.Resources</span></span>
* <span data-ttu-id="e726f-1786">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="e726f-1786">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1787">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1787">Az.Sql</span></span>
* <span data-ttu-id="e726f-1788">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="e726f-1788">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e726f-1789">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1789">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-1790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1790">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1791">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="e726f-1791">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-1792">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1792">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-1793">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="e726f-1793">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e726f-1794">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="e726f-1794">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1795">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1795">Az.Compute</span></span>
* <span data-ttu-id="e726f-1796">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e726f-1796">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e726f-1797">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1797">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e726f-1798">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1798">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e726f-1799">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="e726f-1799">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e726f-1800">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="e726f-1800">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e726f-1801">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-1801">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="e726f-1802">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="e726f-1802">Breaking changes</span></span>
    - <span data-ttu-id="e726f-1803">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e726f-1803">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e726f-1804">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="e726f-1804">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e726f-1805">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e726f-1805">Az.DeploymentManager</span></span>
* <span data-ttu-id="e726f-1806">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1806">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e726f-1807">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e726f-1807">Az.Dns</span></span>
* <span data-ttu-id="e726f-1808">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="e726f-1808">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e726f-1809">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="e726f-1809">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e726f-1810">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="e726f-1810">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e726f-1811">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-1811">Az.FrontDoor</span></span>
* <span data-ttu-id="e726f-1812">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1812">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e726f-1813">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="e726f-1813">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e726f-1814">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-1814">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-1815">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="e726f-1815">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e726f-1816">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e726f-1816">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e726f-1817">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e726f-1817">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e726f-1818">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e726f-1818">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e726f-1819">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="e726f-1819">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e726f-1820">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="e726f-1820">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e726f-1821">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="e726f-1821">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-1822">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-1822">Az.Monitor</span></span>
* <span data-ttu-id="e726f-1823">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="e726f-1823">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="e726f-1824">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e726f-1824">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e726f-1825">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-1825">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e726f-1826">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e726f-1826">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e726f-1827">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e726f-1827">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e726f-1828">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e726f-1828">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e726f-1829">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e726f-1829">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e726f-1830">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e726f-1830">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e726f-1831">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e726f-1831">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e726f-1832">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e726f-1832">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e726f-1833">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e726f-1833">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e726f-1834">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e726f-1834">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e726f-1835">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="e726f-1835">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e726f-1836">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="e726f-1836">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1837">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1837">Az.Network</span></span>
* <span data-ttu-id="e726f-1838">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="e726f-1838">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e726f-1839">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="e726f-1839">New cmdlets</span></span>
        - <span data-ttu-id="e726f-1840">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e726f-1840">New-AzNatGateway</span></span>
        - <span data-ttu-id="e726f-1841">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e726f-1841">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e726f-1842">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e726f-1842">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e726f-1843">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e726f-1843">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e726f-1844">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="e726f-1844">Updated cmdlets</span></span>
        - <span data-ttu-id="e726f-1845">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e726f-1845">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e726f-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e726f-1846">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e726f-1847">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="e726f-1847">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e726f-1848">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e726f-1848">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e726f-1849">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="e726f-1849">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-1850">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1850">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-1851">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="e726f-1851">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e726f-1852">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="e726f-1852">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e726f-1853">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="e726f-1853">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1854">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1854">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1855">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e726f-1855">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e726f-1856">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e726f-1856">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e726f-1857">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e726f-1857">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e726f-1858">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-1858">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e726f-1859">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e726f-1859">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e726f-1860">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="e726f-1860">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e726f-1861">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e726f-1861">Az.Relay</span></span>
* <span data-ttu-id="e726f-1862">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="e726f-1862">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e726f-1863">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e726f-1863">Az.ServiceBus</span></span>
* <span data-ttu-id="e726f-1864">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="e726f-1864">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1865">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1865">Az.Storage</span></span>
* <span data-ttu-id="e726f-1866">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="e726f-1866">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e726f-1867">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="e726f-1867">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e726f-1868">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="e726f-1868">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e726f-1869">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1869">New-AzStorageAccount</span></span>
* <span data-ttu-id="e726f-1870">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="e726f-1870">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e726f-1871">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1871">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e726f-1872">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1872">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e726f-1873">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-1873">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1874">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1874">Az.Websites</span></span>
* <span data-ttu-id="e726f-1875">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e726f-1875">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e726f-1876">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="e726f-1876">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e726f-1877">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1877">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e726f-1878">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e726f-1878">Highlights since the last major release</span></span>
* <span data-ttu-id="e726f-1879">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="e726f-1879">General availability of `Az` module</span></span>
* <span data-ttu-id="e726f-1880">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e726f-1880">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e726f-1881">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e726f-1881">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e726f-1882">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1882">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e726f-1883">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e726f-1883">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e726f-1884">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1884">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e726f-1885">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="e726f-1885">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-1886">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1886">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1887">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="e726f-1887">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e726f-1888">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e726f-1888">Az.Batch</span></span>
* <span data-ttu-id="e726f-1889">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e726f-1890">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-1890">Az.Cdn</span></span>
* <span data-ttu-id="e726f-1891">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1891">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-1892">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1892">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-1893">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1894">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1894">Az.Compute</span></span>
* <span data-ttu-id="e726f-1895">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="e726f-1895">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e726f-1896">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1896">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e726f-1897">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e726f-1897">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-1898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-1898">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-1899">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e726f-1899">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-1900">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-1900">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-1901">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e726f-1902">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e726f-1902">Az.EventGrid</span></span>
* <span data-ttu-id="e726f-1903">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="e726f-1903">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e726f-1904">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1904">Az.EventHub</span></span>
* <span data-ttu-id="e726f-1905">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="e726f-1905">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="e726f-1906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e726f-1906">Az.HDInsight</span></span>
* <span data-ttu-id="e726f-1907">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-1908">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-1908">Az.IotHub</span></span>
* <span data-ttu-id="e726f-1909">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1909">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-1910">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-1910">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-1911">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e726f-1912">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e726f-1912">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e726f-1913">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e726f-1913">Az.MachineLearning</span></span>
* <span data-ttu-id="e726f-1914">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1914">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e726f-1915">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e726f-1915">Az.Media</span></span>
* <span data-ttu-id="e726f-1916">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1916">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-1917">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-1917">Az.Monitor</span></span>
  * <span data-ttu-id="e726f-1918">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="e726f-1918">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e726f-1919">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e726f-1919">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e726f-1920">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e726f-1920">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e726f-1921">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e726f-1921">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e726f-1922">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e726f-1922">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e726f-1923">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e726f-1923">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e726f-1924">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="e726f-1924">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1925">Az.Network</span></span>
* <span data-ttu-id="e726f-1926">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e726f-1927">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e726f-1927">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e726f-1928">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e726f-1928">Az.NotificationHubs</span></span>
* <span data-ttu-id="e726f-1929">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-1930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-1930">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-1931">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e726f-1932">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e726f-1932">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e726f-1933">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1933">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-1934">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1934">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-1935">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1935">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e726f-1936">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1936">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e726f-1937">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="e726f-1937">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e726f-1938">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="e726f-1938">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e726f-1939">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e726f-1939">Az.RedisCache</span></span>
* <span data-ttu-id="e726f-1940">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1940">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1941">Az.Resources</span></span>
* <span data-ttu-id="e726f-1942">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e726f-1942">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1943">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1943">Az.Sql</span></span>
* <span data-ttu-id="e726f-1944">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="e726f-1944">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e726f-1945">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e726f-1946">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="e726f-1946">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e726f-1947">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="e726f-1947">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e726f-1948">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="e726f-1948">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e726f-1949">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="e726f-1949">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e726f-1950">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="e726f-1950">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-1951">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-1951">Az.Websites</span></span>
* <span data-ttu-id="e726f-1952">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="e726f-1952">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e726f-1953">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="e726f-1953">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e726f-1954">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="e726f-1954">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e726f-1955">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="e726f-1955">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e726f-1956">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-1956">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e726f-1957">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e726f-1957">Highlights since the last major release</span></span>
* <span data-ttu-id="e726f-1958">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="e726f-1958">General availability of `Az` module</span></span>
* <span data-ttu-id="e726f-1959">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e726f-1959">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e726f-1960">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e726f-1960">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e726f-1961">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-1961">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e726f-1962">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e726f-1962">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e726f-1963">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1963">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e726f-1964">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="e726f-1964">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e726f-1965">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-1965">Az.Accounts</span></span>
* <span data-ttu-id="e726f-1966">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e726f-1966">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e726f-1967">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e726f-1967">Az.AnalysisServices</span></span>
* <span data-ttu-id="e726f-1968">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="e726f-1968">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e726f-1969">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="e726f-1969">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-1970">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-1970">Az.Automation</span></span>
* <span data-ttu-id="e726f-1971">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="e726f-1971">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e726f-1972">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="e726f-1972">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e726f-1973">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1973">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-1974">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-1974">Az.Compute</span></span>
* <span data-ttu-id="e726f-1975">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-1975">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e726f-1976">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="e726f-1976">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="e726f-1977">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-1977">Az.ContainerInstance</span></span>
* <span data-ttu-id="e726f-1978">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="e726f-1978">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-1979">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-1979">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-1980">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="e726f-1980">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e726f-1981">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e726f-1981">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-1982">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-1982">Az.Resources</span></span>
* <span data-ttu-id="e726f-1983">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="e726f-1983">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e726f-1984">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-1984">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e726f-1985">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="e726f-1985">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e726f-1986">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e726f-1986">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e726f-1987">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="e726f-1987">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e726f-1988">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e726f-1988">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-1989">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-1989">Az.Sql</span></span>
* <span data-ttu-id="e726f-1990">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="e726f-1990">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-1991">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-1991">Az.Storage</span></span>
* <span data-ttu-id="e726f-1992">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-1992">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e726f-1993">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e726f-1993">New-AzStorageContext</span></span>
* <span data-ttu-id="e726f-1994">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="e726f-1994">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e726f-1995">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e726f-1995">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e726f-1996">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e726f-1996">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e726f-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-1997">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e726f-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-1998">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e726f-1999">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="e726f-1999">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e726f-2000">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e726f-2000">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e726f-2001">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e726f-2001">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e726f-2002">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e726f-2002">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e726f-2003">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e726f-2003">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e726f-2004">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-2004">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e726f-2005">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="e726f-2005">Highlights since the last major release</span></span>
* <span data-ttu-id="e726f-2006">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="e726f-2006">General availability of `Az` module</span></span>
* <span data-ttu-id="e726f-2007">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e726f-2007">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e726f-2008">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e726f-2008">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e726f-2009">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2009">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e726f-2010">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e726f-2010">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e726f-2011">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-2011">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e726f-2012">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="e726f-2012">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-2013">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-2013">Az.Automation</span></span>
* <span data-ttu-id="e726f-2014">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="e726f-2014">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e726f-2015">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="e726f-2015">Dynamic grouping</span></span>
    * <span data-ttu-id="e726f-2016">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="e726f-2016">Pre-Post script</span></span>
    * <span data-ttu-id="e726f-2017">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="e726f-2017">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2018">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2018">Az.Compute</span></span>
* <span data-ttu-id="e726f-2019">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e726f-2019">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e726f-2020">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="e726f-2020">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-2021">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-2021">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-2022">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-2022">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-2023">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2023">Az.Network</span></span>
* <span data-ttu-id="e726f-2024">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-2024">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e726f-2025">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="e726f-2025">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-2026">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2026">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-2027">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="e726f-2027">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e726f-2028">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="e726f-2028">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2029">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2029">Az.Resources</span></span>
* <span data-ttu-id="e726f-2030">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e726f-2030">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e726f-2031">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="e726f-2031">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-2032">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2032">Az.Sql</span></span>
* <span data-ttu-id="e726f-2033">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="e726f-2033">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-2034">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-2034">Az.Storage</span></span>
* <span data-ttu-id="e726f-2035">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="e726f-2035">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e726f-2036">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-2036">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e726f-2037">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-2037">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e726f-2038">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-2038">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e726f-2039">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e726f-2039">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e726f-2040">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e726f-2040">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e726f-2041">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e726f-2041">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-2042">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-2042">Az.Websites</span></span>
* <span data-ttu-id="e726f-2043">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="e726f-2043">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="e726f-2044">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-2044">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-2045">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2045">Az.Accounts</span></span>
* <span data-ttu-id="e726f-2046">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="e726f-2046">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e726f-2047">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-2047">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-2048">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-2048">Az.Automation</span></span>
* <span data-ttu-id="e726f-2049">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-2049">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e726f-2050">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="e726f-2050">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e726f-2051">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="e726f-2051">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e726f-2052">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-2052">Az.Cdn</span></span>
* <span data-ttu-id="e726f-2053">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="e726f-2053">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2054">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2054">Az.Compute</span></span>
* <span data-ttu-id="e726f-2055">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="e726f-2055">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-2056">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-2056">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-2057">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="e726f-2057">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e726f-2058">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e726f-2058">Az.LogicApp</span></span>
* <span data-ttu-id="e726f-2059">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="e726f-2059">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-2060">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2060">Az.Network</span></span>
* <span data-ttu-id="e726f-2061">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2061">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-2062">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2062">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-2063">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-2063">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e726f-2064">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="e726f-2064">SDK Update</span></span>
* <span data-ttu-id="e726f-2065">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e726f-2065">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e726f-2066">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e726f-2066">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2067">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2067">Az.Resources</span></span>
* <span data-ttu-id="e726f-2068">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="e726f-2068">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e726f-2069">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e726f-2069">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e726f-2070">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e726f-2070">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e726f-2071">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e726f-2071">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e726f-2072">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e726f-2072">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e726f-2073">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e726f-2073">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-2074">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2074">Az.Sql</span></span>
* <span data-ttu-id="e726f-2075">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="e726f-2075">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e726f-2076">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="e726f-2076">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-2077">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-2077">Az.Storage</span></span>
* <span data-ttu-id="e726f-2078">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-2078">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e726f-2079">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-2079">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e726f-2080">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2080">Az.AnalysisServices</span></span>
* <span data-ttu-id="e726f-2081">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-2081">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-2082">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-2082">Az.Automation</span></span>
* <span data-ttu-id="e726f-2083">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2083">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e726f-2084">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2084">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e726f-2085">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2085">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-2087">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="e726f-2087">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2088">Az.Compute</span></span>
* <span data-ttu-id="e726f-2089">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="e726f-2089">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e726f-2090">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="e726f-2090">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e726f-2091">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e726f-2091">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e726f-2092">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="e726f-2092">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-2093">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-2093">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-2094">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="e726f-2094">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e726f-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-2095">Az.EventHub</span></span>
* <span data-ttu-id="e726f-2096">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="e726f-2096">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-2097">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-2097">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-2098">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e726f-2098">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e726f-2099">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e726f-2099">Az.LogicApp</span></span>
* <span data-ttu-id="e726f-2100">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="e726f-2100">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e726f-2101">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="e726f-2101">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e726f-2102">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="e726f-2102">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e726f-2103">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e726f-2103">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e726f-2104">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e726f-2104">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e726f-2105">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e726f-2105">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e726f-2106">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e726f-2106">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e726f-2107">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="e726f-2107">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e726f-2108">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2108">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e726f-2109">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2109">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e726f-2110">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2110">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e726f-2111">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2111">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e726f-2112">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e726f-2112">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e726f-2113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-2113">Az.Monitor</span></span>
* <span data-ttu-id="e726f-2114">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="e726f-2114">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-2115">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2115">Az.Network</span></span>
* <span data-ttu-id="e726f-2116">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e726f-2116">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-2117">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-2117">Az.OperationalInsights</span></span>
* <span data-ttu-id="e726f-2118">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="e726f-2118">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e726f-2119">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="e726f-2119">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="e726f-2120">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="e726f-2120">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2121">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2121">Az.Resources</span></span>
* <span data-ttu-id="e726f-2122">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e726f-2122">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e726f-2123">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e726f-2123">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e726f-2124">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e726f-2124">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e726f-2125">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="e726f-2125">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-2126">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2126">Az.Sql</span></span>
* <span data-ttu-id="e726f-2127">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="e726f-2127">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e726f-2128">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="e726f-2128">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-2129">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-2129">Az.Websites</span></span>
* <span data-ttu-id="e726f-2130">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="e726f-2130">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e726f-2131">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-2131">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-2132">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2132">Az.Accounts</span></span>
* <span data-ttu-id="e726f-2133">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e726f-2133">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e726f-2134">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2134">Az.AnalysisServices</span></span>
<span data-ttu-id="e726f-2135">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="e726f-2135">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2136">Az.Compute</span></span>
* <span data-ttu-id="e726f-2137">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="e726f-2137">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e726f-2138">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="e726f-2138">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e726f-2139">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="e726f-2139">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-2140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2140">Az.RecoveryServices</span></span>
<span data-ttu-id="e726f-2141">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="e726f-2141">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2142">Az.Resources</span></span>
* <span data-ttu-id="e726f-2143">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="e726f-2143">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="e726f-2144">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e726f-2144">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e726f-2145">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="e726f-2145">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="e726f-2146">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e726f-2146">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-2147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2147">Az.Sql</span></span>
* <span data-ttu-id="e726f-2148">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e726f-2148">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e726f-2149">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="e726f-2149">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e726f-2150">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="e726f-2150">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e726f-2151">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-2151">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-2152">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2152">Az.Accounts</span></span>
* <span data-ttu-id="e726f-2153">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="e726f-2153">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e726f-2154">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2154">Az.AnalysisServices</span></span>
* <span data-ttu-id="e726f-2155">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-2155">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-2156">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2156">Az.RecoveryServices</span></span>
* <span data-ttu-id="e726f-2157">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-2157">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e726f-2158">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-2158">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-2159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2159">Az.Accounts</span></span>
* <span data-ttu-id="e726f-2160">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="e726f-2160">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e726f-2161">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2161">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e726f-2162">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="e726f-2162">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e726f-2163">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e726f-2163">Az.Aks</span></span>
* <span data-ttu-id="e726f-2164">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2164">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e726f-2165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-2165">Az.Automation</span></span>
* <span data-ttu-id="e726f-2166">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="e726f-2166">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e726f-2167">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2167">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e726f-2168">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e726f-2168">Az.Cdn</span></span>
* <span data-ttu-id="e726f-2169">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2169">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2170">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2170">Az.Compute</span></span>
* <span data-ttu-id="e726f-2171">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="e726f-2171">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e726f-2172">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e726f-2172">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e726f-2173">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="e726f-2173">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e726f-2174">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e726f-2174">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e726f-2175">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2175">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e726f-2176">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e726f-2176">Az.DataFactory</span></span>
* <span data-ttu-id="e726f-2177">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e726f-2177">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-2178">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-2178">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-2179">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="e726f-2179">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e726f-2180">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e726f-2180">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e726f-2181">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2181">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-2182">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-2182">Az.IotHub</span></span>
* <span data-ttu-id="e726f-2183">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e726f-2183">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e726f-2184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-2184">Az.KeyVault</span></span>
* <span data-ttu-id="e726f-2185">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2185">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-2186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2186">Az.Network</span></span>
* <span data-ttu-id="e726f-2187">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2187">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2188">Az.Resources</span></span>
* <span data-ttu-id="e726f-2189">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="e726f-2189">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e726f-2190">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e726f-2190">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e726f-2191">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="e726f-2191">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e726f-2192">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e726f-2192">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e726f-2193">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e726f-2193">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e726f-2194">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="e726f-2194">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e726f-2195">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e726f-2195">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-2196">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-2196">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-2197">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="e726f-2197">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e726f-2198">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="e726f-2198">Fix some error messages.</span></span>
* <span data-ttu-id="e726f-2199">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="e726f-2199">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e726f-2200">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="e726f-2200">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e726f-2201">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e726f-2201">Az.SignalR</span></span>
* <span data-ttu-id="e726f-2202">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2202">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-2203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2203">Az.Sql</span></span>
* <span data-ttu-id="e726f-2204">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2204">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e726f-2205">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="e726f-2205">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e726f-2206">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="e726f-2206">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e726f-2207">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="e726f-2207">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-2208">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-2208">Az.Storage</span></span>
* <span data-ttu-id="e726f-2209">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2209">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e726f-2210">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="e726f-2210">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e726f-2211">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e726f-2211">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e726f-2212">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e726f-2212">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e726f-2213">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e726f-2213">Az.TrafficManager</span></span>
* <span data-ttu-id="e726f-2214">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2214">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-2215">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-2215">Az.Websites</span></span>
* <span data-ttu-id="e726f-2216">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="e726f-2216">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e726f-2217">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="e726f-2217">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e726f-2218">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="e726f-2218">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e726f-2219">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="e726f-2219">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e726f-2220">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2220">Az.Accounts</span></span>
* <span data-ttu-id="e726f-2221">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="e726f-2221">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2222">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2222">Az.Compute</span></span>
* <span data-ttu-id="e726f-2223">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e726f-2223">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e726f-2224">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="e726f-2224">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e726f-2225">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2225">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-2227">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="e726f-2227">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e726f-2228">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="e726f-2228">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e726f-2229">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e726f-2229">Az.EventGrid</span></span>
* <span data-ttu-id="e726f-2230">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="e726f-2230">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e726f-2231">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="e726f-2231">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e726f-2232">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="e726f-2232">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e726f-2233">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="e726f-2233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e726f-2234">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="e726f-2234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e726f-2235">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="e726f-2235">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e726f-2236">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="e726f-2236">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e726f-2237">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="e726f-2237">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e726f-2238">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="e726f-2238">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e726f-2239">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="e726f-2239">Dead letter endpoint.</span></span>
* <span data-ttu-id="e726f-2240">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="e726f-2240">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e726f-2241">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="e726f-2241">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e726f-2242">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-2242">Az.IotHub</span></span>
* <span data-ttu-id="e726f-2243">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="e726f-2243">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e726f-2244">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e726f-2244">Az.LogicApp</span></span>
* <span data-ttu-id="e726f-2245">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="e726f-2245">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2246">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2246">Az.Resources</span></span>
* <span data-ttu-id="e726f-2247">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="e726f-2247">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e726f-2248">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e726f-2248">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e726f-2249">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e726f-2249">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e726f-2250">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e726f-2250">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e726f-2251">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="e726f-2251">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e726f-2252">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e726f-2252">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e726f-2253">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e726f-2253">Az.SignalR</span></span>
* <span data-ttu-id="e726f-2254">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2254">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-2255">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2255">Az.Sql</span></span>
* <span data-ttu-id="e726f-2256">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="e726f-2256">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e726f-2257">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-2257">Az.Storage</span></span>
* <span data-ttu-id="e726f-2258">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="e726f-2258">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e726f-2259">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e726f-2259">New-AzStorageContext</span></span>
* <span data-ttu-id="e726f-2260">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="e726f-2260">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e726f-2261">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e726f-2261">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-2262">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-2262">Az.Websites</span></span>
* <span data-ttu-id="e726f-2263">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="e726f-2263">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e726f-2264">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2264">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e726f-2265">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e726f-2265">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e726f-2266">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-2266">General</span></span>

- <span data-ttu-id="e726f-2267">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="e726f-2267">General Availability of Az Module</span></span>
- <span data-ttu-id="e726f-2268">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="e726f-2268">Online help for each module</span></span>
- <span data-ttu-id="e726f-2269">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="e726f-2269">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e726f-2270">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="e726f-2270">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e726f-2271">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2271">Az.Accounts</span></span>
- <span data-ttu-id="e726f-2272">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e726f-2272">Changed from Az.Profile</span></span>
- <span data-ttu-id="e726f-2273">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="e726f-2273">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e726f-2274">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-2274">Az.ApiManagement</span></span>
- <span data-ttu-id="e726f-2275">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="e726f-2275">Fixes for #7002</span></span>
- <span data-ttu-id="e726f-2276">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e726f-2277">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e726f-2277">Az.Batch</span></span>
- <span data-ttu-id="e726f-2278">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="e726f-2278">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e726f-2279">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="e726f-2279">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e726f-2280">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2280">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e726f-2281">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e726f-2281">Az.Billing</span></span>
- <span data-ttu-id="e726f-2282">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2282">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e726f-2283">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2283">Az.CognitivServices</span></span>
- <span data-ttu-id="e726f-2284">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-2284">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e726f-2285">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e726f-2285">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e726f-2286">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-2286">Az.ContainerInstance</span></span>
- <span data-ttu-id="e726f-2287">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e726f-2287">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e726f-2288">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e726f-2288">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e726f-2289">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2289">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e726f-2290">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-2290">Az.DataLakeStore</span></span>
- <span data-ttu-id="e726f-2291">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2291">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e726f-2292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e726f-2292">Az.Monitor</span></span>
- <span data-ttu-id="e726f-2293">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2293">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e726f-2294">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e726f-2294">Az.KeyVault</span></span>
- <span data-ttu-id="e726f-2295">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="e726f-2295">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e726f-2296">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e726f-2296">Az.MachineLearning</span></span>
- <span data-ttu-id="e726f-2297">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="e726f-2297">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e726f-2298">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e726f-2298">Az.Media</span></span>
- <span data-ttu-id="e726f-2299">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="e726f-2299">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e726f-2300">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2300">Az.Network</span></span>
<span data-ttu-id="e726f-2301">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="e726f-2301">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e726f-2302">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="e726f-2302">New cmdlets added:</span></span>
        - <span data-ttu-id="e726f-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-2303">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e726f-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-2304">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e726f-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-2305">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e726f-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-2306">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e726f-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-2307">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e726f-2308">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e726f-2308">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e726f-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e726f-2309">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e726f-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e726f-2310">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e726f-2311">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e726f-2311">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e726f-2312">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e726f-2312">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e726f-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e726f-2313">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e726f-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e726f-2314">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e726f-2315">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-2315">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e726f-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-2316">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e726f-2317">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="e726f-2317">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e726f-2318">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e726f-2318">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e726f-2319">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e726f-2319">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e726f-2320">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e726f-2320">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e726f-2321">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e726f-2321">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e726f-2322">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e726f-2322">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e726f-2323">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e726f-2324">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-2324">Az.OperationalInsights</span></span>
- <span data-ttu-id="e726f-2325">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e726f-2326">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e726f-2326">Az.Profile</span></span>
- <span data-ttu-id="e726f-2327">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e726f-2327">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-2328">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2328">Az.RecoveryServices</span></span>
- <span data-ttu-id="e726f-2329">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2329">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e726f-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2330">Az.Resources</span></span>
- <span data-ttu-id="e726f-2331">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2331">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e726f-2332">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-2332">Az.ServiceFabric</span></span>
- <span data-ttu-id="e726f-2333">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="e726f-2333">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e726f-2334">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2334">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e726f-2335">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e726f-2335">Az.SIgnalR</span></span>
- <span data-ttu-id="e726f-2336">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e726f-2336">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e726f-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2337">Az.Sql</span></span>
- <span data-ttu-id="e726f-2338">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="e726f-2338">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e726f-2339">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="e726f-2339">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e726f-2340">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e726f-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-2341">Az.Storage</span></span>
- <span data-ttu-id="e726f-2342">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2342">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e726f-2343">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-2343">Az.Websites</span></span>
- <span data-ttu-id="e726f-2344">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="e726f-2344">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e726f-2345">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e726f-2345">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e726f-2346">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-2346">General</span></span>

* <span data-ttu-id="e726f-2347">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="e726f-2347">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e726f-2348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2348">Az.Compute</span></span>

* <span data-ttu-id="e726f-2349">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="e726f-2349">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e726f-2350">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-2350">Az.DataLakeStore</span></span>

* <span data-ttu-id="e726f-2351">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="e726f-2351">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e726f-2352">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e726f-2352">Az.FrontDoor</span></span>

* <span data-ttu-id="e726f-2353">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="e726f-2353">Fixed some broken links</span></span>
    - <span data-ttu-id="e726f-2354">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="e726f-2354">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e726f-2355">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="e726f-2355">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e726f-2356">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2356">Az.RecoveryServices</span></span>

* <span data-ttu-id="e726f-2357">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="e726f-2357">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e726f-2358">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="e726f-2358">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e726f-2359">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2359">Az.Resources</span></span>

* <span data-ttu-id="e726f-2360">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="e726f-2360">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e726f-2361">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="e726f-2361">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e726f-2362">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2362">Az.Sql</span></span>

* <span data-ttu-id="e726f-2363">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="e726f-2363">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e726f-2364">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="e726f-2364">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e726f-2365">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="e726f-2365">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e726f-2366">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-2366">Az.Storage</span></span>

* <span data-ttu-id="e726f-2367">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-2367">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e726f-2368">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="e726f-2368">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e726f-2369">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e726f-2369">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e726f-2370">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="e726f-2370">Support Static Website configuration</span></span>
    - <span data-ttu-id="e726f-2371">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e726f-2371">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e726f-2372">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e726f-2372">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e726f-2373">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-2373">Az.Websites</span></span>

* <span data-ttu-id="e726f-2374">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e726f-2374">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="e726f-2375">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="e726f-2375">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e726f-2376">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e726f-2376">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e726f-2377">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e726f-2377">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e726f-2378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e726f-2378">Az.ApiManagement</span></span>
* <span data-ttu-id="e726f-2379">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e726f-2379">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e726f-2380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e726f-2380">Az.Automation</span></span>
* <span data-ttu-id="e726f-2381">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="e726f-2381">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e726f-2382">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-2382">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e726f-2383">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-2383">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e726f-2384">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="e726f-2384">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e726f-2385">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="e726f-2385">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e726f-2386">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2386">Az.Compute</span></span>
* <span data-ttu-id="e726f-2387">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e726f-2387">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e726f-2388">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e726f-2388">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e726f-2389">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-2389">Az.ContainerInstance</span></span>
* <span data-ttu-id="e726f-2390">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e726f-2390">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e726f-2391">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e726f-2391">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e726f-2392">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="e726f-2392">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e726f-2393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2393">Az.Network</span></span>
* <span data-ttu-id="e726f-2394">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-2394">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e726f-2395">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="e726f-2395">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e726f-2396">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="e726f-2396">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="e726f-2397">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e726f-2397">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e726f-2398">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e726f-2398">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e726f-2399">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="e726f-2399">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e726f-2400">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="e726f-2400">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e726f-2401">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e726f-2401">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e726f-2402">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e726f-2402">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e726f-2403">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="e726f-2403">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e726f-2404">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e726f-2404">Az.Relay</span></span>
* <span data-ttu-id="e726f-2405">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="e726f-2405">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e726f-2406">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2406">Az.Resources</span></span>
* <span data-ttu-id="e726f-2407">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="e726f-2407">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e726f-2408">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="e726f-2408">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e726f-2409">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="e726f-2409">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e726f-2410">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-2410">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-2411">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="e726f-2411">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e726f-2412">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2412">Az.Sql</span></span>
* <span data-ttu-id="e726f-2413">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="e726f-2413">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e726f-2414">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-2414">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e726f-2415">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-2415">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e726f-2416">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-2416">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e726f-2417">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e726f-2417">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e726f-2418">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e726f-2418">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e726f-2419">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e726f-2419">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e726f-2420">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e726f-2420">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e726f-2421">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e726f-2421">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e726f-2422">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e726f-2422">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e726f-2423">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="e726f-2423">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e726f-2424">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="e726f-2424">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e726f-2425">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e726f-2425">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e726f-2426">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e726f-2426">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e726f-2427">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e726f-2427">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e726f-2428">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e726f-2428">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e726f-2429">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e726f-2429">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e726f-2430">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e726f-2430">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e726f-2431">Geral</span><span class="sxs-lookup"><span data-stu-id="e726f-2431">General</span></span>
* <span data-ttu-id="e726f-2432">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="e726f-2432">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e726f-2433">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e726f-2433">Az.Profile</span></span>
* <span data-ttu-id="e726f-2434">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e726f-2434">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e726f-2435">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="e726f-2435">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e726f-2436">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="e726f-2436">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e726f-2437">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="e726f-2437">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e726f-2438">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="e726f-2438">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e726f-2439">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="e726f-2439">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e726f-2440">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="e726f-2440">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-2441">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2441">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-2442">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="e726f-2442">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2443">Az.Compute</span></span>
* <span data-ttu-id="e726f-2444">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e726f-2444">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e726f-2445">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="e726f-2445">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e726f-2446">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="e726f-2446">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-2447">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-2447">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-2448">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="e726f-2448">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e726f-2449">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="e726f-2449">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e726f-2450">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e726f-2450">Az.Insights</span></span>
* <span data-ttu-id="e726f-2451">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="e726f-2451">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e726f-2452">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="e726f-2452">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e726f-2453">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="e726f-2453">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e726f-2454">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="e726f-2454">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-2455">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2455">Az.Network</span></span>
* <span data-ttu-id="e726f-2456">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="e726f-2456">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e726f-2457">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e726f-2457">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e726f-2458">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e726f-2458">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e726f-2459">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e726f-2459">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e726f-2460">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e726f-2460">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e726f-2461">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e726f-2461">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e726f-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e726f-2462">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e726f-2463">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e726f-2463">Az.PolicyInsights</span></span>
* <span data-ttu-id="e726f-2464">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="e726f-2464">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2465">Az.Resources</span></span>
* <span data-ttu-id="e726f-2466">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="e726f-2466">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e726f-2467">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="e726f-2467">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e726f-2468">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e726f-2468">Az.ServiceBus</span></span>
* <span data-ttu-id="e726f-2469">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="e726f-2469">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e726f-2470">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e726f-2470">Az.ServiceFabric</span></span>
* <span data-ttu-id="e726f-2471">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="e726f-2471">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e726f-2472">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="e726f-2472">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e726f-2473">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e726f-2473">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e726f-2474">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e726f-2474">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e726f-2475">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="e726f-2475">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e726f-2476">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="e726f-2476">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e726f-2477">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e726f-2477">Az.Profile</span></span>
* <span data-ttu-id="e726f-2478">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="e726f-2478">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e726f-2479">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="e726f-2479">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2480">Az.Compute</span></span>
* <span data-ttu-id="e726f-2481">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="e726f-2481">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e726f-2482">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e726f-2482">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e726f-2483">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e726f-2483">Az.DataLakeStore</span></span>
* <span data-ttu-id="e726f-2484">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="e726f-2484">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e726f-2485">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e726f-2485">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e726f-2486">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="e726f-2486">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e726f-2487">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="e726f-2487">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e726f-2488">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e726f-2488">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-2489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2489">Az.Network</span></span>
* <span data-ttu-id="e726f-2490">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="e726f-2490">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e726f-2491">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="e726f-2491">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2492">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2492">Az.Resources</span></span>
* <span data-ttu-id="e726f-2493">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="e726f-2493">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e726f-2494">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="e726f-2494">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e726f-2495">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="e726f-2495">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e726f-2496">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e726f-2496">Azure.Storage</span></span>
* <span data-ttu-id="e726f-2497">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="e726f-2497">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e726f-2498">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e726f-2498">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e726f-2499">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e726f-2499">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e726f-2500">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e726f-2500">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e726f-2501">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e726f-2501">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e726f-2502">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e726f-2502">Az.CognitiveServices</span></span>
* <span data-ttu-id="e726f-2503">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="e726f-2503">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e726f-2504">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e726f-2504">Az.Compute</span></span>
* <span data-ttu-id="e726f-2505">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="e726f-2505">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e726f-2506">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e726f-2506">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e726f-2507">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="e726f-2507">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e726f-2508">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e726f-2508">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e726f-2509">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="e726f-2509">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e726f-2510">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e726f-2510">Az.Network</span></span>
* <span data-ttu-id="e726f-2511">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="e726f-2511">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e726f-2512">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="e726f-2512">new cmdlets added</span></span>
    - <span data-ttu-id="e726f-2513">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e726f-2513">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e726f-2514">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e726f-2514">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e726f-2515">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e726f-2515">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e726f-2516">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e726f-2516">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e726f-2517">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-2517">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e726f-2518">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-2518">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e726f-2519">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="e726f-2519">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e726f-2520">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e726f-2520">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e726f-2521">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="e726f-2521">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e726f-2522">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e726f-2522">Az.RedisCache</span></span>
* <span data-ttu-id="e726f-2523">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="e726f-2523">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e726f-2524">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="e726f-2524">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e726f-2525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e726f-2525">Az.Resources</span></span>
* <span data-ttu-id="e726f-2526">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e726f-2526">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e726f-2527">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="e726f-2527">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e726f-2528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e726f-2528">Az.Sql</span></span>
* <span data-ttu-id="e726f-2529">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="e726f-2529">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e726f-2530">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e726f-2530">Az.Websites</span></span>
* <span data-ttu-id="e726f-2531">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="e726f-2531">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e726f-2532">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="e726f-2532">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e726f-2533">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="e726f-2533">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e726f-2534">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="e726f-2534">Initial Release</span></span>
