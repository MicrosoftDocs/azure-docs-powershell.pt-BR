---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 04e85c32b1af0bbdfb622973e0900724b8e3c8e3
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244221"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="4bd31-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4bd31-103">Azure PowerShell release notes</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="4bd31-104">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-104">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="4bd31-105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-105">Az.Compute</span></span>
* <span data-ttu-id="4bd31-106">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="4bd31-106">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="4bd31-107">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-107">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-108">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-109">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="4bd31-109">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="4bd31-110">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="4bd31-110">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-111">Az.Automation</span></span>
* <span data-ttu-id="4bd31-112">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="4bd31-112">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-113">Az.Compute</span></span>
* <span data-ttu-id="4bd31-114">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="4bd31-114">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="4bd31-115">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="4bd31-115">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="4bd31-116">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="4bd31-116">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="4bd31-117">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-117">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-118">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-118">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-119">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="4bd31-119">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-120">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-121">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="4bd31-121">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-122">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-122">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-123">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="4bd31-123">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="4bd31-124">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="4bd31-124">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="4bd31-125">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="4bd31-125">Az.Maintenance</span></span>
* <span data-ttu-id="4bd31-126">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-126">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="4bd31-127">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-127">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4bd31-128">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-128">Az.ManagedServices</span></span>
* <span data-ttu-id="4bd31-129">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="4bd31-129">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-130">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-130">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-131">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="4bd31-131">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="4bd31-132">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="4bd31-132">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-133">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-133">Az.Resources</span></span>
* <span data-ttu-id="4bd31-134">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="4bd31-134">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="4bd31-135">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-135">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="4bd31-136">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-136">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="4bd31-137">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="4bd31-137">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="4bd31-138">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="4bd31-138">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="4bd31-139">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="4bd31-139">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="4bd31-140">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="4bd31-140">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="4bd31-141">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="4bd31-141">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4bd31-142">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4bd31-142">Az.SignalR</span></span>
* <span data-ttu-id="4bd31-143">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="4bd31-143">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="4bd31-144">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="4bd31-144">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-145">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-145">Az.Storage</span></span>
* <span data-ttu-id="4bd31-146">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="4bd31-146">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="4bd31-147">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="4bd31-147">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="4bd31-148">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="4bd31-148">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="4bd31-149">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="4bd31-149">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="4bd31-150">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-150">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="4bd31-151">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4bd31-151">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="4bd31-152">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="4bd31-152">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="4bd31-153">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-153">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="4bd31-154">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-154">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="4bd31-155">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="4bd31-155">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="4bd31-156">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-156">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="4bd31-157">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-157">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="4bd31-158">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-158">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="4bd31-159">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-159">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="4bd31-160">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4bd31-160">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="4bd31-161">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-161">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-162">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-163">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="4bd31-163">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="4bd31-164">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="4bd31-164">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="4bd31-165">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="4bd31-165">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="4bd31-166">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="4bd31-166">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="4bd31-167">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="4bd31-167">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="4bd31-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4bd31-168">Az.Aks</span></span>
* <span data-ttu-id="4bd31-169">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="4bd31-169">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="4bd31-170">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="4bd31-170">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-171">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-172">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-172">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="4bd31-173">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-173">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4bd31-174">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bd31-174">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4bd31-175">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="4bd31-175">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="4bd31-176">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-176">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4bd31-177">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bd31-177">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4bd31-178">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="4bd31-178">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="4bd31-179">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-179">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="4bd31-180">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-180">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4bd31-181">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bd31-181">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="4bd31-182">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-182">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="4bd31-183">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="4bd31-183">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-184">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-184">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-185">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="4bd31-185">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-186">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-186">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-187">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="4bd31-187">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-188">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-189">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="4bd31-189">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="4bd31-190">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4bd31-190">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="4bd31-191">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-191">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="4bd31-192">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="4bd31-192">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="4bd31-193">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4bd31-193">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="4bd31-194">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-194">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="4bd31-195">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4bd31-195">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-196">Az.Network</span></span>
* <span data-ttu-id="4bd31-197">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="4bd31-197">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="4bd31-198">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="4bd31-198">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="4bd31-199">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="4bd31-199">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="4bd31-200">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="4bd31-200">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-201">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-202">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="4bd31-202">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="4bd31-203">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="4bd31-203">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="4bd31-204">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4bd31-204">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-206">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-206">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-207">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-207">Az.Resources</span></span>
* <span data-ttu-id="4bd31-208">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4bd31-208">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="4bd31-209">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="4bd31-209">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-210">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-210">Az.Sql</span></span>
* <span data-ttu-id="4bd31-211">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="4bd31-211">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4bd31-212">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4bd31-212">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-213">Az.Storage</span></span>
* <span data-ttu-id="4bd31-214">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="4bd31-214">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="4bd31-215">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="4bd31-215">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="4bd31-216">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4bd31-216">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="4bd31-217">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="4bd31-217">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="4bd31-218">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="4bd31-218">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="4bd31-219">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="4bd31-219">Supported get single file share usage</span></span>
    - <span data-ttu-id="4bd31-220">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-220">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="4bd31-221">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-221">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-222">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-223">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-223">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="4bd31-224">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="4bd31-224">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4bd31-225">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4bd31-225">Az.Aks</span></span>
* <span data-ttu-id="4bd31-226">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="4bd31-226">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4bd31-227">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-227">Az.AnalysisServices</span></span>
* <span data-ttu-id="4bd31-228">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="4bd31-228">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-229">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-229">Az.Automation</span></span>
* <span data-ttu-id="4bd31-230">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="4bd31-230">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-231">Az.Compute</span></span>
* <span data-ttu-id="4bd31-232">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="4bd31-232">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-233">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-233">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-234">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4bd31-234">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4bd31-235">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4bd31-235">Az.EventGrid</span></span>
* <span data-ttu-id="4bd31-236">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="4bd31-236">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="4bd31-237">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-237">Added new features:</span></span>
    - <span data-ttu-id="4bd31-238">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="4bd31-238">Input mapping</span></span>
    - <span data-ttu-id="4bd31-239">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="4bd31-239">Event Delivery Schema</span></span>
    - <span data-ttu-id="4bd31-240">Link Privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-240">Private Link</span></span>
    - <span data-ttu-id="4bd31-241">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="4bd31-241">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="4bd31-242">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="4bd31-242">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="4bd31-243">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="4bd31-243">Azure Function As Destination</span></span>
    - <span data-ttu-id="4bd31-244">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="4bd31-244">WebHook Batching</span></span>
    - <span data-ttu-id="4bd31-245">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="4bd31-245">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="4bd31-246">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="4bd31-246">IpFiltering</span></span>
* <span data-ttu-id="4bd31-247">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-247">Updated cmdlets:</span></span>
    - <span data-ttu-id="4bd31-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="4bd31-248">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="4bd31-249">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="4bd31-249">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="4bd31-250">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="4bd31-250">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="4bd31-251">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-251">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="4bd31-252">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="4bd31-252">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="4bd31-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="4bd31-253">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4bd31-254">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="4bd31-254">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="4bd31-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="4bd31-255">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="4bd31-256">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-256">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-257">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-257">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-258">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="4bd31-258">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="4bd31-259">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="4bd31-259">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-260">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-260">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-261">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="4bd31-261">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-262">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-262">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-263">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="4bd31-263">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-264">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-264">Az.Network</span></span>
* <span data-ttu-id="4bd31-265">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="4bd31-265">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="4bd31-266">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-266">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="4bd31-267">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4bd31-267">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4bd31-268">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4bd31-268">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4bd31-269">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4bd31-269">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4bd31-270">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="4bd31-270">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="4bd31-271">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="4bd31-271">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="4bd31-272">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-272">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="4bd31-273">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4bd31-273">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4bd31-274">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4bd31-274">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4bd31-275">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4bd31-275">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4bd31-276">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="4bd31-276">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="4bd31-277">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="4bd31-277">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="4bd31-278">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="4bd31-278">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="4bd31-279">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-279">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4bd31-280">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-280">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="4bd31-281">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-281">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-282">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-282">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-283">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="4bd31-283">Removed project reference to Authentication</span></span>
* <span data-ttu-id="4bd31-284">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="4bd31-284">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="4bd31-285">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-285">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-286">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-286">Az.Resources</span></span>
* <span data-ttu-id="4bd31-287">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="4bd31-287">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="4bd31-288">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-288">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-289">Az.Sql</span></span>
* <span data-ttu-id="4bd31-290">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="4bd31-290">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="4bd31-291">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-291">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="4bd31-292">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="4bd31-292">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-293">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-293">Az.Storage</span></span>
* <span data-ttu-id="4bd31-294">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-294">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="4bd31-295">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="4bd31-295">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="4bd31-296">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-296">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4bd31-297">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-297">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4bd31-298">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-298">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="4bd31-299">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="4bd31-299">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="4bd31-300">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="4bd31-300">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="4bd31-301">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4bd31-301">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="4bd31-302">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="4bd31-302">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="4bd31-303">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4bd31-303">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="4bd31-304">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4bd31-304">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="4bd31-305">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="4bd31-305">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="4bd31-306">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-306">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4bd31-307">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="4bd31-307">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="4bd31-308">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="4bd31-308">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="4bd31-309">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-309">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="4bd31-310">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-310">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4bd31-311">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4bd31-311">Az.StorageSync</span></span>
* <span data-ttu-id="4bd31-312">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="4bd31-312">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="4bd31-313">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-313">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="4bd31-314">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="4bd31-314">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="4bd31-315">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="4bd31-315">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-316">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-316">Az.Websites</span></span>
* <span data-ttu-id="4bd31-317">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4bd31-317">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="4bd31-318">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-318">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-319">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-320">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-320">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="4bd31-321">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="4bd31-321">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="4bd31-322">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="4bd31-322">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="4bd31-323">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="4bd31-323">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="4bd31-324">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4bd31-324">Az.Aks</span></span>
* <span data-ttu-id="4bd31-325">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="4bd31-325">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4bd31-326">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-326">Az.Batch</span></span>
* <span data-ttu-id="4bd31-327">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="4bd31-327">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="4bd31-328">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-328">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-329">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-329">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-330">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="4bd31-330">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="4bd31-331">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="4bd31-331">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-332">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-332">Az.Compute</span></span>
* <span data-ttu-id="4bd31-333">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4bd31-333">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="4bd31-334">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4bd31-334">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="4bd31-335">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="4bd31-335">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="4bd31-336">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4bd31-336">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="4bd31-337">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="4bd31-337">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-338">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-338">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-339">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-339">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-340">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-341">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="4bd31-341">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4bd31-342">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4bd31-342">Az.Functions</span></span>
* <span data-ttu-id="4bd31-343">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="4bd31-343">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-344">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-344">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-345">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4bd31-345">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4bd31-346">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4bd31-346">Az.HealthcareApis</span></span>
* <span data-ttu-id="4bd31-347">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-347">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="4bd31-348">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="4bd31-348">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-349">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-349">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-350">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="4bd31-350">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="4bd31-351">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="4bd31-351">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-352">Az.Network</span></span>
* <span data-ttu-id="4bd31-353">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="4bd31-353">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="4bd31-354">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-354">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4bd31-355">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="4bd31-355">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="4bd31-356">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4bd31-356">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="4bd31-357">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="4bd31-357">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="4bd31-358">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="4bd31-358">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="4bd31-359">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4bd31-359">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4bd31-360">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4bd31-360">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4bd31-361">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4bd31-361">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="4bd31-362">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="4bd31-362">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="4bd31-363">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="4bd31-363">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="4bd31-364">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-364">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="4bd31-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="4bd31-365">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="4bd31-366">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-366">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="4bd31-367">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4bd31-367">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="4bd31-368">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="4bd31-368">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="4bd31-369">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="4bd31-369">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="4bd31-370">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-370">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="4bd31-371">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="4bd31-371">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="4bd31-372">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="4bd31-372">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="4bd31-373">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4bd31-373">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="4bd31-374">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="4bd31-374">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="4bd31-375">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="4bd31-375">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="4bd31-376">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-376">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="4bd31-377">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4bd31-377">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4bd31-378">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4bd31-378">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="4bd31-379">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-379">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="4bd31-380">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4bd31-380">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="4bd31-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-381">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4bd31-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-382">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4bd31-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-383">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4bd31-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-384">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4bd31-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-385">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="4bd31-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-386">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="4bd31-387">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="4bd31-387">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="4bd31-388">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="4bd31-388">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="4bd31-389">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4bd31-389">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4bd31-390">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4bd31-390">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4bd31-391">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4bd31-391">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="4bd31-392">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="4bd31-392">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="4bd31-393">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="4bd31-393">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="4bd31-394">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-394">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4bd31-395">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-395">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="4bd31-396">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-396">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4bd31-397">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-397">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4bd31-398">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-398">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="4bd31-399">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-399">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="4bd31-400">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="4bd31-400">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="4bd31-401">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="4bd31-401">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-402">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-402">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-403">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="4bd31-403">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="4bd31-404">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4bd31-404">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="4bd31-405">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="4bd31-405">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="4bd31-406">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4bd31-406">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4bd31-407">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4bd31-407">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-408">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-408">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-409">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-409">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="4bd31-410">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="4bd31-410">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-411">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-411">Az.Resources</span></span>
* <span data-ttu-id="4bd31-412">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="4bd31-412">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="4bd31-413">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="4bd31-413">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="4bd31-414">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4bd31-414">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="4bd31-415">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-415">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="4bd31-416">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="4bd31-416">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="4bd31-417">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="4bd31-417">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-418">Az.Sql</span></span>
* <span data-ttu-id="4bd31-419">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4bd31-419">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="4bd31-420">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-420">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="4bd31-421">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="4bd31-421">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-422">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-422">Az.Storage</span></span>
* <span data-ttu-id="4bd31-423">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="4bd31-423">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="4bd31-424">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-424">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="4bd31-425">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-425">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-426">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-426">Az.Websites</span></span>
* <span data-ttu-id="4bd31-427">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="4bd31-427">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4bd31-428">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="4bd31-428">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="4bd31-429">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="4bd31-429">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="4bd31-430">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-430">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="4bd31-431">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="4bd31-431">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="4bd31-432">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="4bd31-432">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="4bd31-433">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-433">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-434">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-434">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-435">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="4bd31-435">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4bd31-436">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-436">Az.AnalysisServices</span></span>
* <span data-ttu-id="4bd31-437">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-437">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-438">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-439">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-439">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="4bd31-440">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4bd31-440">Az.Billing</span></span>
* <span data-ttu-id="4bd31-441">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-441">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-442">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-442">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-443">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="4bd31-443">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-444">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-445">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-445">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="4bd31-446">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-446">Az.DataShare</span></span>
* <span data-ttu-id="4bd31-447">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="4bd31-447">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="4bd31-448">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="4bd31-448">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="4bd31-449">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="4bd31-449">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-450">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-450">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-451">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-451">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="4bd31-452">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="4bd31-452">Added optional parameters to</span></span> 
    - <span data-ttu-id="4bd31-453">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4bd31-453">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="4bd31-454">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="4bd31-454">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-455">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-455">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-456">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="4bd31-456">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4bd31-457">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4bd31-457">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4bd31-458">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-458">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4bd31-459">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4bd31-459">Az.PrivateDns</span></span>
* <span data-ttu-id="4bd31-460">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-460">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-461">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-461">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-462">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="4bd31-462">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="4bd31-463">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4bd31-463">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-464">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-464">Az.Resources</span></span>
* <span data-ttu-id="4bd31-465">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="4bd31-465">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="4bd31-466">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="4bd31-466">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="4bd31-467">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-467">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="4bd31-468">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd31-468">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="4bd31-469">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-469">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-470">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-470">Az.Sql</span></span>
* <span data-ttu-id="4bd31-471">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="4bd31-471">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4bd31-472">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="4bd31-472">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="4bd31-473">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="4bd31-473">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-474">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-474">Az.Storage</span></span>
* <span data-ttu-id="4bd31-475">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-475">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="4bd31-476">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-476">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4bd31-477">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="4bd31-477">Highlights since the last release</span></span>
* <span data-ttu-id="4bd31-478">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4bd31-478">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="4bd31-479">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4bd31-479">General availability of Az.Functions</span></span> 
* <span data-ttu-id="4bd31-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="4bd31-480">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-481">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-482">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="4bd31-482">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="4bd31-483">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="4bd31-483">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="4bd31-484">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4bd31-484">Az.Aks</span></span>
* <span data-ttu-id="4bd31-485">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="4bd31-485">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="4bd31-486">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="4bd31-486">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="4bd31-487">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="4bd31-487">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-488">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-489">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="4bd31-489">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="4bd31-490">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="4bd31-490">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="4bd31-491">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-491">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4bd31-492">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4bd31-492">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4bd31-493">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-493">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4bd31-494">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4bd31-494">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="4bd31-495">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-495">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4bd31-496">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4bd31-496">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4bd31-497">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-497">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="4bd31-498">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="4bd31-498">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="4bd31-499">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4bd31-499">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="4bd31-500">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="4bd31-500">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="4bd31-501">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="4bd31-501">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="4bd31-502">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4bd31-502">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="4bd31-503">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="4bd31-503">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="4bd31-504">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="4bd31-504">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4bd31-505">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-505">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4bd31-506">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="4bd31-506">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="4bd31-507">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="4bd31-507">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="4bd31-508">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="4bd31-508">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4bd31-509">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-509">Az.Batch</span></span>
* <span data-ttu-id="4bd31-510">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="4bd31-510">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="4bd31-511">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-511">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="4bd31-512">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="4bd31-512">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="4bd31-513">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-513">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="4bd31-514">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-514">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="4bd31-515">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-515">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="4bd31-516">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-516">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="4bd31-517">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-517">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="4bd31-518">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-518">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-519">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-519">Az.Compute</span></span>
* <span data-ttu-id="4bd31-520">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="4bd31-520">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="4bd31-521">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-521">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="4bd31-522">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4bd31-522">Breaking changes</span></span>
    - <span data-ttu-id="4bd31-523">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-523">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="4bd31-524">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-524">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="4bd31-525">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-525">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="4bd31-526">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="4bd31-526">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="4bd31-527">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="4bd31-527">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="4bd31-528">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="4bd31-528">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="4bd31-529">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="4bd31-529">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-530">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-530">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-531">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-531">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-532">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-532">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-533">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="4bd31-533">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4bd31-534">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="4bd31-534">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="4bd31-535">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="4bd31-535">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="4bd31-536">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="4bd31-536">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="4bd31-537">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="4bd31-537">Az.Functions</span></span>
* <span data-ttu-id="4bd31-538">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="4bd31-538">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-539">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-539">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-540">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="4bd31-540">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4bd31-541">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4bd31-541">Az.HealthcareApis</span></span>
* <span data-ttu-id="4bd31-542">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="4bd31-542">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-543">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-543">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-544">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="4bd31-544">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="4bd31-545">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="4bd31-545">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="4bd31-546">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="4bd31-546">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="4bd31-547">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="4bd31-547">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="4bd31-548">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="4bd31-548">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="4bd31-549">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-549">New cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-550">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-550">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4bd31-551">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-551">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4bd31-552">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-552">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="4bd31-553">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-553">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="4bd31-554">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="4bd31-554">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="4bd31-555">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-555">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-556">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-556">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-557">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="4bd31-557">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="4bd31-558">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4bd31-558">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="4bd31-559">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="4bd31-559">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="4bd31-560">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="4bd31-560">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="4bd31-561">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="4bd31-561">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="4bd31-562">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="4bd31-562">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="4bd31-563">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="4bd31-563">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-564">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-564">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-565">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="4bd31-565">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="4bd31-566">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="4bd31-566">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="4bd31-567">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="4bd31-567">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="4bd31-568">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="4bd31-568">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="4bd31-569">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="4bd31-569">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="4bd31-570">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="4bd31-570">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="4bd31-571">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="4bd31-571">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-572">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-572">Az.Network</span></span>
* <span data-ttu-id="4bd31-573">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="4bd31-573">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="4bd31-574">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="4bd31-574">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="4bd31-575">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="4bd31-575">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="4bd31-576">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="4bd31-576">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="4bd31-577">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4bd31-577">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="4bd31-578">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-578">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-579">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4bd31-579">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4bd31-580">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4bd31-580">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4bd31-581">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4bd31-581">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="4bd31-582">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="4bd31-582">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="4bd31-583">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-583">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="4bd31-584">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-584">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="4bd31-585">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="4bd31-585">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="4bd31-586">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="4bd31-586">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="4bd31-587">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="4bd31-587">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="4bd31-588">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-588">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="4bd31-589">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="4bd31-589">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="4bd31-590">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4bd31-590">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4bd31-591">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4bd31-591">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4bd31-592">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4bd31-592">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="4bd31-593">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="4bd31-593">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="4bd31-594">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="4bd31-594">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="4bd31-595">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="4bd31-595">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="4bd31-596">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4bd31-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="4bd31-597">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4bd31-597">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-598">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-598">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-599">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="4bd31-599">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="4bd31-600">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="4bd31-600">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="4bd31-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="4bd31-601">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="4bd31-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="4bd31-602">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="4bd31-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="4bd31-603">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="4bd31-604">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4bd31-604">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="4bd31-605">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="4bd31-605">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="4bd31-606">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="4bd31-606">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-607">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-607">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-608">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-608">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="4bd31-609">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="4bd31-609">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="4bd31-610">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="4bd31-610">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="4bd31-611">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-611">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="4bd31-612">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="4bd31-612">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-613">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-613">Az.Resources</span></span>
* <span data-ttu-id="4bd31-614">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="4bd31-614">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="4bd31-615">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="4bd31-615">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="4bd31-616">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="4bd31-616">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="4bd31-617">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="4bd31-617">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="4bd31-618">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4bd31-618">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="4bd31-619">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="4bd31-619">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="4bd31-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="4bd31-620">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="4bd31-621">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="4bd31-621">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="4bd31-622">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="4bd31-622">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="4bd31-623">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="4bd31-623">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="4bd31-624">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="4bd31-624">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="4bd31-625">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="4bd31-625">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="4bd31-626">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="4bd31-626">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="4bd31-627">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="4bd31-627">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="4bd31-628">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="4bd31-628">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="4bd31-629">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="4bd31-629">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="4bd31-630">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-630">'New-AzDeployment'</span></span>
    - <span data-ttu-id="4bd31-631">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-631">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="4bd31-632">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-632">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4bd31-633">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-633">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-634">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-634">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-635">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="4bd31-635">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-636">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-636">Az.Sql</span></span>
* <span data-ttu-id="4bd31-637">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="4bd31-637">Enhance performance of:</span></span>
    - <span data-ttu-id="4bd31-638">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4bd31-638">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4bd31-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4bd31-639">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4bd31-640">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4bd31-640">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4bd31-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="4bd31-641">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="4bd31-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4bd31-642">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4bd31-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4bd31-643">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4bd31-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4bd31-644">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="4bd31-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="4bd31-645">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="4bd31-646">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-646">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="4bd31-647">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="4bd31-647">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-648">Az.Storage</span></span>
* <span data-ttu-id="4bd31-649">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-649">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="4bd31-650">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="4bd31-650">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="4bd31-651">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-651">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4bd31-652">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="4bd31-652">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="4bd31-653">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4bd31-653">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4bd31-654">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="4bd31-654">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="4bd31-655">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="4bd31-655">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="4bd31-656">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="4bd31-656">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="4bd31-657">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="4bd31-657">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="4bd31-658">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="4bd31-658">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="4bd31-659">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="4bd31-659">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="4bd31-660">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="4bd31-660">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="4bd31-661">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="4bd31-661">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="4bd31-662">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-662">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="4bd31-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="4bd31-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4bd31-665">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-665">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="4bd31-666">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4bd31-666">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="4bd31-667">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4bd31-667">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4bd31-668">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="4bd31-668">Supported failover Storage account</span></span>
    - <span data-ttu-id="4bd31-669">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="4bd31-669">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="4bd31-670">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-670">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="4bd31-671">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-671">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="4bd31-672">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="4bd31-672">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="4bd31-673">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4bd31-673">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4bd31-674">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="4bd31-674">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="4bd31-675">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="4bd31-675">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="4bd31-676">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-676">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4bd31-677">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-677">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="4bd31-678">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-678">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="4bd31-679">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4bd31-679">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4bd31-680">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4bd31-680">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="4bd31-681">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="4bd31-681">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="4bd31-682">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4bd31-682">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="4bd31-683">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4bd31-683">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="4bd31-684">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4bd31-684">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="4bd31-685">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="4bd31-685">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="4bd31-686">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="4bd31-686">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="4bd31-687">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="4bd31-687">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4bd31-688">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4bd31-688">Az.TrafficManager</span></span>
* <span data-ttu-id="4bd31-689">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="4bd31-689">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-690">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-690">Az.Websites</span></span>
* <span data-ttu-id="4bd31-691">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-691">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="4bd31-692">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-692">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="4bd31-693">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="4bd31-693">Highlights since the last release</span></span>
* <span data-ttu-id="4bd31-694">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="4bd31-694">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-695">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-695">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-696">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="4bd31-696">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-697">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-698">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4bd31-698">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4bd31-699">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="4bd31-699">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4bd31-700">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-700">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-701">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="4bd31-701">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-702">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-702">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-703">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="4bd31-703">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-704">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-704">Az.Compute</span></span>
* <span data-ttu-id="4bd31-705">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-705">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="4bd31-706">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="4bd31-706">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-707">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-707">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-708">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-708">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-709">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="4bd31-709">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="4bd31-710">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="4bd31-710">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="4bd31-711">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="4bd31-711">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="4bd31-712">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-712">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-713">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="4bd31-713">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="4bd31-714">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="4bd31-714">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="4bd31-715">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="4bd31-715">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="4bd31-716">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-716">New cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-717">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-717">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4bd31-718">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-718">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4bd31-719">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-719">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="4bd31-720">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-720">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="4bd31-721">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="4bd31-721">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-722">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-722">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-723">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="4bd31-723">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="4bd31-724">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="4bd31-724">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="4bd31-725">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="4bd31-725">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="4bd31-726">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-726">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="4bd31-727">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="4bd31-727">Az.Maintenance</span></span>
* <span data-ttu-id="4bd31-728">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-728">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-729">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-729">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-730">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-730">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="4bd31-731">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4bd31-731">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4bd31-732">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4bd31-732">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4bd31-733">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4bd31-733">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4bd31-734">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="4bd31-734">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="4bd31-735">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4bd31-735">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4bd31-736">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4bd31-736">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="4bd31-737">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="4bd31-737">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-738">Az.Network</span></span>
* <span data-ttu-id="4bd31-739">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="4bd31-739">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="4bd31-740">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4bd31-740">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4bd31-741">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4bd31-741">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="4bd31-742">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-742">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="4bd31-743">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-743">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="4bd31-744">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="4bd31-744">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="4bd31-745">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="4bd31-745">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="4bd31-746">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="4bd31-746">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="4bd31-747">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="4bd31-747">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="4bd31-748">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-748">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4bd31-749">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="4bd31-749">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="4bd31-750">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="4bd31-750">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="4bd31-751">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="4bd31-751">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="4bd31-752">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="4bd31-752">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="4bd31-753">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-753">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="4bd31-754">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-754">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-755">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-755">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-756">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="4bd31-756">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="4bd31-757">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="4bd31-757">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-758">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-758">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-759">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="4bd31-759">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-760">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-760">Az.Sql</span></span>
* <span data-ttu-id="4bd31-761">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-761">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="4bd31-762">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="4bd31-762">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-763">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-763">Az.Storage</span></span>
* <span data-ttu-id="4bd31-764">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4bd31-764">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="4bd31-765">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-765">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="4bd31-766">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-766">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="4bd31-767">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-767">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="4bd31-768">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="4bd31-768">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="4bd31-769">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4bd31-769">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4bd31-770">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4bd31-770">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4bd31-771">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="4bd31-771">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="4bd31-772">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4bd31-772">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4bd31-773">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="4bd31-773">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="4bd31-774">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4bd31-774">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="4bd31-775">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-775">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="4bd31-776">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="4bd31-776">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="4bd31-777">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-777">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="4bd31-778">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-778">General</span></span>
* <span data-ttu-id="4bd31-779">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="4bd31-779">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="4bd31-780">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="4bd31-780">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="4bd31-781">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="4bd31-781">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="4bd31-782">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="4bd31-782">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="4bd31-783">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4bd31-783">Az.Billing</span></span>
  - <span data-ttu-id="4bd31-784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-784">Az.Compute</span></span>
  - <span data-ttu-id="4bd31-785">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4bd31-785">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="4bd31-786">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-786">Az.EventHub</span></span>
  - <span data-ttu-id="4bd31-787">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-787">Az.IotHub</span></span>
  - <span data-ttu-id="4bd31-788">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-788">Az.KeyVault</span></span>
  - <span data-ttu-id="4bd31-789">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-789">Az.Monitor</span></span>
  - <span data-ttu-id="4bd31-790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-790">Az.Network</span></span>
  - <span data-ttu-id="4bd31-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-791">Az.Resources</span></span>
  - <span data-ttu-id="4bd31-792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-792">Az.Storage</span></span>
  - <span data-ttu-id="4bd31-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-793">Az.Websites</span></span>
* <span data-ttu-id="4bd31-794">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-794">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="4bd31-795">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4bd31-795">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="4bd31-796">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="4bd31-796">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="4bd31-797">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-797">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-798">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-798">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-799">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="4bd31-799">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-800">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-800">Az.Compute</span></span>
* <span data-ttu-id="4bd31-801">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="4bd31-801">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="4bd31-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="4bd31-802">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="4bd31-803">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-803">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="4bd31-804">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-804">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="4bd31-805">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="4bd31-805">[#11354]</span></span>
* <span data-ttu-id="4bd31-806">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="4bd31-806">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="4bd31-807">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4bd31-807">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4bd31-808">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4bd31-808">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4bd31-809">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4bd31-809">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="4bd31-810">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="4bd31-810">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="4bd31-811">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-811">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="4bd31-812">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="4bd31-812">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="4bd31-813">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-813">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="4bd31-814">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="4bd31-814">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-815">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-816">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-816">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="4bd31-817">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="4bd31-817">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-818">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-818">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-819">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="4bd31-819">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="4bd31-820">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-820">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-821">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-821">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-822">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="4bd31-822">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-823">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-823">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-824">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bd31-824">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="4bd31-825">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-825">New Cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-826">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="4bd31-826">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="4bd31-827">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="4bd31-827">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-828">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-828">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-829">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="4bd31-829">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-830">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-830">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-831">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="4bd31-831">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-832">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-832">Az.Network</span></span>
* <span data-ttu-id="4bd31-833">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="4bd31-833">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="4bd31-834">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-834">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4bd31-835">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="4bd31-835">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="4bd31-836">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="4bd31-836">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="4bd31-837">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="4bd31-837">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="4bd31-838">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="4bd31-838">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-839">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-839">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-840">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="4bd31-840">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-841">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-841">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-842">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="4bd31-842">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="4bd31-843">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="4bd31-843">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="4bd31-844">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="4bd31-844">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="4bd31-845">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="4bd31-845">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="4bd31-846">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-846">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="4bd31-847">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="4bd31-847">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-848">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-848">Az.Resources</span></span>
* <span data-ttu-id="4bd31-849">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="4bd31-849">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="4bd31-850">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="4bd31-850">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="4bd31-851">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-851">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="4bd31-852">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-852">Added example.</span></span>
* <span data-ttu-id="4bd31-853">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="4bd31-853">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="4bd31-854">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="4bd31-854">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-855">Az.Sql</span></span>
* <span data-ttu-id="4bd31-856">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="4bd31-856">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="4bd31-857">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-857">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="4bd31-858">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-858">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="4bd31-859">Az.Support</span><span class="sxs-lookup"><span data-stu-id="4bd31-859">Az.Support</span></span>
* <span data-ttu-id="4bd31-860">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="4bd31-860">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-861">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-861">Az.Websites</span></span>
* <span data-ttu-id="4bd31-862">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="4bd31-862">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="4bd31-863">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4bd31-863">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4bd31-864">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4bd31-864">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4bd31-865">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4bd31-865">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="4bd31-866">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="4bd31-866">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="4bd31-867">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-867">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-868">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-869">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="4bd31-869">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="4bd31-870">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="4bd31-870">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="4bd31-871">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="4bd31-871">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-872">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-873">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="4bd31-873">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="4bd31-874">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="4bd31-874">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="4bd31-875">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="4bd31-875">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="4bd31-876">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="4bd31-876">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-877">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-877">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-878">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="4bd31-878">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-879">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-880">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4bd31-880">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4bd31-881">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-881">New Cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-882">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-882">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4bd31-883">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-883">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4bd31-884">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-884">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4bd31-885">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-885">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="4bd31-886">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4bd31-886">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="4bd31-887">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-887">New Cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-888">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4bd31-888">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="4bd31-889">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4bd31-889">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="4bd31-890">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4bd31-890">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="4bd31-891">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="4bd31-891">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="4bd31-892">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4bd31-892">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4bd31-893">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4bd31-893">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="4bd31-894">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="4bd31-894">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="4bd31-895">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-895">New Cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-896">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-896">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="4bd31-897">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="4bd31-897">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="4bd31-898">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4bd31-898">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-899">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-899">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-900">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="4bd31-900">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-901">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-901">Az.Network</span></span>
* <span data-ttu-id="4bd31-902">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="4bd31-902">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="4bd31-903">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="4bd31-903">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="4bd31-904">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="4bd31-904">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="4bd31-905">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-905">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-906">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-906">Az.Resources</span></span>
* <span data-ttu-id="4bd31-907">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-907">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="4bd31-908">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="4bd31-908">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="4bd31-909">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="4bd31-909">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="4bd31-910">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="4bd31-910">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="4bd31-911">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="4bd31-911">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="4bd31-912">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="4bd31-912">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="4bd31-913">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="4bd31-913">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="4bd31-914">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd31-914">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="4bd31-915">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd31-915">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4bd31-916">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd31-916">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="4bd31-917">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd31-917">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="4bd31-918">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-918">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="4bd31-919">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd31-919">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="4bd31-920">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-920">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-921">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-921">Az.Sql</span></span>
* <span data-ttu-id="4bd31-922">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-922">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="4bd31-923">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4bd31-923">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="4bd31-924">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4bd31-924">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="4bd31-925">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="4bd31-925">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="4bd31-926">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="4bd31-926">Remove an LTR backup</span></span>
    - <span data-ttu-id="4bd31-927">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="4bd31-927">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="4bd31-928">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="4bd31-928">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="4bd31-929">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-929">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="4bd31-930">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-930">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-931">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-931">Az.Storage</span></span>
* <span data-ttu-id="4bd31-932">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-932">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="4bd31-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-933">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="4bd31-934">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4bd31-934">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="4bd31-935">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="4bd31-935">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="4bd31-936">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="4bd31-936">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-937">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-937">Az.Websites</span></span>
* <span data-ttu-id="4bd31-938">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="4bd31-938">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="4bd31-939">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="4bd31-939">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="4bd31-940">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4bd31-940">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="4bd31-941">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="4bd31-941">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="4bd31-942">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4bd31-942">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="4bd31-943">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-943">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4bd31-944">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4bd31-944">Highlights since the last major release</span></span>
* <span data-ttu-id="4bd31-945">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-945">Updated client side telemetry.</span></span>
* <span data-ttu-id="4bd31-946">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-946">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="4bd31-947">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="4bd31-947">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-948">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-948">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-949">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="4bd31-949">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-950">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-950">Az.Automation</span></span>
* <span data-ttu-id="4bd31-951">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="4bd31-951">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-952">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-952">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-953">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-953">Updated SDK to 7.0</span></span>
* <span data-ttu-id="4bd31-954">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="4bd31-954">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-955">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-955">Az.Compute</span></span>
* <span data-ttu-id="4bd31-956">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="4bd31-956">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-957">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-957">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-958">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="4bd31-958">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-959">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-959">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-960">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="4bd31-960">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="4bd31-961">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-961">New Cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-962">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-962">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4bd31-963">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-963">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4bd31-964">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-964">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="4bd31-965">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="4bd31-965">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-966">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-966">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-967">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="4bd31-967">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-968">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-968">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-969">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="4bd31-969">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="4bd31-970">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-970">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="4bd31-971">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="4bd31-971">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-972">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-972">Az.Network</span></span>
* <span data-ttu-id="4bd31-973">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-973">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="4bd31-974">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4bd31-974">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4bd31-975">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="4bd31-975">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="4bd31-976">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="4bd31-976">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="4bd31-977">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-977">No new cmdlets are added.</span></span> <span data-ttu-id="4bd31-978">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="4bd31-978">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-980">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="4bd31-980">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-981">Az.Resources</span></span>
* <span data-ttu-id="4bd31-982">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="4bd31-982">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="4bd31-983">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4bd31-983">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="4bd31-984">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="4bd31-984">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="4bd31-985">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="4bd31-985">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="4bd31-986">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4bd31-986">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="4bd31-987">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="4bd31-987">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="4bd31-988">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="4bd31-988">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="4bd31-989">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-989">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-990">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-990">Az.Sql</span></span>
* <span data-ttu-id="4bd31-991">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-991">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="4bd31-992">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="4bd31-992">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="4bd31-993">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="4bd31-993">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4bd31-994">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4bd31-994">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4bd31-995">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4bd31-995">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4bd31-996">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4bd31-996">Az.StorageSync</span></span>
* <span data-ttu-id="4bd31-997">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-997">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="4bd31-998">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-998">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4bd31-999">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4bd31-999">Highlights since the last major release</span></span>
* <span data-ttu-id="4bd31-1000">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4bd31-1000">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="4bd31-1001">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1001">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1002">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1002">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1003">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="4bd31-1003">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="4bd31-1004">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="4bd31-1004">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-1005">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-1005">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-1006">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="4bd31-1006">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="4bd31-1007">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="4bd31-1007">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="4bd31-1008">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="4bd31-1008">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="4bd31-1009">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1009">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1010">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1011">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1011">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="4bd31-1012">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1012">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="4bd31-1013">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1013">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="4bd31-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1014">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="4bd31-1015">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1015">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1016">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1016">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1017">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1017">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4bd31-1018">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4bd31-1018">Az.DeploymentManager</span></span>
* <span data-ttu-id="4bd31-1019">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1019">Adds LIST operations for resources</span></span>
* <span data-ttu-id="4bd31-1020">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="4bd31-1020">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-1021">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-1021">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-1022">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1022">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-1023">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-1023">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-1024">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1024">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1025">Az.Network</span></span>
* <span data-ttu-id="4bd31-1026">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1026">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="4bd31-1027">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-1027">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="4bd31-1028">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1028">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4bd31-1029">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="4bd31-1029">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="4bd31-1030">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1030">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="4bd31-1031">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1031">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="4bd31-1032">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1032">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="4bd31-1033">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1033">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="4bd31-1034">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1034">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-1035">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="4bd31-1036">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-1036">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="4bd31-1037">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1037">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="4bd31-1038">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="4bd31-1038">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-1039">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1039">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-1040">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="4bd31-1040">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="4bd31-1041">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="4bd31-1041">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="4bd31-1042">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="4bd31-1042">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="4bd31-1043">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="4bd31-1043">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1044">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1044">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1045">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1045">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="4bd31-1046">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1046">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1047">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1047">Az.Resources</span></span>
* <span data-ttu-id="4bd31-1048">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="4bd31-1048">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="4bd31-1049">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="4bd31-1049">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1050">Az.Sql</span></span>
<span data-ttu-id="4bd31-1051">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1051">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1052">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1052">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1053">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-1053">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="4bd31-1054">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1054">New-AzStorageAccount</span></span>
* <span data-ttu-id="4bd31-1055">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="4bd31-1055">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="4bd31-1056">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1056">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-1057">Az.Websites</span></span>
* <span data-ttu-id="4bd31-1058">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="4bd31-1058">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="4bd31-1059">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="4bd31-1059">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="4bd31-1060">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="4bd31-1060">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1061">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1061">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1062">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4bd31-1062">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4bd31-1063">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-1063">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-1064">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4bd31-1064">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1065">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1065">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1066">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1066">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4bd31-1067">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-1067">Az.ContainerInstance</span></span>
* <span data-ttu-id="4bd31-1068">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1068">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4bd31-1069">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1069">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4bd31-1070">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1070">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4bd31-1071">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1071">Get the Edge Storage Container</span></span>
* <span data-ttu-id="4bd31-1072">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1072">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4bd31-1073">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1073">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="4bd31-1074">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1074">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4bd31-1075">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1075">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="4bd31-1076">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1076">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="4bd31-1077">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1077">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="4bd31-1078">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1078">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4bd31-1079">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1079">Get the Edge Storage Account</span></span>
* <span data-ttu-id="4bd31-1080">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1080">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4bd31-1081">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1081">Create new Edge Storage Account</span></span>
* <span data-ttu-id="4bd31-1082">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1082">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="4bd31-1083">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1083">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="4bd31-1084">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1084">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="4bd31-1085">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-1085">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="4bd31-1086">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1086">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="4bd31-1087">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1087">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1088">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1088">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1089">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4bd31-1089">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="4bd31-1090">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1090">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="4bd31-1091">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1091">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="4bd31-1092">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="4bd31-1092">Az.DevTestLabs</span></span>
* <span data-ttu-id="4bd31-1093">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="4bd31-1093">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-1094">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1094">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-1095">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="4bd31-1095">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-1096">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-1096">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-1097">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1097">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4bd31-1098">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4bd31-1098">Az.MachineLearning</span></span>
* <span data-ttu-id="4bd31-1099">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="4bd31-1099">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="4bd31-1100">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4bd31-1100">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="4bd31-1101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="4bd31-1101">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="4bd31-1102">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4bd31-1102">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="4bd31-1103">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4bd31-1103">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="4bd31-1104">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="4bd31-1104">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="4bd31-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="4bd31-1105">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="4bd31-1106">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1106">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1107">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1107">Az.Network</span></span>
* <span data-ttu-id="4bd31-1108">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="4bd31-1108">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1109">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1109">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1110">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1110">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="4bd31-1111">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1111">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4bd31-1112">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1112">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="4bd31-1113">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1113">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1114">Az.Resources</span></span>
* <span data-ttu-id="4bd31-1115">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1115">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1116">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1117">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1117">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="4bd31-1118">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="4bd31-1118">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="4bd31-1119">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4bd31-1119">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="4bd31-1120">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="4bd31-1120">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1121">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1121">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1122">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="4bd31-1122">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="4bd31-1123">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1123">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="4bd31-1124">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="4bd31-1124">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="4bd31-1125">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1125">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="4bd31-1126">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1126">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="4bd31-1127">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-1127">General</span></span>
* <span data-ttu-id="4bd31-1128">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1128">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1129">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1130">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="4bd31-1130">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="4bd31-1131">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="4bd31-1131">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4bd31-1132">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-1132">Az.Batch</span></span>
* <span data-ttu-id="4bd31-1133">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1133">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1134">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1134">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1135">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1135">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-1136">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1136">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-1137">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="4bd31-1137">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="4bd31-1138">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="4bd31-1138">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4bd31-1139">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4bd31-1139">Az.HealthcareApis</span></span>
* <span data-ttu-id="4bd31-1140">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="4bd31-1140">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-1141">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-1141">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-1142">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="4bd31-1142">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="4bd31-1143">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="4bd31-1143">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="4bd31-1144">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1144">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-1145">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1145">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-1146">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1146">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="4bd31-1147">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="4bd31-1147">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="4bd31-1148">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1148">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1149">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1149">Az.Network</span></span>
* <span data-ttu-id="4bd31-1150">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1150">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1151">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1151">Az.Resources</span></span>
* <span data-ttu-id="4bd31-1152">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1152">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="4bd31-1153">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1153">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1154">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1154">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1155">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="4bd31-1155">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1156">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1157">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="4bd31-1157">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="4bd31-1158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4bd31-1158">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="4bd31-1159">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4bd31-1159">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="4bd31-1160">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1160">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="4bd31-1161">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="4bd31-1161">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="4bd31-1162">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1162">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="4bd31-1163">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1163">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="4bd31-1164">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-1164">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="4bd31-1165">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-1165">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="4bd31-1166">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1166">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="4bd31-1167">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4bd31-1167">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="4bd31-1168">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="4bd31-1168">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="4bd31-1169">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="4bd31-1169">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="4bd31-1170">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1170">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4bd31-1171">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4bd31-1171">Highlights since the last major release</span></span>
* <span data-ttu-id="4bd31-1172">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1172">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="4bd31-1173">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1173">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1174">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1174">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1175">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="4bd31-1175">VM Reapply feature</span></span>
    - <span data-ttu-id="4bd31-1176">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bd31-1176">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="4bd31-1177">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1177">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="4bd31-1178">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-1178">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="4bd31-1179">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bd31-1179">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="4bd31-1180">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-1180">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4bd31-1181">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="4bd31-1181">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="4bd31-1182">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="4bd31-1182">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="4bd31-1183">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4bd31-1183">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="4bd31-1184">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4bd31-1184">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="4bd31-1185">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-1185">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="4bd31-1186">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="4bd31-1186">Az.DataBoxEdge</span></span>
* <span data-ttu-id="4bd31-1187">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1187">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4bd31-1188">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="4bd31-1188">Get the Order</span></span>
* <span data-ttu-id="4bd31-1189">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1189">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4bd31-1190">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="4bd31-1190">Create new Order</span></span>
* <span data-ttu-id="4bd31-1191">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1191">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="4bd31-1192">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="4bd31-1192">Remove the Order</span></span>
* <span data-ttu-id="4bd31-1193">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="4bd31-1193">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="4bd31-1194">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="4bd31-1194">Now creates Local Share</span></span>
* <span data-ttu-id="4bd31-1195">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1195">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="4bd31-1196">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="4bd31-1196">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="4bd31-1197">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1197">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="4bd31-1198">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1198">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="4bd31-1199">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1199">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4bd31-1200">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1200">Gets the information about Triggers</span></span>
* <span data-ttu-id="4bd31-1201">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1201">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4bd31-1202">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1202">Create new Triggers</span></span>
* <span data-ttu-id="4bd31-1203">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1203">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="4bd31-1204">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1204">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1205">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1206">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1206">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="4bd31-1207">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1207">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-1208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-1208">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-1209">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="4bd31-1209">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-1210">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1210">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-1211">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="4bd31-1211">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-1212">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1212">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-1213">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-1213">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="4bd31-1214">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-1214">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="4bd31-1215">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="4bd31-1215">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="4bd31-1216">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-1216">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1217">Az.Network</span></span>
* <span data-ttu-id="4bd31-1218">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1218">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="4bd31-1219">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="4bd31-1219">Az.PrivateDns</span></span>
* <span data-ttu-id="4bd31-1220">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1220">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1222">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1222">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="4bd31-1223">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1223">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="4bd31-1224">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1224">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4bd31-1225">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4bd31-1225">Az.RedisCache</span></span>
* <span data-ttu-id="4bd31-1226">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1226">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="4bd31-1227">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1227">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="4bd31-1228">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1228">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1229">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1229">Az.Resources</span></span>
- <span data-ttu-id="4bd31-1230">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1230">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="4bd31-1231">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1231">Updated create policy definition help example</span></span>
- <span data-ttu-id="4bd31-1232">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1232">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="4bd31-1233">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1233">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="4bd31-1234">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1234">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1235">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1235">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1236">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1236">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="4bd31-1237">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="4bd31-1237">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="4bd31-1238">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1238">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="4bd31-1239">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-1239">General</span></span>
* <span data-ttu-id="4bd31-1240">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1240">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1241">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1241">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1242">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1242">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4bd31-1243">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1243">Az.Advisor</span></span>
* <span data-ttu-id="4bd31-1244">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1244">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4bd31-1245">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-1245">Az.Batch</span></span>
* <span data-ttu-id="4bd31-1246">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1246">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="4bd31-1247">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1247">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="4bd31-1248">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1248">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="4bd31-1249">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1249">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="4bd31-1250">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1250">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="4bd31-1251">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1251">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="4bd31-1252">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1252">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="4bd31-1253">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1253">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="4bd31-1254">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1254">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="4bd31-1255">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1255">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4bd31-1256">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1256">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="4bd31-1257">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1257">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="4bd31-1258">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1258">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="4bd31-1259">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1259">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="4bd31-1260">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1260">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="4bd31-1261">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1261">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="4bd31-1262">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1262">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="4bd31-1263">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1263">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="4bd31-1264">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1264">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="4bd31-1265">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1265">This operation is no longer supported.</span></span>
* <span data-ttu-id="4bd31-1266">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1266">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4bd31-1267">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1267">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="4bd31-1268">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1268">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="4bd31-1269">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1269">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="4bd31-1270">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1270">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="4bd31-1271">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1271">New non-verified images are also now returned.</span></span> <span data-ttu-id="4bd31-1272">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1272">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="4bd31-1273">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1273">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="4bd31-1274">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1274">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="4bd31-1275">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1275">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="4bd31-1276">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1276">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="4bd31-1277">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1277">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="4bd31-1278">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1278">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="4bd31-1279">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1279">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="4bd31-1280">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="4bd31-1280">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="4bd31-1281">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="4bd31-1281">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4bd31-1282">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-1282">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-1283">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1283">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="4bd31-1284">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1284">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1285">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1285">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1286">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="4bd31-1286">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="4bd31-1287">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1287">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="4bd31-1288">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4bd31-1288">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="4bd31-1289">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1289">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4bd31-1290">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1290">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="4bd31-1291">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="4bd31-1291">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="4bd31-1292">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-1292">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="4bd31-1293">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4bd31-1293">Breaking changes</span></span>
    - <span data-ttu-id="4bd31-1294">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1294">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="4bd31-1295">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="4bd31-1295">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1296">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1296">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1297">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1297">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-1298">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-1298">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-1299">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="4bd31-1299">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="4bd31-1300">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1300">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="4bd31-1301">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="4bd31-1301">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="4bd31-1302">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="4bd31-1302">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="4bd31-1303">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="4bd31-1303">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="4bd31-1304">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="4bd31-1304">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-1305">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1305">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-1306">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1306">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-1307">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-1308">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1308">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="4bd31-1309">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1309">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="4bd31-1310">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1310">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="4bd31-1311">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1311">Removed five cmdlets:</span></span>
    - <span data-ttu-id="4bd31-1312">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4bd31-1312">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4bd31-1313">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4bd31-1313">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4bd31-1314">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="4bd31-1314">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="4bd31-1315">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4bd31-1315">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="4bd31-1316">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4bd31-1316">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="4bd31-1317">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1317">Added three cmdlets:</span></span>
    - <span data-ttu-id="4bd31-1318">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1318">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4bd31-1319">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1319">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="4bd31-1320">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1320">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="4bd31-1321">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1321">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="4bd31-1322">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1322">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="4bd31-1323">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1323">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="4bd31-1324">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1324">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="4bd31-1325">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1325">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="4bd31-1326">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1326">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="4bd31-1327">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1327">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="4bd31-1328">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1328">Added some scenario test cases.</span></span>
* <span data-ttu-id="4bd31-1329">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1329">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-1330">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1330">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-1331">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1331">Breaking changes:</span></span>
    - <span data-ttu-id="4bd31-1332">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1332">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4bd31-1333">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1333">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4bd31-1334">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1334">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4bd31-1335">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1335">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4bd31-1336">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1336">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="4bd31-1337">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1337">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="4bd31-1338">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1338">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="4bd31-1339">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1339">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="4bd31-1340">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1340">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4bd31-1341">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1341">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="4bd31-1342">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1342">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="4bd31-1343">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1343">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1344">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1344">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1345">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1345">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="4bd31-1346">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1346">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="4bd31-1347">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1347">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="4bd31-1348">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1348">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="4bd31-1349">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1349">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="4bd31-1350">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1350">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="4bd31-1351">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1351">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="4bd31-1352">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1352">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="4bd31-1353">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="4bd31-1353">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1354">Az.Resources</span></span>
* <span data-ttu-id="4bd31-1355">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="4bd31-1355">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1356">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1356">Az.Network</span></span>
* <span data-ttu-id="4bd31-1357">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1357">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="4bd31-1358">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1358">Updated cmdlet:</span></span>
        - <span data-ttu-id="4bd31-1359">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1359">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1360">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1360">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1361">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1361">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1362">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1362">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1363">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1363">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4bd31-1364">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1364">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="4bd31-1365">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1365">New cmdlet:</span></span>
        - <span data-ttu-id="4bd31-1366">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="4bd31-1366">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="4bd31-1367">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1367">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="4bd31-1368">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1368">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="4bd31-1369">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1369">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="4bd31-1370">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1370">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="4bd31-1371">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1371">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="4bd31-1372">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-1372">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="4bd31-1373">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1373">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="4bd31-1374">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1374">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-1375">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1375">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="4bd31-1376">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-1376">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4bd31-1377">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-1377">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4bd31-1378">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-1378">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="4bd31-1379">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1379">Set-AzVirtualHub</span></span>
* <span data-ttu-id="4bd31-1380">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="4bd31-1380">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="4bd31-1381">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4bd31-1382">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1382">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4bd31-1383">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1383">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="4bd31-1384">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1384">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="4bd31-1385">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1385">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="4bd31-1386">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1386">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="4bd31-1387">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1387">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-1388">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1388">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="4bd31-1389">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1389">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4bd31-1390">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1390">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4bd31-1391">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1391">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4bd31-1392">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1392">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4bd31-1393">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1393">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="4bd31-1394">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1394">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="4bd31-1395">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="4bd31-1395">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="4bd31-1396">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1396">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-1397">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="4bd31-1397">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="4bd31-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="4bd31-1398">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="4bd31-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="4bd31-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="4bd31-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4bd31-1400">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="4bd31-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-1401">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="4bd31-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1402">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="4bd31-1403">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1403">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4bd31-1404">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1404">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="4bd31-1405">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-1405">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="4bd31-1406">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="4bd31-1406">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="4bd31-1407">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="4bd31-1407">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="4bd31-1408">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1408">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="4bd31-1409">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1409">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="4bd31-1410">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1410">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="4bd31-1411">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="4bd31-1411">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="4bd31-1412">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-1412">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="4bd31-1413">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1413">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="4bd31-1414">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1414">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-1415">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1415">New-AzIpGroup</span></span>
        - <span data-ttu-id="4bd31-1416">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1416">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="4bd31-1417">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1417">Get-AzIpGroup</span></span>
        - <span data-ttu-id="4bd31-1418">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1418">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-1419">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-1419">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-1420">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1420">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1421">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1422">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1422">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="4bd31-1423">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1423">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="4bd31-1424">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1424">Removed deprecated aliases:</span></span>
* <span data-ttu-id="4bd31-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1425">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="4bd31-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1426">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="4bd31-1427">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1427">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4bd31-1428">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1428">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="4bd31-1429">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="4bd31-1429">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="4bd31-1430">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1430">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1431">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1432">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-1432">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="4bd31-1433">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1433">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4bd31-1434">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1434">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4bd31-1435">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="4bd31-1435">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="4bd31-1436">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4bd31-1436">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="4bd31-1437">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4bd31-1437">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="4bd31-1438">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1438">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="4bd31-1439">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-1439">General</span></span>
* <span data-ttu-id="4bd31-1440">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1440">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1441">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1442">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1442">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-1443">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-1443">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-1444">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1444">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="4bd31-1445">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="4bd31-1445">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-1446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-1446">Az.Automation</span></span>
* <span data-ttu-id="4bd31-1447">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1447">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4bd31-1448">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-1448">Az.Batch</span></span>
* <span data-ttu-id="4bd31-1449">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1449">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1450">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1451">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-1451">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="4bd31-1452">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4bd31-1452">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="4bd31-1453">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1453">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="4bd31-1454">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1454">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1455">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1456">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1456">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="4bd31-1457">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1457">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="4bd31-1458">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1458">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-1459">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-1459">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-1460">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="4bd31-1460">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="4bd31-1461">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="4bd31-1461">Az.HealthcareApis</span></span>
* <span data-ttu-id="4bd31-1462">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1462">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="4bd31-1463">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="4bd31-1463">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="4bd31-1464">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="4bd31-1464">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="4bd31-1465">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1465">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-1466">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1466">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-1467">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="4bd31-1467">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="4bd31-1468">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bd31-1468">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-1469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1469">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-1470">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="4bd31-1470">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="4bd31-1471">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1471">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="4bd31-1472">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="4bd31-1472">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="4bd31-1473">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1473">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1474">Az.Network</span></span>
* <span data-ttu-id="4bd31-1475">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1475">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="4bd31-1476">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4bd31-1476">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="4bd31-1477">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1477">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-1478">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1478">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="4bd31-1479">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1479">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4bd31-1480">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4bd31-1480">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="4bd31-1481">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1481">Updated cmdlets:</span></span>
        - <span data-ttu-id="4bd31-1482">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1482">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4bd31-1483">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1483">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4bd31-1484">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1484">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4bd31-1485">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="4bd31-1485">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="4bd31-1486">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="4bd31-1486">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="4bd31-1487">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1487">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="4bd31-1488">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1488">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4bd31-1489">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4bd31-1489">Az.RedisCache</span></span>
* <span data-ttu-id="4bd31-1490">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1490">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1491">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1491">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1492">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="4bd31-1492">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1493">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1493">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1494">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-1494">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="4bd31-1495">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4bd31-1495">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4bd31-1496">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4bd31-1496">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="4bd31-1497">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="4bd31-1497">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="4bd31-1498">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1498">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4bd31-1499">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4bd31-1499">Az.StorageSync</span></span>
* <span data-ttu-id="4bd31-1500">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1500">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-1501">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-1501">Az.Websites</span></span>
* <span data-ttu-id="4bd31-1502">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="4bd31-1502">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="4bd31-1503">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1503">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-1504">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-1504">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-1505">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1505">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="4bd31-1506">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1506">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="4bd31-1507">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1507">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-1508">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-1508">Az.Automation</span></span>
* <span data-ttu-id="4bd31-1509">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1509">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="4bd31-1510">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="4bd31-1510">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="4bd31-1511">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1511">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1512">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1512">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1513">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1513">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="4bd31-1514">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1514">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4bd31-1515">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1515">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="4bd31-1516">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1516">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="4bd31-1517">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1517">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="4bd31-1518">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1518">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="4bd31-1519">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1519">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="4bd31-1520">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1520">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="4bd31-1521">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1521">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1522">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1522">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1523">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="4bd31-1523">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="4bd31-1524">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="4bd31-1524">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-1525">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-1525">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-1526">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="4bd31-1526">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-1527">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1527">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-1528">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1528">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="4bd31-1529">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1529">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="4bd31-1530">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1530">New cmdlets are:</span></span>
    - <span data-ttu-id="4bd31-1531">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4bd31-1531">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4bd31-1532">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4bd31-1532">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4bd31-1533">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4bd31-1533">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="4bd31-1534">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="4bd31-1534">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-1535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1535">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-1536">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="4bd31-1536">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="4bd31-1537">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1537">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="4bd31-1538">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1538">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="4bd31-1539">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1539">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="4bd31-1540">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1540">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="4bd31-1541">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1541">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="4bd31-1542">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1542">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="4bd31-1543">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1543">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="4bd31-1544">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1544">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4bd31-1545">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1545">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="4bd31-1546">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1546">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="4bd31-1547">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1547">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="4bd31-1548">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="4bd31-1548">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="4bd31-1549">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4bd31-1549">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="4bd31-1550">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="4bd31-1550">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="4bd31-1551">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1551">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="4bd31-1552">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1552">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="4bd31-1553">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-1553">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="4bd31-1554">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1554">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="4bd31-1555">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-1555">Overall improved help files</span></span>
* <span data-ttu-id="4bd31-1556">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1556">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1557">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1557">Az.Network</span></span>
* <span data-ttu-id="4bd31-1558">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1558">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="4bd31-1559">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="4bd31-1559">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="4bd31-1560">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="4bd31-1560">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="4bd31-1561">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="4bd31-1561">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="4bd31-1562">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="4bd31-1562">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="4bd31-1563">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="4bd31-1563">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="4bd31-1564">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1564">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="4bd31-1565">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4bd31-1565">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="4bd31-1566">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-1566">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="4bd31-1567">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="4bd31-1567">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="4bd31-1568">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-1568">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="4bd31-1569">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="4bd31-1569">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="4bd31-1570">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4bd31-1570">New cmdlets</span></span>
        - <span data-ttu-id="4bd31-1571">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="4bd31-1571">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="4bd31-1572">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1572">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="4bd31-1573">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1573">Updated cmdlet:</span></span>
        - <span data-ttu-id="4bd31-1574">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4bd31-1574">New-VpnSite</span></span>
        - <span data-ttu-id="4bd31-1575">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="4bd31-1575">Update-VpnSite</span></span>
        - <span data-ttu-id="4bd31-1576">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1576">New-VpnConnection</span></span>
        - <span data-ttu-id="4bd31-1577">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1577">Update-VpnConnection</span></span>
* <span data-ttu-id="4bd31-1578">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4bd31-1578">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1579">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1579">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1580">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1580">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="4bd31-1581">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="4bd31-1581">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1582">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1582">Az.Resources</span></span>
* <span data-ttu-id="4bd31-1583">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1583">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-1584">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-1584">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-1585">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1585">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="4bd31-1586">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1586">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="4bd31-1587">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4bd31-1587">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4bd31-1588">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4bd31-1588">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4bd31-1589">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4bd31-1589">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4bd31-1590">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1590">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="4bd31-1591">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4bd31-1591">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4bd31-1592">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4bd31-1592">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4bd31-1593">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4bd31-1593">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4bd31-1594">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4bd31-1594">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4bd31-1595">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1595">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="4bd31-1596">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="4bd31-1596">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="4bd31-1597">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="4bd31-1597">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="4bd31-1598">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="4bd31-1598">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="4bd31-1599">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="4bd31-1599">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="4bd31-1600">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1600">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4bd31-1601">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4bd31-1601">Az.SignalR</span></span>
* <span data-ttu-id="4bd31-1602">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1602">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1603">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1604">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1604">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="4bd31-1605">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="4bd31-1605">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="4bd31-1606">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1606">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="4bd31-1607">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1607">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="4bd31-1608">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="4bd31-1608">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1609">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1609">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1610">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1610">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="4bd31-1611">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="4bd31-1611">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="4bd31-1612">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-1612">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="4bd31-1613">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-1613">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="4bd31-1614">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1614">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="4bd31-1615">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-1615">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="4bd31-1616">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-1616">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="4bd31-1617">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-1617">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4bd31-1618">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-1618">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4bd31-1619">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-1619">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="4bd31-1620">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-1620">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-1621">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-1621">Az.Websites</span></span>
* <span data-ttu-id="4bd31-1622">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="4bd31-1622">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="4bd31-1623">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="4bd31-1623">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="4bd31-1624">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1624">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="4bd31-1625">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1625">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="4bd31-1626">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-1626">General</span></span>
* <span data-ttu-id="4bd31-1627">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1627">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1628">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1629">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1629">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="4bd31-1630">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4bd31-1630">Az.Aks</span></span>
* <span data-ttu-id="4bd31-1631">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1631">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="4bd31-1632">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="4bd31-1632">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-1633">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-1633">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-1634">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="4bd31-1634">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="4bd31-1635">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="4bd31-1635">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="4bd31-1636">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1636">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="4bd31-1637">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="4bd31-1637">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="4bd31-1638">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1638">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4bd31-1639">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-1639">Az.Batch</span></span>
* <span data-ttu-id="4bd31-1640">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="4bd31-1640">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4bd31-1641">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-1641">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-1642">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="4bd31-1642">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1643">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1643">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1644">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1644">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="4bd31-1645">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-1645">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="4bd31-1646">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="4bd31-1646">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="4bd31-1647">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1647">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="4bd31-1648">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="4bd31-1648">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="4bd31-1649">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bd31-1649">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="4bd31-1650">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4bd31-1650">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="4bd31-1651">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1651">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1652">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1653">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1653">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="4bd31-1654">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="4bd31-1654">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="4bd31-1655">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="4bd31-1655">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="4bd31-1656">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="4bd31-1656">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-1657">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-1658">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1658">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-1659">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1659">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-1660">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1660">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="4bd31-1661">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="4bd31-1661">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="4bd31-1662">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4bd31-1662">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="4bd31-1663">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4bd31-1663">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="4bd31-1664">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4bd31-1664">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4bd31-1665">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="4bd31-1665">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1666">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-1667">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-1667">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1668">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1668">Az.Network</span></span>
* <span data-ttu-id="4bd31-1669">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1669">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="4bd31-1670">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1670">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="4bd31-1671">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1671">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="4bd31-1672">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="4bd31-1672">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="4bd31-1673">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1673">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="4bd31-1674">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1674">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="4bd31-1675">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4bd31-1675">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-1676">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1676">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-1677">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1677">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="4bd31-1678">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1678">Added example</span></span>
    - <span data-ttu-id="4bd31-1679">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1679">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="4bd31-1680">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4bd31-1680">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="4bd31-1681">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="4bd31-1681">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1682">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1683">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1683">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1684">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1684">Az.Resources</span></span>
* <span data-ttu-id="4bd31-1685">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="4bd31-1685">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="4bd31-1686">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="4bd31-1686">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="4bd31-1687">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1687">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="4bd31-1688">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-1688">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4bd31-1689">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4bd31-1689">Az.ServiceBus</span></span>
* <span data-ttu-id="4bd31-1690">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-1690">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="4bd31-1691">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="4bd31-1691">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="4bd31-1692">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="4bd31-1692">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-1693">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-1693">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-1694">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1694">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="4bd31-1695">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1695">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="4bd31-1696">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="4bd31-1696">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="4bd31-1697">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1697">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="4bd31-1698">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="4bd31-1698">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="4bd31-1699">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd31-1699">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1700">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1700">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1701">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1701">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1702">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1702">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1703">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="4bd31-1703">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="4bd31-1704">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="4bd31-1704">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="4bd31-1705">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-1705">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="4bd31-1706">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1706">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="4bd31-1707">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="4bd31-1707">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="4bd31-1708">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1708">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-1709">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-1709">Az.Websites</span></span>
* <span data-ttu-id="4bd31-1710">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bd31-1710">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="4bd31-1711">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1711">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1712">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1712">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1713">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4bd31-1713">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="4bd31-1714">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1714">Az.ApplicationInsights</span></span>
* <span data-ttu-id="4bd31-1715">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1715">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-1716">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-1716">Az.Automation</span></span>
* <span data-ttu-id="4bd31-1717">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1717">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-1718">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1718">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-1719">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1719">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1720">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1720">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1721">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1721">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4bd31-1722">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4bd31-1722">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4bd31-1723">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="4bd31-1723">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="4bd31-1724">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="4bd31-1724">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1725">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1725">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1726">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-1726">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="4bd31-1727">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="4bd31-1727">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-1728">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1728">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-1729">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4bd31-1729">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4bd31-1730">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4bd31-1730">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-1731">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-1731">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-1732">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1732">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4bd31-1733">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-1733">Az.LogicApp</span></span>
* <span data-ttu-id="4bd31-1734">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="4bd31-1734">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="4bd31-1735">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="4bd31-1735">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="4bd31-1736">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1736">Az.ManagedServices</span></span>
* <span data-ttu-id="4bd31-1737">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1737">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1738">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1738">Az.Network</span></span>
* <span data-ttu-id="4bd31-1739">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1739">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="4bd31-1740">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4bd31-1740">New cmdlets</span></span>
        - <span data-ttu-id="4bd31-1741">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4bd31-1741">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4bd31-1742">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1742">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4bd31-1743">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1743">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1744">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1744">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1745">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1745">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1746">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1746">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="4bd31-1747">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="4bd31-1747">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="4bd31-1748">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1748">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="4bd31-1749">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="4bd31-1749">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="4bd31-1750">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="4bd31-1750">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="4bd31-1751">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1751">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="4bd31-1752">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1752">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="4bd31-1753">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="4bd31-1753">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="4bd31-1754">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="4bd31-1754">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="4bd31-1755">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1755">Updated cmdlets</span></span>
        - <span data-ttu-id="4bd31-1756">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1756">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4bd31-1757">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1757">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="4bd31-1758">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1758">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="4bd31-1759">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1759">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="4bd31-1760">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-1760">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="4bd31-1761">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1761">Updated cmdlet:</span></span>
        - <span data-ttu-id="4bd31-1762">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1762">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4bd31-1763">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1763">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="4bd31-1764">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1764">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="4bd31-1765">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="4bd31-1765">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="4bd31-1766">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1766">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="4bd31-1767">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1767">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-1768">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1768">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-1769">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1769">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="4bd31-1770">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="4bd31-1770">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1771">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1772">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1772">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4bd31-1773">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1773">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="4bd31-1774">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1774">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="4bd31-1775">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1775">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="4bd31-1776">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1776">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="4bd31-1777">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1777">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4bd31-1778">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1778">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="4bd31-1779">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1779">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="4bd31-1780">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-1780">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="4bd31-1781">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1781">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1782">Az.Resources</span></span>
- <span data-ttu-id="4bd31-1783">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1783">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="4bd31-1784">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4bd31-1784">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4bd31-1785">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4bd31-1785">Az.ServiceBus</span></span>
* <span data-ttu-id="4bd31-1786">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="4bd31-1786">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="4bd31-1787">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="4bd31-1787">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1788">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1789">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4bd31-1789">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="4bd31-1790">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="4bd31-1790">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="4bd31-1791">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1791">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1792">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1792">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1793">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="4bd31-1793">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4bd31-1794">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4bd31-1794">Az.StorageSync</span></span>
* <span data-ttu-id="4bd31-1795">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1795">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="4bd31-1796">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="4bd31-1796">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-1797">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-1797">Az.Websites</span></span>
* <span data-ttu-id="4bd31-1798">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-1798">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="4bd31-1799">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-1799">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="4bd31-1800">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="4bd31-1800">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="4bd31-1801">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1801">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1802">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1803">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="4bd31-1803">Add support for profile cmdlets</span></span>
* <span data-ttu-id="4bd31-1804">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1804">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="4bd31-1805">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4bd31-1805">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="4bd31-1806">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1806">Az.Advisor</span></span>
* <span data-ttu-id="4bd31-1807">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1807">GA release of Az.Advisor</span></span>
* <span data-ttu-id="4bd31-1808">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1808">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-1809">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-1809">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-1810">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="4bd31-1810">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="4bd31-1811">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4bd31-1811">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="4bd31-1812">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="4bd31-1812">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="4bd31-1813">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1813">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="4bd31-1814">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="4bd31-1814">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="4bd31-1815">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4bd31-1815">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="4bd31-1816">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="4bd31-1816">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-1817">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-1817">Az.Automation</span></span>
* <span data-ttu-id="4bd31-1818">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1818">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1819">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1820">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1820">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-1821">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-1821">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-1822">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1822">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4bd31-1823">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4bd31-1823">Az.EventGrid</span></span>
* <span data-ttu-id="4bd31-1824">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1824">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-1825">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1825">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-1826">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1826">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1827">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1827">Az.Network</span></span>
* <span data-ttu-id="4bd31-1828">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="4bd31-1828">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="4bd31-1829">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1829">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-1830">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1830">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-1831">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="4bd31-1831">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="4bd31-1832">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="4bd31-1832">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-1833">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1833">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-1834">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="4bd31-1834">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-1835">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-1835">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-1836">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="4bd31-1836">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1837">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1837">Az.Resources</span></span>
    - <span data-ttu-id="4bd31-1838">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="4bd31-1838">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="4bd31-1839">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="4bd31-1839">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="4bd31-1840">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-1840">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="4bd31-1841">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1841">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4bd31-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4bd31-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="4bd31-1843">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="4bd31-1843">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1844">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1845">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="4bd31-1845">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="4bd31-1846">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1846">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="4bd31-1847">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4bd31-1847">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4bd31-1848">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4bd31-1848">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4bd31-1849">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4bd31-1849">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="4bd31-1850">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4bd31-1850">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4bd31-1851">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4bd31-1851">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="4bd31-1852">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="4bd31-1852">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="4bd31-1853">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="4bd31-1853">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1854">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1854">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1855">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1855">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="4bd31-1856">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4bd31-1856">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="4bd31-1857">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1857">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="4bd31-1858">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="4bd31-1858">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="4bd31-1859">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-1859">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="4bd31-1860">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1860">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="4bd31-1861">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1861">Set-AzStorageAccount</span></span>
* <span data-ttu-id="4bd31-1862">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1862">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="4bd31-1863">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4bd31-1863">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="4bd31-1864">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="4bd31-1864">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="4bd31-1865">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="4bd31-1865">Az.StorageSync</span></span>
* <span data-ttu-id="4bd31-1866">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1866">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="4bd31-1867">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1867">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-1868">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-1868">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-1869">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="4bd31-1869">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="4bd31-1870">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="4bd31-1870">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="4bd31-1871">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="4bd31-1871">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="4bd31-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4bd31-1872">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="4bd31-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="4bd31-1873">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1874">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1874">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1875">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1875">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="4bd31-1876">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1876">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="4bd31-1877">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4bd31-1877">Az.Dns</span></span>
* <span data-ttu-id="4bd31-1878">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1878">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4bd31-1879">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4bd31-1879">Az.EventGrid</span></span>
* <span data-ttu-id="4bd31-1880">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1880">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="4bd31-1881">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1881">New cmdlets:</span></span>
    - <span data-ttu-id="4bd31-1882">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4bd31-1882">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4bd31-1883">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1883">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4bd31-1884">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4bd31-1884">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4bd31-1885">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1885">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="4bd31-1886">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="4bd31-1886">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="4bd31-1887">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1887">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4bd31-1888">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4bd31-1888">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4bd31-1889">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1889">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="4bd31-1890">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="4bd31-1890">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="4bd31-1891">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1891">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="4bd31-1892">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1892">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4bd31-1893">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1893">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="4bd31-1894">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="4bd31-1894">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="4bd31-1895">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="4bd31-1895">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="4bd31-1896">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1896">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="4bd31-1897">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1897">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="4bd31-1898">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1898">Updated cmdlets:</span></span>
    - <span data-ttu-id="4bd31-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1899">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="4bd31-1900">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1900">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4bd31-1901">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1901">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="4bd31-1902">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="4bd31-1902">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="4bd31-1903">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1903">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="4bd31-1904">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="4bd31-1904">Event subscription expiration date,</span></span>
            - <span data-ttu-id="4bd31-1905">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1905">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="4bd31-1906">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1906">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="4bd31-1907">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="4bd31-1907">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="4bd31-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1908">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="4bd31-1909">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1909">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="4bd31-1910">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4bd31-1910">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="4bd31-1911">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1911">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="4bd31-1912">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1912">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-1913">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-1913">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-1914">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-1914">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="4bd31-1915">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="4bd31-1915">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="4bd31-1916">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-1916">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="4bd31-1917">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="4bd31-1917">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1918">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1918">Az.Network</span></span>
* <span data-ttu-id="4bd31-1919">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4bd31-1919">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="4bd31-1920">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4bd31-1920">New cmdlets</span></span>
        - <span data-ttu-id="4bd31-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="4bd31-1921">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="4bd31-1922">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4bd31-1922">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="4bd31-1923">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4bd31-1923">New cmdlets</span></span>
        - <span data-ttu-id="4bd31-1924">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="4bd31-1924">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="4bd31-1925">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1925">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="4bd31-1926">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4bd31-1926">New cmdlets</span></span>
        - <span data-ttu-id="4bd31-1927">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1927">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4bd31-1928">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1928">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4bd31-1929">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="4bd31-1929">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="4bd31-1930">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-1930">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="4bd31-1931">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1931">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="4bd31-1932">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4bd31-1932">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="4bd31-1933">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4bd31-1933">New cmdlets</span></span>
        - <span data-ttu-id="4bd31-1934">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4bd31-1934">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4bd31-1935">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4bd31-1935">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4bd31-1936">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="4bd31-1936">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="4bd31-1937">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1937">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="4bd31-1938">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="4bd31-1938">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="4bd31-1939">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1939">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="4bd31-1940">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1940">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="4bd31-1941">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1941">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="4bd31-1942">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1942">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="4bd31-1943">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bd31-1943">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="4bd31-1944">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-1944">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="4bd31-1945">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1945">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="4bd31-1946">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-1946">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="4bd31-1947">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="4bd31-1947">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="4bd31-1948">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="4bd31-1948">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="4bd31-1949">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="4bd31-1949">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="4bd31-1950">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="4bd31-1950">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="4bd31-1951">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-1951">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="4bd31-1952">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="4bd31-1952">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="4bd31-1953">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="4bd31-1953">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="4bd31-1954">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4bd31-1954">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="4bd31-1955">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="4bd31-1955">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="4bd31-1956">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4bd31-1956">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="4bd31-1957">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1957">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="4bd31-1958">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1958">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4bd31-1959">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1959">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="4bd31-1960">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1960">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-1961">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1961">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-1962">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="4bd31-1962">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-1963">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-1963">Az.Resources</span></span>
* <span data-ttu-id="4bd31-1964">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="4bd31-1964">Support for additional Template Export options</span></span>
    - <span data-ttu-id="4bd31-1965">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1965">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4bd31-1966">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-1966">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="4bd31-1967">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="4bd31-1967">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-1968">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-1969">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="4bd31-1969">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-1970">Az.Sql</span></span>
* <span data-ttu-id="4bd31-1971">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4bd31-1971">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="4bd31-1972">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4bd31-1972">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="4bd31-1973">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4bd31-1973">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="4bd31-1974">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bd31-1974">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4bd31-1975">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bd31-1975">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4bd31-1976">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bd31-1976">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="4bd31-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4bd31-1977">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="4bd31-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="4bd31-1978">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-1979">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-1979">Az.Storage</span></span>
* <span data-ttu-id="4bd31-1980">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-1980">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="4bd31-1981">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-1981">New-AzStorageAccount</span></span>
* <span data-ttu-id="4bd31-1982">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="4bd31-1982">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="4bd31-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-1983">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-1984">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-1984">Az.Websites</span></span>
* <span data-ttu-id="4bd31-1985">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="4bd31-1985">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="4bd31-1986">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bd31-1986">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="4bd31-1987">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-1987">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="4bd31-1988">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-1988">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-1989">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1989">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-1990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-1990">Az.Compute</span></span>
* <span data-ttu-id="4bd31-1991">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="4bd31-1991">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="4bd31-1992">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bd31-1992">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-1993">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-1993">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-1994">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="4bd31-1994">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="4bd31-1995">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd31-1995">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-1996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-1996">Az.Network</span></span>
* <span data-ttu-id="4bd31-1997">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="4bd31-1997">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="4bd31-1998">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="4bd31-1998">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-1999">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-1999">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-2000">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="4bd31-2000">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2001">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2001">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-2002">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="4bd31-2002">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4bd31-2003">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4bd31-2003">Az.ServiceBus</span></span>
* <span data-ttu-id="4bd31-2004">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd31-2004">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-2005">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2005">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-2006">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2006">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="4bd31-2007">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2007">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2008">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2008">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2009">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2009">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="4bd31-2010">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2010">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="4bd31-2011">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="4bd31-2011">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="4bd31-2012">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2012">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2013">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2013">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2014">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2014">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="4bd31-2015">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2015">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="4bd31-2016">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-2016">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-2017">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2017">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="4bd31-2018">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2018">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="4bd31-2019">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2019">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="4bd31-2020">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2020">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="4bd31-2021">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2021">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="4bd31-2022">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="4bd31-2022">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="4bd31-2023">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2023">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="4bd31-2024">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2024">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="4bd31-2025">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-2025">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="4bd31-2026">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="4bd31-2026">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="4bd31-2027">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2027">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="4bd31-2028">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="4bd31-2028">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="4bd31-2029">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="4bd31-2029">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="4bd31-2030">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2030">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="4bd31-2031">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2031">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="4bd31-2032">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2032">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="4bd31-2033">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2033">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="4bd31-2034">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="4bd31-2034">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="4bd31-2035">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2035">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="4bd31-2036">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="4bd31-2036">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="4bd31-2037">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="4bd31-2037">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="4bd31-2038">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2038">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="4bd31-2039">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2039">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="4bd31-2040">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-2040">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="4bd31-2041">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2041">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="4bd31-2042">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2042">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="4bd31-2043">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2043">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="4bd31-2044">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2044">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="4bd31-2045">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2045">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="4bd31-2046">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="4bd31-2046">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="4bd31-2047">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2047">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="4bd31-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="4bd31-2048">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="4bd31-2049">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2049">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="4bd31-2050">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4bd31-2050">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4bd31-2051">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2051">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="4bd31-2052">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="4bd31-2052">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="4bd31-2053">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2053">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="4bd31-2054">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2054">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="4bd31-2055">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2055">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="4bd31-2056">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4bd31-2056">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4bd31-2057">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2057">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4bd31-2058">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2058">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4bd31-2059">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2059">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="4bd31-2060">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2060">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4bd31-2061">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="4bd31-2061">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="4bd31-2062">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2062">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="4bd31-2063">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2063">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="4bd31-2064">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2064">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="4bd31-2065">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="4bd31-2065">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="4bd31-2066">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2066">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="4bd31-2067">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2067">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="4bd31-2068">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2068">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="4bd31-2069">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2069">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="4bd31-2070">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="4bd31-2070">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="4bd31-2071">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2071">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="4bd31-2072">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2072">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="4bd31-2073">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4bd31-2073">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4bd31-2074">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2074">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4bd31-2075">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2075">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4bd31-2076">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2076">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4bd31-2077">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="4bd31-2077">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="4bd31-2078">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2078">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="4bd31-2079">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2079">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="4bd31-2080">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2080">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="4bd31-2081">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="4bd31-2081">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="4bd31-2082">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2082">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="4bd31-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="4bd31-2083">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="4bd31-2084">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2084">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="4bd31-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="4bd31-2085">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="4bd31-2086">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2086">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="4bd31-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="4bd31-2087">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="4bd31-2088">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2088">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="4bd31-2089">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2089">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="4bd31-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2090">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="4bd31-2091">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2091">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="4bd31-2092">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2092">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="4bd31-2093">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2093">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-2094">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2094">Az.Automation</span></span>
* <span data-ttu-id="4bd31-2095">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2095">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="4bd31-2096">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="4bd31-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="4bd31-2097">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="4bd31-2097">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="4bd31-2098">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2098">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="4bd31-2099">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="4bd31-2099">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="4bd31-2100">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2100">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="4bd31-2101">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2101">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2102">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2103">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2103">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="4bd31-2104">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2104">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2105">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2105">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-2106">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2106">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-2107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-2107">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-2108">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-2108">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2109">Az.Network</span></span>
* <span data-ttu-id="4bd31-2110">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2110">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="4bd31-2111">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="4bd31-2111">Updated cmdlet:</span></span>
        - <span data-ttu-id="4bd31-2112">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-2112">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="4bd31-2113">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd31-2113">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2114">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2115">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="4bd31-2115">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2116">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2116">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2117">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="4bd31-2117">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="4bd31-2118">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2118">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2119">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2119">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2120">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="4bd31-2120">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-2121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2121">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-2122">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2122">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="4bd31-2123">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2123">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2124">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2124">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2125">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2125">Proximity placement group feature.</span></span>
    - <span data-ttu-id="4bd31-2126">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-2126">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="4bd31-2127">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-2127">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="4bd31-2128">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2128">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="4bd31-2129">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2129">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="4bd31-2130">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-2130">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="4bd31-2131">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="4bd31-2131">Breaking changes</span></span>
    - <span data-ttu-id="4bd31-2132">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2132">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="4bd31-2133">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2133">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="4bd31-2134">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="4bd31-2134">Az.DeploymentManager</span></span>
* <span data-ttu-id="4bd31-2135">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2135">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="4bd31-2136">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="4bd31-2136">Az.Dns</span></span>
* <span data-ttu-id="4bd31-2137">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="4bd31-2137">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="4bd31-2138">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2138">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="4bd31-2139">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2139">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-2140">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-2140">Az.FrontDoor</span></span>
* <span data-ttu-id="4bd31-2141">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2141">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="4bd31-2142">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2142">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-2143">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-2143">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-2144">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="4bd31-2144">Removed two cmdlets:</span></span>
    - <span data-ttu-id="4bd31-2145">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4bd31-2145">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="4bd31-2146">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4bd31-2146">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4bd31-2147">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="4bd31-2147">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="4bd31-2148">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="4bd31-2148">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="4bd31-2149">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2149">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="4bd31-2150">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2150">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-2151">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-2151">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-2152">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="4bd31-2152">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="4bd31-2153">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="4bd31-2153">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="4bd31-2154">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-2154">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="4bd31-2155">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="4bd31-2155">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="4bd31-2156">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2156">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="4bd31-2157">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="4bd31-2157">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="4bd31-2158">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="4bd31-2158">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="4bd31-2159">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2159">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4bd31-2160">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2160">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4bd31-2161">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2161">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4bd31-2162">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2162">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4bd31-2163">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2163">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="4bd31-2164">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="4bd31-2164">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="4bd31-2165">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4bd31-2165">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2166">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2166">Az.Network</span></span>
* <span data-ttu-id="4bd31-2167">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="4bd31-2167">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="4bd31-2168">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="4bd31-2168">New cmdlets</span></span>
        - <span data-ttu-id="4bd31-2169">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4bd31-2169">New-AzNatGateway</span></span>
        - <span data-ttu-id="4bd31-2170">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4bd31-2170">Get-AzNatGateway</span></span>
        - <span data-ttu-id="4bd31-2171">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4bd31-2171">Set-AzNatGateway</span></span>
        - <span data-ttu-id="4bd31-2172">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4bd31-2172">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="4bd31-2173">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2173">Updated cmdlets</span></span>
        - <span data-ttu-id="4bd31-2174">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4bd31-2174">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="4bd31-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="4bd31-2175">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="4bd31-2176">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2176">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="4bd31-2177">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2177">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="4bd31-2178">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2178">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-2179">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-2179">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-2180">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2180">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="4bd31-2181">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2181">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="4bd31-2182">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2182">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2183">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2183">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-2184">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2184">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="4bd31-2185">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2185">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="4bd31-2186">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2186">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="4bd31-2187">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2187">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="4bd31-2188">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2188">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="4bd31-2189">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2189">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="4bd31-2190">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4bd31-2190">Az.Relay</span></span>
* <span data-ttu-id="4bd31-2191">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="4bd31-2191">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4bd31-2192">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4bd31-2192">Az.ServiceBus</span></span>
* <span data-ttu-id="4bd31-2193">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4bd31-2193">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-2194">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2194">Az.Storage</span></span>
* <span data-ttu-id="4bd31-2195">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="4bd31-2195">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="4bd31-2196">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2196">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="4bd31-2197">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2197">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="4bd31-2198">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2198">New-AzStorageAccount</span></span>
* <span data-ttu-id="4bd31-2199">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2199">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="4bd31-2200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2200">New-AzStorageAccount</span></span>
    - <span data-ttu-id="4bd31-2201">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2201">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="4bd31-2202">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2202">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2203">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2203">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2204">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-2204">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="4bd31-2205">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2205">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="4bd31-2206">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2206">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4bd31-2207">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4bd31-2207">Highlights since the last major release</span></span>
* <span data-ttu-id="4bd31-2208">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4bd31-2208">General availability of `Az` module</span></span>
* <span data-ttu-id="4bd31-2209">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4bd31-2209">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4bd31-2210">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4bd31-2210">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4bd31-2211">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2211">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4bd31-2212">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4bd31-2212">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4bd31-2213">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2213">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4bd31-2214">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4bd31-2214">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2215">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2215">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2216">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="4bd31-2216">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="4bd31-2217">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-2217">Az.Batch</span></span>
* <span data-ttu-id="4bd31-2218">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4bd31-2219">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-2219">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-2220">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2220">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-2222">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2223">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2224">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2224">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="4bd31-2225">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2225">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4bd31-2226">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4bd31-2226">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-2227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-2227">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-2228">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2228">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2229">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2229">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-2230">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2230">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4bd31-2231">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4bd31-2231">Az.EventGrid</span></span>
* <span data-ttu-id="4bd31-2232">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2232">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-2233">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-2233">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-2234">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="4bd31-2234">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="4bd31-2235">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="4bd31-2235">Az.HDInsight</span></span>
* <span data-ttu-id="4bd31-2236">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-2237">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-2237">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-2238">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-2239">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-2239">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-2240">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4bd31-2241">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4bd31-2241">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="4bd31-2242">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4bd31-2242">Az.MachineLearning</span></span>
* <span data-ttu-id="4bd31-2243">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2243">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="4bd31-2244">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4bd31-2244">Az.Media</span></span>
* <span data-ttu-id="4bd31-2245">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2245">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-2246">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-2246">Az.Monitor</span></span>
  * <span data-ttu-id="4bd31-2247">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="4bd31-2247">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="4bd31-2248">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="4bd31-2248">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="4bd31-2249">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="4bd31-2249">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="4bd31-2250">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4bd31-2250">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4bd31-2251">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4bd31-2251">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="4bd31-2252">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="4bd31-2252">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="4bd31-2253">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="4bd31-2253">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2254">Az.Network</span></span>
* <span data-ttu-id="4bd31-2255">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4bd31-2256">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4bd31-2256">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="4bd31-2257">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="4bd31-2257">Az.NotificationHubs</span></span>
* <span data-ttu-id="4bd31-2258">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2258">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-2259">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-2259">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-2260">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="4bd31-2261">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="4bd31-2261">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="4bd31-2262">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2262">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2263">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2263">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-2264">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2264">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4bd31-2265">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2265">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="4bd31-2266">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="4bd31-2266">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="4bd31-2267">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="4bd31-2267">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4bd31-2268">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4bd31-2268">Az.RedisCache</span></span>
* <span data-ttu-id="4bd31-2269">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2269">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2270">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2271">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4bd31-2271">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2272">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2272">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2273">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="4bd31-2273">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="4bd31-2274">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2274">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4bd31-2275">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2275">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="4bd31-2276">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2276">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="4bd31-2277">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2277">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="4bd31-2278">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2278">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="4bd31-2279">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="4bd31-2279">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2280">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2280">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2281">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="4bd31-2281">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="4bd31-2282">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2282">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="4bd31-2283">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2283">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="4bd31-2284">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2284">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="4bd31-2285">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2285">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4bd31-2286">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4bd31-2286">Highlights since the last major release</span></span>
* <span data-ttu-id="4bd31-2287">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4bd31-2287">General availability of `Az` module</span></span>
* <span data-ttu-id="4bd31-2288">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4bd31-2288">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4bd31-2289">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4bd31-2289">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4bd31-2290">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2290">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4bd31-2291">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4bd31-2291">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4bd31-2292">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2292">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4bd31-2293">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4bd31-2293">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2294">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2294">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2295">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd31-2295">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4bd31-2296">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2296">Az.AnalysisServices</span></span>
* <span data-ttu-id="4bd31-2297">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="4bd31-2297">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="4bd31-2298">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="4bd31-2298">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-2299">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2299">Az.Automation</span></span>
* <span data-ttu-id="4bd31-2300">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2300">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="4bd31-2301">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2301">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="4bd31-2302">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2302">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2303">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2303">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2304">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-2304">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="4bd31-2305">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2305">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="4bd31-2306">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-2306">Az.ContainerInstance</span></span>
* <span data-ttu-id="4bd31-2307">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="4bd31-2307">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-2308">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-2308">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-2309">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="4bd31-2309">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="4bd31-2310">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2310">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2311">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2311">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2312">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="4bd31-2312">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="4bd31-2313">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2313">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="4bd31-2314">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="4bd31-2314">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="4bd31-2315">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4bd31-2315">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="4bd31-2316">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="4bd31-2316">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="4bd31-2317">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="4bd31-2317">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2318">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2318">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2319">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2319">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-2320">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2320">Az.Storage</span></span>
* <span data-ttu-id="4bd31-2321">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2321">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="4bd31-2322">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4bd31-2322">New-AzStorageContext</span></span>
* <span data-ttu-id="4bd31-2323">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-2323">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="4bd31-2324">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4bd31-2324">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4bd31-2325">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4bd31-2325">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="4bd31-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2326">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="4bd31-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2327">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="4bd31-2328">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2328">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="4bd31-2329">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-2329">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4bd31-2330">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-2330">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="4bd31-2331">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-2331">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="4bd31-2332">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4bd31-2332">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="4bd31-2333">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2333">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="4bd31-2334">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="4bd31-2334">Highlights since the last major release</span></span>
* <span data-ttu-id="4bd31-2335">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="4bd31-2335">General availability of `Az` module</span></span>
* <span data-ttu-id="4bd31-2336">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="4bd31-2336">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="4bd31-2337">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="4bd31-2337">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="4bd31-2338">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2338">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="4bd31-2339">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4bd31-2339">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4bd31-2340">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2340">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="4bd31-2341">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="4bd31-2341">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-2342">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2342">Az.Automation</span></span>
* <span data-ttu-id="4bd31-2343">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="4bd31-2343">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="4bd31-2344">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="4bd31-2344">Dynamic grouping</span></span>
    * <span data-ttu-id="4bd31-2345">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="4bd31-2345">Pre-Post script</span></span>
    * <span data-ttu-id="4bd31-2346">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="4bd31-2346">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2347">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2347">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2348">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="4bd31-2348">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="4bd31-2349">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2349">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-2350">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-2350">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-2351">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-2351">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2352">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2352">Az.Network</span></span>
* <span data-ttu-id="4bd31-2353">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2353">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="4bd31-2354">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2354">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2355">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2355">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-2356">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2356">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="4bd31-2357">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="4bd31-2357">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2358">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2358">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2359">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4bd31-2359">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="4bd31-2360">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="4bd31-2360">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2361">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2361">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2362">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2362">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-2363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2363">Az.Storage</span></span>
* <span data-ttu-id="4bd31-2364">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-2364">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="4bd31-2365">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2365">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4bd31-2366">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2366">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4bd31-2367">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2367">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="4bd31-2368">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="4bd31-2368">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="4bd31-2369">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="4bd31-2369">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="4bd31-2370">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2370">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2371">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2372">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="4bd31-2372">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="4bd31-2373">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2373">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2374">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2374">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2375">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="4bd31-2375">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="4bd31-2376">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2376">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-2377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2377">Az.Automation</span></span>
* <span data-ttu-id="4bd31-2378">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2378">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="4bd31-2379">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2379">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="4bd31-2380">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="4bd31-2380">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4bd31-2381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-2381">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-2382">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2382">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2383">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2384">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="4bd31-2384">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-2385">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-2385">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-2386">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="4bd31-2386">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4bd31-2387">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-2387">Az.LogicApp</span></span>
* <span data-ttu-id="4bd31-2388">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2388">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2389">Az.Network</span></span>
* <span data-ttu-id="4bd31-2390">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2390">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2391">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-2392">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2392">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="4bd31-2393">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="4bd31-2393">SDK Update</span></span>
* <span data-ttu-id="4bd31-2394">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4bd31-2394">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="4bd31-2395">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4bd31-2395">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2396">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2396">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2397">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="4bd31-2397">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="4bd31-2398">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="4bd31-2398">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="4bd31-2399">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4bd31-2399">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="4bd31-2400">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="4bd31-2400">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="4bd31-2401">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="4bd31-2401">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="4bd31-2402">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="4bd31-2402">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2403">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2403">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2404">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2404">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="4bd31-2405">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2405">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-2406">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2406">Az.Storage</span></span>
* <span data-ttu-id="4bd31-2407">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2407">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="4bd31-2408">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2408">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="4bd31-2409">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2409">Az.AnalysisServices</span></span>
* <span data-ttu-id="4bd31-2410">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2410">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-2411">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2411">Az.Automation</span></span>
* <span data-ttu-id="4bd31-2412">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2412">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="4bd31-2413">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2413">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="4bd31-2414">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2414">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-2415">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2415">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-2416">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2416">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2417">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2418">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="4bd31-2418">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="4bd31-2419">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="4bd31-2419">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="4bd31-2420">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2420">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="4bd31-2421">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2421">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2422">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2422">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-2423">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2423">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="4bd31-2424">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-2424">Az.EventHub</span></span>
* <span data-ttu-id="4bd31-2425">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-2425">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-2426">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-2426">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-2427">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4bd31-2427">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4bd31-2428">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-2428">Az.LogicApp</span></span>
* <span data-ttu-id="4bd31-2429">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="4bd31-2429">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="4bd31-2430">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="4bd31-2430">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="4bd31-2431">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="4bd31-2431">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="4bd31-2432">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4bd31-2432">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4bd31-2433">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4bd31-2433">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4bd31-2434">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4bd31-2434">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="4bd31-2435">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4bd31-2435">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="4bd31-2436">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="4bd31-2436">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="4bd31-2437">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2437">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4bd31-2438">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2438">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4bd31-2439">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2439">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="4bd31-2440">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2440">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="4bd31-2441">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-2441">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="4bd31-2442">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-2442">Az.Monitor</span></span>
* <span data-ttu-id="4bd31-2443">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2443">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2444">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2444">Az.Network</span></span>
* <span data-ttu-id="4bd31-2445">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4bd31-2445">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-2446">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-2446">Az.OperationalInsights</span></span>
* <span data-ttu-id="4bd31-2447">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2447">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="4bd31-2448">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2448">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="4bd31-2449">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2449">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2450">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2451">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4bd31-2451">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4bd31-2452">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4bd31-2452">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="4bd31-2453">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="4bd31-2453">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="4bd31-2454">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="4bd31-2454">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2455">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2456">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="4bd31-2456">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="4bd31-2457">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="4bd31-2457">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2458">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2458">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2459">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="4bd31-2459">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="4bd31-2460">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2460">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2461">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2461">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2462">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4bd31-2462">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4bd31-2463">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2463">Az.AnalysisServices</span></span>
<span data-ttu-id="4bd31-2464">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2464">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2465">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2466">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="4bd31-2466">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="4bd31-2467">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4bd31-2467">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="4bd31-2468">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2468">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2469">Az.RecoveryServices</span></span>
<span data-ttu-id="4bd31-2470">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2470">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2471">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2471">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2472">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2472">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="4bd31-2473">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="4bd31-2473">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="4bd31-2474">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="4bd31-2474">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="4bd31-2475">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="4bd31-2475">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2476">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2476">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2477">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2477">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="4bd31-2478">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="4bd31-2478">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="4bd31-2479">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="4bd31-2479">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="4bd31-2480">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2480">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2481">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2482">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="4bd31-2482">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="4bd31-2483">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2483">Az.AnalysisServices</span></span>
* <span data-ttu-id="4bd31-2484">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-2484">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2485">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2485">Az.RecoveryServices</span></span>
* <span data-ttu-id="4bd31-2486">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-2486">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="4bd31-2487">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2487">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2488">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2489">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4bd31-2489">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="4bd31-2490">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2490">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4bd31-2491">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="4bd31-2491">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="4bd31-2492">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="4bd31-2492">Az.Aks</span></span>
* <span data-ttu-id="4bd31-2493">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2493">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="4bd31-2494">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2494">Az.Automation</span></span>
* <span data-ttu-id="4bd31-2495">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="4bd31-2495">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="4bd31-2496">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2496">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="4bd31-2497">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="4bd31-2497">Az.Cdn</span></span>
* <span data-ttu-id="4bd31-2498">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2498">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2499">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2499">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2500">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2500">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="4bd31-2501">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bd31-2501">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="4bd31-2502">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bd31-2502">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="4bd31-2503">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="4bd31-2503">Az.ContainerRegistry</span></span>
* <span data-ttu-id="4bd31-2504">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2504">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="4bd31-2505">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="4bd31-2505">Az.DataFactory</span></span>
* <span data-ttu-id="4bd31-2506">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="4bd31-2506">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2507">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2507">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-2508">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4bd31-2508">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="4bd31-2509">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="4bd31-2509">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="4bd31-2510">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2510">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-2511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-2511">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-2512">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2512">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="4bd31-2513">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-2513">Az.KeyVault</span></span>
* <span data-ttu-id="4bd31-2514">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2514">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2515">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2515">Az.Network</span></span>
* <span data-ttu-id="4bd31-2516">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2516">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2517">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2517">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2518">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2518">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="4bd31-2519">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2519">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="4bd31-2520">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="4bd31-2520">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="4bd31-2521">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="4bd31-2521">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="4bd31-2522">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="4bd31-2522">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="4bd31-2523">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2523">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="4bd31-2524">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="4bd31-2524">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-2525">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2525">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-2526">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="4bd31-2526">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="4bd31-2527">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2527">Fix some error messages.</span></span>
* <span data-ttu-id="4bd31-2528">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2528">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="4bd31-2529">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2529">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4bd31-2530">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4bd31-2530">Az.SignalR</span></span>
* <span data-ttu-id="4bd31-2531">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2531">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2532">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2533">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2533">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4bd31-2534">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4bd31-2534">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="4bd31-2535">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="4bd31-2535">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="4bd31-2536">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2536">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-2537">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2537">Az.Storage</span></span>
* <span data-ttu-id="4bd31-2538">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2538">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4bd31-2539">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2539">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="4bd31-2540">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="4bd31-2540">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="4bd31-2541">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4bd31-2541">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="4bd31-2542">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4bd31-2542">Az.TrafficManager</span></span>
* <span data-ttu-id="4bd31-2543">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2543">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2544">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2544">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2545">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="4bd31-2545">Update incorrect online help URLs</span></span>
* <span data-ttu-id="4bd31-2546">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2546">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="4bd31-2547">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2547">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="4bd31-2548">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="4bd31-2548">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="4bd31-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2549">Az.Accounts</span></span>
* <span data-ttu-id="4bd31-2550">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="4bd31-2550">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2551">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2551">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2552">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2552">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="4bd31-2553">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="4bd31-2553">Updated the description of ID in help files</span></span>
* <span data-ttu-id="4bd31-2554">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2554">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2555">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2555">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-2556">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2556">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="4bd31-2557">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="4bd31-2557">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="4bd31-2558">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="4bd31-2558">Az.EventGrid</span></span>
* <span data-ttu-id="4bd31-2559">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2559">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="4bd31-2560">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="4bd31-2560">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="4bd31-2561">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4bd31-2561">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4bd31-2562">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4bd31-2562">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4bd31-2563">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2563">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4bd31-2564">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2564">Dead letter endpoint.</span></span>
    - <span data-ttu-id="4bd31-2565">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="4bd31-2565">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="4bd31-2566">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="4bd31-2566">Event Time-To-Live,</span></span>
        - <span data-ttu-id="4bd31-2567">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2567">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="4bd31-2568">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="4bd31-2568">Dead letter endpoint.</span></span>
* <span data-ttu-id="4bd31-2569">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2569">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="4bd31-2570">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2570">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="4bd31-2571">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-2571">Az.IotHub</span></span>
* <span data-ttu-id="4bd31-2572">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd31-2572">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="4bd31-2573">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="4bd31-2573">Az.LogicApp</span></span>
* <span data-ttu-id="4bd31-2574">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="4bd31-2574">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2575">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2576">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2576">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="4bd31-2577">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="4bd31-2577">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="4bd31-2578">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4bd31-2578">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4bd31-2579">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4bd31-2579">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="4bd31-2580">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2580">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="4bd31-2581">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="4bd31-2581">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="4bd31-2582">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="4bd31-2582">Az.SignalR</span></span>
* <span data-ttu-id="4bd31-2583">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2583">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2584">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2584">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2585">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2585">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="4bd31-2586">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2586">Az.Storage</span></span>
* <span data-ttu-id="4bd31-2587">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="4bd31-2587">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="4bd31-2588">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4bd31-2588">New-AzStorageContext</span></span>
* <span data-ttu-id="4bd31-2589">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2589">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="4bd31-2590">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4bd31-2590">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2591">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2591">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2592">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="4bd31-2592">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="4bd31-2593">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2593">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="4bd31-2594">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4bd31-2594">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="4bd31-2595">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-2595">General</span></span>

- <span data-ttu-id="4bd31-2596">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="4bd31-2596">General Availability of Az Module</span></span>
- <span data-ttu-id="4bd31-2597">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2597">Online help for each module</span></span>
- <span data-ttu-id="4bd31-2598">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="4bd31-2598">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="4bd31-2599">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="4bd31-2599">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="4bd31-2600">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2600">Az.Accounts</span></span>
- <span data-ttu-id="4bd31-2601">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2601">Changed from Az.Profile</span></span>
- <span data-ttu-id="4bd31-2602">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="4bd31-2602">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4bd31-2603">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-2603">Az.ApiManagement</span></span>
- <span data-ttu-id="4bd31-2604">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="4bd31-2604">Fixes for #7002</span></span>
- <span data-ttu-id="4bd31-2605">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="4bd31-2606">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="4bd31-2606">Az.Batch</span></span>
- <span data-ttu-id="4bd31-2607">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2607">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="4bd31-2608">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2608">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="4bd31-2609">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2609">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="4bd31-2610">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="4bd31-2610">Az.Billing</span></span>
- <span data-ttu-id="4bd31-2611">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2611">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="4bd31-2612">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2612">Az.CognitivServices</span></span>
- <span data-ttu-id="4bd31-2613">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2613">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="4bd31-2614">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="4bd31-2614">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4bd31-2615">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-2615">Az.ContainerInstance</span></span>
- <span data-ttu-id="4bd31-2616">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="4bd31-2616">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="4bd31-2617">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="4bd31-2617">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="4bd31-2618">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2618">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2619">Az.DataLakeStore</span></span>
- <span data-ttu-id="4bd31-2620">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2620">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="4bd31-2621">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="4bd31-2621">Az.Monitor</span></span>
- <span data-ttu-id="4bd31-2622">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2622">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="4bd31-2623">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="4bd31-2623">Az.KeyVault</span></span>
- <span data-ttu-id="4bd31-2624">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="4bd31-2624">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="4bd31-2625">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="4bd31-2625">Az.MachineLearning</span></span>
- <span data-ttu-id="4bd31-2626">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2626">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="4bd31-2627">Az.Media</span><span class="sxs-lookup"><span data-stu-id="4bd31-2627">Az.Media</span></span>
- <span data-ttu-id="4bd31-2628">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4bd31-2628">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4bd31-2629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2629">Az.Network</span></span>
<span data-ttu-id="4bd31-2630">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2630">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="4bd31-2631">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="4bd31-2631">New cmdlets added:</span></span>
        - <span data-ttu-id="4bd31-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2632">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4bd31-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2633">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4bd31-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2634">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4bd31-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2635">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4bd31-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2636">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="4bd31-2637">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2637">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="4bd31-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2638">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="4bd31-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd31-2639">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="4bd31-2640">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2640">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="4bd31-2641">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bd31-2641">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="4bd31-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2642">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4bd31-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4bd31-2643">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="4bd31-2644">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-2644">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="4bd31-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-2645">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="4bd31-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2646">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="4bd31-2647">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4bd31-2647">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="4bd31-2648">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd31-2648">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4bd31-2649">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd31-2649">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="4bd31-2650">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4bd31-2650">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="4bd31-2651">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4bd31-2651">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="4bd31-2652">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2652">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="4bd31-2653">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-2653">Az.OperationalInsights</span></span>
- <span data-ttu-id="4bd31-2654">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="4bd31-2655">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2655">Az.Profile</span></span>
- <span data-ttu-id="4bd31-2656">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="4bd31-2656">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2657">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2657">Az.RecoveryServices</span></span>
- <span data-ttu-id="4bd31-2658">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2658">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="4bd31-2659">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2659">Az.Resources</span></span>
- <span data-ttu-id="4bd31-2660">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2660">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4bd31-2661">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2661">Az.ServiceFabric</span></span>
- <span data-ttu-id="4bd31-2662">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="4bd31-2662">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="4bd31-2663">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2663">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="4bd31-2664">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4bd31-2664">Az.SIgnalR</span></span>
- <span data-ttu-id="4bd31-2665">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="4bd31-2665">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="4bd31-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2666">Az.Sql</span></span>
- <span data-ttu-id="4bd31-2667">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="4bd31-2667">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="4bd31-2668">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="4bd31-2668">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="4bd31-2669">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2669">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="4bd31-2670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2670">Az.Storage</span></span>
- <span data-ttu-id="4bd31-2671">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2671">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4bd31-2672">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2672">Az.Websites</span></span>
- <span data-ttu-id="4bd31-2673">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="4bd31-2673">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="4bd31-2674">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4bd31-2674">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="4bd31-2675">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-2675">General</span></span>

* <span data-ttu-id="4bd31-2676">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4bd31-2676">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="4bd31-2677">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2677">Az.Compute</span></span>

* <span data-ttu-id="4bd31-2678">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2678">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2679">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2679">Az.DataLakeStore</span></span>

* <span data-ttu-id="4bd31-2680">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="4bd31-2680">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="4bd31-2681">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="4bd31-2681">Az.FrontDoor</span></span>

* <span data-ttu-id="4bd31-2682">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="4bd31-2682">Fixed some broken links</span></span>
    - <span data-ttu-id="4bd31-2683">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2683">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="4bd31-2684">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2684">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="4bd31-2685">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2685">Az.RecoveryServices</span></span>

* <span data-ttu-id="4bd31-2686">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2686">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="4bd31-2687">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2687">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="4bd31-2688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2688">Az.Resources</span></span>

* <span data-ttu-id="4bd31-2689">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="4bd31-2689">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="4bd31-2690">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2690">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="4bd31-2691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2691">Az.Sql</span></span>

* <span data-ttu-id="4bd31-2692">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="4bd31-2692">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="4bd31-2693">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="4bd31-2693">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="4bd31-2694">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2694">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="4bd31-2695">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2695">Az.Storage</span></span>

* <span data-ttu-id="4bd31-2696">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2696">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="4bd31-2697">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="4bd31-2697">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="4bd31-2698">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2698">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4bd31-2699">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="4bd31-2699">Support Static Website configuration</span></span>
    - <span data-ttu-id="4bd31-2700">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4bd31-2700">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="4bd31-2701">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="4bd31-2701">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="4bd31-2702">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2702">Az.Websites</span></span>

* <span data-ttu-id="4bd31-2703">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4bd31-2703">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="4bd31-2704">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2704">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="4bd31-2705">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2705">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="4bd31-2706">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4bd31-2706">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="4bd31-2707">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4bd31-2707">Az.ApiManagement</span></span>
* <span data-ttu-id="4bd31-2708">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2708">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="4bd31-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="4bd31-2709">Az.Automation</span></span>
* <span data-ttu-id="4bd31-2710">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="4bd31-2710">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="4bd31-2711">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2711">Added Update Management cmdlets</span></span>
* <span data-ttu-id="4bd31-2712">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2712">Added Source Control cmdlets</span></span>
* <span data-ttu-id="4bd31-2713">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="4bd31-2713">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="4bd31-2714">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="4bd31-2714">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="4bd31-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2715">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2716">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="4bd31-2716">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="4bd31-2717">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2717">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="4bd31-2718">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-2718">Az.ContainerInstance</span></span>
* <span data-ttu-id="4bd31-2719">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2719">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="4bd31-2720">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="4bd31-2720">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="4bd31-2721">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="4bd31-2721">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="4bd31-2722">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2722">Az.Network</span></span>
* <span data-ttu-id="4bd31-2723">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2723">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="4bd31-2724">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="4bd31-2724">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="4bd31-2725">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2725">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="4bd31-2726">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bd31-2726">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="4bd31-2727">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="4bd31-2727">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="4bd31-2728">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2728">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="4bd31-2729">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2729">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="4bd31-2730">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="4bd31-2730">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="4bd31-2731">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4bd31-2731">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="4bd31-2732">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="4bd31-2732">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="4bd31-2733">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="4bd31-2733">Az.Relay</span></span>
* <span data-ttu-id="4bd31-2734">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2734">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="4bd31-2735">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2735">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2736">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="4bd31-2736">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="4bd31-2737">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="4bd31-2737">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="4bd31-2738">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="4bd31-2738">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="4bd31-2739">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2739">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-2740">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="4bd31-2740">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="4bd31-2741">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2741">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2742">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="4bd31-2742">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="4bd31-2743">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-2743">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4bd31-2744">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-2744">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4bd31-2745">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-2745">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4bd31-2746">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="4bd31-2746">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="4bd31-2747">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4bd31-2747">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4bd31-2748">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4bd31-2748">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4bd31-2749">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4bd31-2749">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="4bd31-2750">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="4bd31-2750">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="4bd31-2751">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2751">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="4bd31-2752">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2752">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="4bd31-2753">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2753">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="4bd31-2754">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2754">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4bd31-2755">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2755">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="4bd31-2756">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2756">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="4bd31-2757">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2757">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="4bd31-2758">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4bd31-2758">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="4bd31-2759">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4bd31-2759">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="4bd31-2760">Geral</span><span class="sxs-lookup"><span data-stu-id="4bd31-2760">General</span></span>
* <span data-ttu-id="4bd31-2761">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="4bd31-2761">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="4bd31-2762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2762">Az.Profile</span></span>
* <span data-ttu-id="4bd31-2763">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4bd31-2763">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="4bd31-2764">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="4bd31-2764">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="4bd31-2765">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="4bd31-2765">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="4bd31-2766">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="4bd31-2766">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="4bd31-2767">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="4bd31-2767">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="4bd31-2768">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="4bd31-2768">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="4bd31-2769">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="4bd31-2769">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-2770">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2770">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-2771">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2771">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2772">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2773">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4bd31-2773">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="4bd31-2774">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="4bd31-2774">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="4bd31-2775">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2775">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2776">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2776">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-2777">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2777">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="4bd31-2778">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2778">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="4bd31-2779">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="4bd31-2779">Az.Insights</span></span>
* <span data-ttu-id="4bd31-2780">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="4bd31-2780">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="4bd31-2781">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="4bd31-2781">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="4bd31-2782">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="4bd31-2782">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="4bd31-2783">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="4bd31-2783">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2784">Az.Network</span></span>
* <span data-ttu-id="4bd31-2785">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="4bd31-2785">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="4bd31-2786">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-2786">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="4bd31-2787">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-2787">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="4bd31-2788">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4bd31-2788">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="4bd31-2789">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-2789">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="4bd31-2790">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4bd31-2790">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="4bd31-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4bd31-2791">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="4bd31-2792">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="4bd31-2792">Az.PolicyInsights</span></span>
* <span data-ttu-id="4bd31-2793">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="4bd31-2793">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2794">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2794">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2795">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="4bd31-2795">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="4bd31-2796">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="4bd31-2796">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="4bd31-2797">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="4bd31-2797">Az.ServiceBus</span></span>
* <span data-ttu-id="4bd31-2798">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2798">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="4bd31-2799">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4bd31-2799">Az.ServiceFabric</span></span>
* <span data-ttu-id="4bd31-2800">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2800">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="4bd31-2801">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="4bd31-2801">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="4bd31-2802">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="4bd31-2802">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="4bd31-2803">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="4bd31-2803">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="4bd31-2804">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2804">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="4bd31-2805">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4bd31-2805">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="4bd31-2806">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2806">Az.Profile</span></span>
* <span data-ttu-id="4bd31-2807">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="4bd31-2807">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="4bd31-2808">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="4bd31-2808">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2809">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2809">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2810">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="4bd31-2810">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="4bd31-2811">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2811">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="4bd31-2812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4bd31-2812">Az.DataLakeStore</span></span>
* <span data-ttu-id="4bd31-2813">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="4bd31-2813">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="4bd31-2814">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2814">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="4bd31-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2815">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4bd31-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2816">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="4bd31-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2817">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2818">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2818">Az.Network</span></span>
* <span data-ttu-id="4bd31-2819">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2819">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="4bd31-2820">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2820">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2821">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2822">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2822">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="4bd31-2823">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2823">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="4bd31-2824">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="4bd31-2824">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="4bd31-2825">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2825">Azure.Storage</span></span>
* <span data-ttu-id="4bd31-2826">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2826">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="4bd31-2827">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2827">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="4bd31-2828">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="4bd31-2828">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="4bd31-2829">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2829">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="4bd31-2830">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="4bd31-2830">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="4bd31-2831">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="4bd31-2831">Az.CognitiveServices</span></span>
* <span data-ttu-id="4bd31-2832">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2832">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="4bd31-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="4bd31-2833">Az.Compute</span></span>
* <span data-ttu-id="4bd31-2834">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="4bd31-2834">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="4bd31-2835">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2835">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="4bd31-2836">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="4bd31-2836">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="4bd31-2837">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4bd31-2837">Az.DataFactoryV2</span></span>
* <span data-ttu-id="4bd31-2838">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2838">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="4bd31-2839">Az.Network</span><span class="sxs-lookup"><span data-stu-id="4bd31-2839">Az.Network</span></span>
* <span data-ttu-id="4bd31-2840">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2840">Added NetworkProfile functionality.</span></span> <span data-ttu-id="4bd31-2841">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="4bd31-2841">new cmdlets added</span></span>
    - <span data-ttu-id="4bd31-2842">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2842">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="4bd31-2843">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2843">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="4bd31-2844">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2844">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="4bd31-2845">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="4bd31-2845">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="4bd31-2846">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-2846">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="4bd31-2847">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-2847">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="4bd31-2848">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="4bd31-2848">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="4bd31-2849">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4bd31-2849">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="4bd31-2850">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="4bd31-2850">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="4bd31-2851">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="4bd31-2851">Az.RedisCache</span></span>
* <span data-ttu-id="4bd31-2852">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="4bd31-2852">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="4bd31-2853">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="4bd31-2853">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="4bd31-2854">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="4bd31-2854">Az.Resources</span></span>
* <span data-ttu-id="4bd31-2855">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4bd31-2855">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="4bd31-2856">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="4bd31-2856">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="4bd31-2857">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="4bd31-2857">Az.Sql</span></span>
* <span data-ttu-id="4bd31-2858">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="4bd31-2858">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="4bd31-2859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="4bd31-2859">Az.Websites</span></span>
* <span data-ttu-id="4bd31-2860">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="4bd31-2860">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="4bd31-2861">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="4bd31-2861">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="4bd31-2862">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="4bd31-2862">0.2.0 - September 2018</span></span>
 <span data-ttu-id="4bd31-2863">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="4bd31-2863">Initial Release</span></span>
