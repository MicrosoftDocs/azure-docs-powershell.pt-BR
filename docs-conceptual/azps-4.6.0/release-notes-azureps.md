---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 52129f31202a8ae04bf80988b5aa07b12fe081b8
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90913390"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="f22c5-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f22c5-103">Azure PowerShell release notes</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="f22c5-104">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-104">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-105">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-106">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="f22c5-106">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="f22c5-107">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="f22c5-107">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-108">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-108">Az.Automation</span></span>
* <span data-ttu-id="f22c5-109">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="f22c5-109">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-110">Az.Compute</span></span>
* <span data-ttu-id="f22c5-111">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="f22c5-111">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="f22c5-112">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="f22c5-112">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="f22c5-113">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="f22c5-113">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="f22c5-114">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-114">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-115">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-116">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="f22c5-116">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-117">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-117">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-118">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="f22c5-118">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-119">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-119">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-120">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="f22c5-120">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="f22c5-121">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="f22c5-121">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f22c5-122">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f22c5-122">Az.Maintenance</span></span>
* <span data-ttu-id="f22c5-123">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-123">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="f22c5-124">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-124">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f22c5-125">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-125">Az.ManagedServices</span></span>
* <span data-ttu-id="f22c5-126">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="f22c5-126">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-127">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-127">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-128">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="f22c5-128">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="f22c5-129">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="f22c5-129">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-130">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-130">Az.Resources</span></span>
* <span data-ttu-id="f22c5-131">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="f22c5-131">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="f22c5-132">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-132">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="f22c5-133">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-133">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="f22c5-134">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="f22c5-134">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="f22c5-135">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="f22c5-135">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f22c5-136">Foram consertados os comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com $WhatIfPreference e $ConfirmPreference.</span><span class="sxs-lookup"><span data-stu-id="f22c5-136">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with $WhatIfPreference and $ConfirmPreference.</span></span>
* <span data-ttu-id="f22c5-137">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="f22c5-137">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="f22c5-138">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="f22c5-138">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f22c5-139">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f22c5-139">Az.SignalR</span></span>
* <span data-ttu-id="f22c5-140">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="f22c5-140">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="f22c5-141">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="f22c5-141">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-142">Az.Storage</span></span>
* <span data-ttu-id="f22c5-143">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="f22c5-143">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="f22c5-144">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="f22c5-144">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="f22c5-145">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="f22c5-145">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="f22c5-146">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="f22c5-146">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="f22c5-147">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-147">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="f22c5-148">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f22c5-148">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="f22c5-149">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="f22c5-149">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="f22c5-150">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-150">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="f22c5-151">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-151">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="f22c5-152">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="f22c5-152">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="f22c5-153">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-153">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="f22c5-154">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-154">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="f22c5-155">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-155">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="f22c5-156">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-156">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="f22c5-157">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f22c5-157">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="f22c5-158">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-158">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-159">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-160">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="f22c5-160">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="f22c5-161">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="f22c5-161">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="f22c5-162">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="f22c5-162">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="f22c5-163">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="f22c5-163">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="f22c5-164">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="f22c5-164">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="f22c5-165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f22c5-165">Az.Aks</span></span>
* <span data-ttu-id="f22c5-166">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="f22c5-166">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="f22c5-167">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="f22c5-167">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-168">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-168">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-169">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-169">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="f22c5-170">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-170">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f22c5-171">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22c5-171">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f22c5-172">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="f22c5-172">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="f22c5-173">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-173">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f22c5-174">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22c5-174">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f22c5-175">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="f22c5-175">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="f22c5-176">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-176">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="f22c5-177">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-177">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f22c5-178">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22c5-178">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="f22c5-179">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-179">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="f22c5-180">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="f22c5-180">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-181">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-181">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-182">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="f22c5-182">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-183">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-183">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-184">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="f22c5-184">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-185">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-185">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-186">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="f22c5-186">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="f22c5-187">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f22c5-187">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f22c5-188">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-188">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f22c5-189">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="f22c5-189">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="f22c5-190">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f22c5-190">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="f22c5-191">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-191">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="f22c5-192">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f22c5-192">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-193">Az.Network</span></span>
* <span data-ttu-id="f22c5-194">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f22c5-194">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f22c5-195">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="f22c5-195">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="f22c5-196">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="f22c5-196">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="f22c5-197">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="f22c5-197">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-198">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-199">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="f22c5-199">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="f22c5-200">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="f22c5-200">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="f22c5-201">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f22c5-201">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-202">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-203">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-203">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-204">Az.Resources</span></span>
* <span data-ttu-id="f22c5-205">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f22c5-205">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="f22c5-206">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="f22c5-206">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-207">Az.Sql</span></span>
* <span data-ttu-id="f22c5-208">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="f22c5-208">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f22c5-209">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f22c5-209">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-210">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-210">Az.Storage</span></span>
* <span data-ttu-id="f22c5-211">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="f22c5-211">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="f22c5-212">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="f22c5-212">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="f22c5-213">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f22c5-213">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="f22c5-214">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="f22c5-214">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="f22c5-215">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="f22c5-215">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="f22c5-216">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="f22c5-216">Supported get single file share usage</span></span>
    - <span data-ttu-id="f22c5-217">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-217">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="f22c5-218">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-218">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-219">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-219">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-220">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-220">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="f22c5-221">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="f22c5-221">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f22c5-222">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f22c5-222">Az.Aks</span></span>
* <span data-ttu-id="f22c5-223">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="f22c5-223">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22c5-224">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-224">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22c5-225">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="f22c5-225">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-226">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-226">Az.Automation</span></span>
* <span data-ttu-id="f22c5-227">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="f22c5-227">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-228">Az.Compute</span></span>
* <span data-ttu-id="f22c5-229">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="f22c5-229">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-230">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-231">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f22c5-231">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22c5-232">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22c5-232">Az.EventGrid</span></span>
* <span data-ttu-id="f22c5-233">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="f22c5-233">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="f22c5-234">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-234">Added new features:</span></span>
    - <span data-ttu-id="f22c5-235">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="f22c5-235">Input mapping</span></span>
    - <span data-ttu-id="f22c5-236">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="f22c5-236">Event Delivery Schema</span></span>
    - <span data-ttu-id="f22c5-237">Link Privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-237">Private Link</span></span>
    - <span data-ttu-id="f22c5-238">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="f22c5-238">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="f22c5-239">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="f22c5-239">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="f22c5-240">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="f22c5-240">Azure Function As Destination</span></span>
    - <span data-ttu-id="f22c5-241">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="f22c5-241">WebHook Batching</span></span>
    - <span data-ttu-id="f22c5-242">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="f22c5-242">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="f22c5-243">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="f22c5-243">IpFiltering</span></span>
* <span data-ttu-id="f22c5-244">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-244">Updated cmdlets:</span></span>
    - <span data-ttu-id="f22c5-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="f22c5-245">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="f22c5-246">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="f22c5-246">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="f22c5-247">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="f22c5-247">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="f22c5-248">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-248">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="f22c5-249">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="f22c5-249">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="f22c5-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="f22c5-250">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f22c5-251">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="f22c5-251">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="f22c5-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="f22c5-252">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="f22c5-253">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-253">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-254">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-255">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="f22c5-255">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="f22c5-256">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="f22c5-256">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-257">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-258">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="f22c5-258">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-259">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-259">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-260">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="f22c5-260">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-261">Az.Network</span></span>
* <span data-ttu-id="f22c5-262">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="f22c5-262">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="f22c5-263">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-263">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="f22c5-264">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f22c5-264">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f22c5-265">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f22c5-265">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f22c5-266">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f22c5-266">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f22c5-267">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="f22c5-267">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="f22c5-268">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="f22c5-268">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="f22c5-269">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-269">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="f22c5-270">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f22c5-270">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f22c5-271">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f22c5-271">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f22c5-272">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f22c5-272">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f22c5-273">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="f22c5-273">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="f22c5-274">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="f22c5-274">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="f22c5-275">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="f22c5-275">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="f22c5-276">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-276">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f22c5-277">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-277">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="f22c5-278">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-278">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-279">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-279">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-280">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="f22c5-280">Removed project reference to Authentication</span></span>
* <span data-ttu-id="f22c5-281">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="f22c5-281">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="f22c5-282">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-282">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-283">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-283">Az.Resources</span></span>
* <span data-ttu-id="f22c5-284">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="f22c5-284">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="f22c5-285">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-285">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-286">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-286">Az.Sql</span></span>
* <span data-ttu-id="f22c5-287">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="f22c5-287">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="f22c5-288">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-288">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="f22c5-289">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="f22c5-289">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-290">Az.Storage</span></span>
* <span data-ttu-id="f22c5-291">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-291">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="f22c5-292">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="f22c5-292">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="f22c5-293">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-293">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f22c5-294">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-294">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f22c5-295">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-295">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="f22c5-296">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="f22c5-296">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="f22c5-297">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="f22c5-297">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="f22c5-298">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f22c5-298">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="f22c5-299">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="f22c5-299">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="f22c5-300">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f22c5-300">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="f22c5-301">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f22c5-301">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="f22c5-302">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="f22c5-302">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="f22c5-303">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-303">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f22c5-304">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="f22c5-304">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="f22c5-305">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="f22c5-305">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="f22c5-306">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-306">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="f22c5-307">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-307">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f22c5-308">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f22c5-308">Az.StorageSync</span></span>
* <span data-ttu-id="f22c5-309">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="f22c5-309">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="f22c5-310">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-310">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="f22c5-311">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="f22c5-311">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="f22c5-312">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f22c5-312">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-313">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-313">Az.Websites</span></span>
* <span data-ttu-id="f22c5-314">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f22c5-314">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="f22c5-315">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-315">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-316">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-317">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-317">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="f22c5-318">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="f22c5-318">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="f22c5-319">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="f22c5-319">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="f22c5-320">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="f22c5-320">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="f22c5-321">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f22c5-321">Az.Aks</span></span>
* <span data-ttu-id="f22c5-322">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="f22c5-322">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22c5-323">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-323">Az.Batch</span></span>
* <span data-ttu-id="f22c5-324">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="f22c5-324">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="f22c5-325">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-325">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-326">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-326">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-327">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="f22c5-327">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="f22c5-328">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="f22c5-328">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-329">Az.Compute</span></span>
* <span data-ttu-id="f22c5-330">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f22c5-330">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="f22c5-331">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f22c5-331">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="f22c5-332">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="f22c5-332">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="f22c5-333">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f22c5-333">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="f22c5-334">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="f22c5-334">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-335">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-335">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-336">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-336">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-337">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-337">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-338">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="f22c5-338">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f22c5-339">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f22c5-339">Az.Functions</span></span>
* <span data-ttu-id="f22c5-340">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="f22c5-340">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-341">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-341">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-342">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f22c5-342">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f22c5-343">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f22c5-343">Az.HealthcareApis</span></span>
* <span data-ttu-id="f22c5-344">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-344">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="f22c5-345">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="f22c5-345">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-346">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-346">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-347">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="f22c5-347">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="f22c5-348">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="f22c5-348">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-349">Az.Network</span></span>
* <span data-ttu-id="f22c5-350">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="f22c5-350">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="f22c5-351">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-351">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f22c5-352">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="f22c5-352">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="f22c5-353">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="f22c5-353">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="f22c5-354">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="f22c5-354">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="f22c5-355">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="f22c5-355">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="f22c5-356">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f22c5-356">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f22c5-357">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f22c5-357">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f22c5-358">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f22c5-358">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="f22c5-359">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="f22c5-359">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="f22c5-360">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="f22c5-360">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="f22c5-361">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-361">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="f22c5-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="f22c5-362">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="f22c5-363">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-363">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="f22c5-364">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="f22c5-364">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="f22c5-365">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="f22c5-365">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="f22c5-366">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="f22c5-366">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="f22c5-367">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-367">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="f22c5-368">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="f22c5-368">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="f22c5-369">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="f22c5-369">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="f22c5-370">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="f22c5-370">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="f22c5-371">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="f22c5-371">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="f22c5-372">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="f22c5-372">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="f22c5-373">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-373">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="f22c5-374">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f22c5-374">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f22c5-375">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f22c5-375">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="f22c5-376">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-376">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="f22c5-377">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f22c5-377">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="f22c5-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-378">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f22c5-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-379">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f22c5-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-380">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f22c5-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-381">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f22c5-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-382">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="f22c5-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-383">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="f22c5-384">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="f22c5-384">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="f22c5-385">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="f22c5-385">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="f22c5-386">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f22c5-386">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f22c5-387">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f22c5-387">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f22c5-388">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f22c5-388">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="f22c5-389">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="f22c5-389">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="f22c5-390">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="f22c5-390">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="f22c5-391">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-391">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f22c5-392">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-392">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="f22c5-393">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-393">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f22c5-394">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-394">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f22c5-395">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-395">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="f22c5-396">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-396">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="f22c5-397">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="f22c5-397">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="f22c5-398">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="f22c5-398">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-399">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-399">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-400">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="f22c5-400">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="f22c5-401">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="f22c5-401">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="f22c5-402">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="f22c5-402">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="f22c5-403">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f22c5-403">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f22c5-404">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f22c5-404">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-405">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-405">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-406">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-406">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="f22c5-407">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="f22c5-407">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-408">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-408">Az.Resources</span></span>
* <span data-ttu-id="f22c5-409">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="f22c5-409">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="f22c5-410">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="f22c5-410">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="f22c5-411">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="f22c5-411">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="f22c5-412">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-412">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="f22c5-413">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="f22c5-413">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="f22c5-414">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="f22c5-414">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-415">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-415">Az.Sql</span></span>
* <span data-ttu-id="f22c5-416">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f22c5-416">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="f22c5-417">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-417">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="f22c5-418">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="f22c5-418">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-419">Az.Storage</span></span>
* <span data-ttu-id="f22c5-420">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="f22c5-420">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="f22c5-421">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-421">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="f22c5-422">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-422">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-423">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-423">Az.Websites</span></span>
* <span data-ttu-id="f22c5-424">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="f22c5-424">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f22c5-425">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="f22c5-425">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="f22c5-426">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="f22c5-426">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="f22c5-427">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-427">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="f22c5-428">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="f22c5-428">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="f22c5-429">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="f22c5-429">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="f22c5-430">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-430">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-431">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-431">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-432">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="f22c5-432">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22c5-433">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-433">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22c5-434">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-434">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-435">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-435">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-436">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-436">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="f22c5-437">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f22c5-437">Az.Billing</span></span>
* <span data-ttu-id="f22c5-438">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-438">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-439">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-439">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-440">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="f22c5-440">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-441">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-442">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-442">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="f22c5-443">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-443">Az.DataShare</span></span>
* <span data-ttu-id="f22c5-444">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="f22c5-444">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="f22c5-445">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="f22c5-445">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="f22c5-446">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="f22c5-446">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-447">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-447">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-448">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-448">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="f22c5-449">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="f22c5-449">Added optional parameters to</span></span> 
    - <span data-ttu-id="f22c5-450">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f22c5-450">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="f22c5-451">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="f22c5-451">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-452">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-452">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-453">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="f22c5-453">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f22c5-454">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f22c5-454">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f22c5-455">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-455">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f22c5-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f22c5-456">Az.PrivateDns</span></span>
* <span data-ttu-id="f22c5-457">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-457">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-459">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="f22c5-459">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="f22c5-460">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f22c5-460">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-461">Az.Resources</span></span>
* <span data-ttu-id="f22c5-462">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="f22c5-462">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="f22c5-463">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f22c5-463">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="f22c5-464">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-464">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="f22c5-465">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f22c5-465">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="f22c5-466">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-466">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-467">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-467">Az.Sql</span></span>
* <span data-ttu-id="f22c5-468">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="f22c5-468">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f22c5-469">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="f22c5-469">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="f22c5-470">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="f22c5-470">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-471">Az.Storage</span></span>
* <span data-ttu-id="f22c5-472">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-472">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="f22c5-473">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-473">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f22c5-474">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="f22c5-474">Highlights since the last release</span></span>
* <span data-ttu-id="f22c5-475">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f22c5-475">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="f22c5-476">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f22c5-476">General availability of Az.Functions</span></span> 
* <span data-ttu-id="f22c5-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="f22c5-477">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-478">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-479">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="f22c5-479">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="f22c5-480">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="f22c5-480">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="f22c5-481">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f22c5-481">Az.Aks</span></span>
* <span data-ttu-id="f22c5-482">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="f22c5-482">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="f22c5-483">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="f22c5-483">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="f22c5-484">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="f22c5-484">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-485">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-485">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-486">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="f22c5-486">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="f22c5-487">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="f22c5-487">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="f22c5-488">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-488">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f22c5-489">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f22c5-489">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f22c5-490">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-490">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f22c5-491">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f22c5-491">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="f22c5-492">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-492">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f22c5-493">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f22c5-493">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f22c5-494">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-494">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="f22c5-495">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="f22c5-495">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="f22c5-496">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="f22c5-496">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="f22c5-497">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="f22c5-497">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="f22c5-498">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="f22c5-498">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="f22c5-499">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f22c5-499">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="f22c5-500">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="f22c5-500">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="f22c5-501">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="f22c5-501">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f22c5-502">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-502">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f22c5-503">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="f22c5-503">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="f22c5-504">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="f22c5-504">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="f22c5-505">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="f22c5-505">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22c5-506">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-506">Az.Batch</span></span>
* <span data-ttu-id="f22c5-507">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="f22c5-507">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="f22c5-508">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-508">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="f22c5-509">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="f22c5-509">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="f22c5-510">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-510">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="f22c5-511">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-511">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="f22c5-512">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-512">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="f22c5-513">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-513">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="f22c5-514">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-514">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="f22c5-515">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-515">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-516">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-516">Az.Compute</span></span>
* <span data-ttu-id="f22c5-517">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="f22c5-517">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="f22c5-518">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-518">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="f22c5-519">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="f22c5-519">Breaking changes</span></span>
    - <span data-ttu-id="f22c5-520">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-520">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="f22c5-521">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-521">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="f22c5-522">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-522">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="f22c5-523">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f22c5-523">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="f22c5-524">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="f22c5-524">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="f22c5-525">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="f22c5-525">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="f22c5-526">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="f22c5-526">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-527">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-527">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-528">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-528">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-529">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-529">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-530">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="f22c5-530">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f22c5-531">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="f22c5-531">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="f22c5-532">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="f22c5-532">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="f22c5-533">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="f22c5-533">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="f22c5-534">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="f22c5-534">Az.Functions</span></span>
* <span data-ttu-id="f22c5-535">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="f22c5-535">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-536">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-536">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-537">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="f22c5-537">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f22c5-538">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f22c5-538">Az.HealthcareApis</span></span>
* <span data-ttu-id="f22c5-539">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="f22c5-539">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-540">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-540">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-541">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="f22c5-541">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="f22c5-542">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="f22c5-542">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="f22c5-543">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="f22c5-543">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="f22c5-544">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="f22c5-544">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="f22c5-545">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="f22c5-545">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="f22c5-546">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-546">New cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-547">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-547">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f22c5-548">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-548">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f22c5-549">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-549">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="f22c5-550">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-550">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="f22c5-551">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="f22c5-551">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="f22c5-552">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-552">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-553">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-553">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-554">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="f22c5-554">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="f22c5-555">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="f22c5-555">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="f22c5-556">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="f22c5-556">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="f22c5-557">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="f22c5-557">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="f22c5-558">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="f22c5-558">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="f22c5-559">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="f22c5-559">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="f22c5-560">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="f22c5-560">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-561">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-561">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-562">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="f22c5-562">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="f22c5-563">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="f22c5-563">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="f22c5-564">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="f22c5-564">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="f22c5-565">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="f22c5-565">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="f22c5-566">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="f22c5-566">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="f22c5-567">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="f22c5-567">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="f22c5-568">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="f22c5-568">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-569">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-569">Az.Network</span></span>
* <span data-ttu-id="f22c5-570">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="f22c5-570">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="f22c5-571">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="f22c5-571">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="f22c5-572">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="f22c5-572">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="f22c5-573">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="f22c5-573">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="f22c5-574">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f22c5-574">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="f22c5-575">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-575">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-576">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f22c5-576">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f22c5-577">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f22c5-577">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f22c5-578">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f22c5-578">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="f22c5-579">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="f22c5-579">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="f22c5-580">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-580">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="f22c5-581">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-581">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="f22c5-582">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="f22c5-582">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="f22c5-583">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="f22c5-583">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="f22c5-584">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="f22c5-584">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="f22c5-585">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-585">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="f22c5-586">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="f22c5-586">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="f22c5-587">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f22c5-587">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f22c5-588">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f22c5-588">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f22c5-589">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f22c5-589">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="f22c5-590">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="f22c5-590">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="f22c5-591">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="f22c5-591">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="f22c5-592">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="f22c5-592">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="f22c5-593">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f22c5-593">Updated cmdlet:</span></span>
        - <span data-ttu-id="f22c5-594">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f22c5-594">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-595">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-595">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-596">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="f22c5-596">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="f22c5-597">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="f22c5-597">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="f22c5-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="f22c5-598">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="f22c5-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="f22c5-599">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="f22c5-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="f22c5-600">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="f22c5-601">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="f22c5-601">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="f22c5-602">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="f22c5-602">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="f22c5-603">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="f22c5-603">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-604">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-604">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-605">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-605">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="f22c5-606">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="f22c5-606">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="f22c5-607">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="f22c5-607">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="f22c5-608">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-608">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="f22c5-609">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="f22c5-609">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-610">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-610">Az.Resources</span></span>
* <span data-ttu-id="f22c5-611">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="f22c5-611">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="f22c5-612">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="f22c5-612">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="f22c5-613">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="f22c5-613">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="f22c5-614">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="f22c5-614">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="f22c5-615">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="f22c5-615">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="f22c5-616">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="f22c5-616">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="f22c5-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="f22c5-617">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="f22c5-618">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="f22c5-618">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="f22c5-619">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="f22c5-619">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="f22c5-620">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="f22c5-620">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="f22c5-621">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="f22c5-621">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="f22c5-622">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="f22c5-622">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="f22c5-623">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="f22c5-623">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="f22c5-624">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="f22c5-624">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="f22c5-625">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="f22c5-625">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="f22c5-626">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="f22c5-626">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="f22c5-627">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-627">'New-AzDeployment'</span></span>
    - <span data-ttu-id="f22c5-628">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-628">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="f22c5-629">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-629">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f22c5-630">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-630">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-631">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-631">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-632">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="f22c5-632">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-633">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-633">Az.Sql</span></span>
* <span data-ttu-id="f22c5-634">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="f22c5-634">Enhance performance of:</span></span>
    - <span data-ttu-id="f22c5-635">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f22c5-635">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f22c5-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f22c5-636">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f22c5-637">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f22c5-637">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f22c5-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="f22c5-638">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="f22c5-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f22c5-639">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f22c5-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f22c5-640">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f22c5-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f22c5-641">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="f22c5-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="f22c5-642">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="f22c5-643">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-643">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="f22c5-644">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="f22c5-644">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-645">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-645">Az.Storage</span></span>
* <span data-ttu-id="f22c5-646">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-646">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="f22c5-647">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="f22c5-647">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="f22c5-648">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-648">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f22c5-649">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="f22c5-649">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="f22c5-650">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="f22c5-650">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f22c5-651">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="f22c5-651">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="f22c5-652">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="f22c5-652">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="f22c5-653">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="f22c5-653">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="f22c5-654">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="f22c5-654">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="f22c5-655">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="f22c5-655">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="f22c5-656">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="f22c5-656">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="f22c5-657">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="f22c5-657">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="f22c5-658">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f22c5-658">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="f22c5-659">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-659">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="f22c5-660">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-660">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="f22c5-661">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-661">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f22c5-662">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-662">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="f22c5-663">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="f22c5-663">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="f22c5-664">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="f22c5-664">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f22c5-665">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="f22c5-665">Supported failover Storage account</span></span>
    - <span data-ttu-id="f22c5-666">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="f22c5-666">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="f22c5-667">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-667">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="f22c5-668">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-668">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="f22c5-669">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="f22c5-669">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="f22c5-670">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="f22c5-670">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f22c5-671">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="f22c5-671">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="f22c5-672">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="f22c5-672">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="f22c5-673">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-673">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f22c5-674">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-674">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="f22c5-675">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-675">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="f22c5-676">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="f22c5-676">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f22c5-677">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="f22c5-677">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="f22c5-678">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="f22c5-678">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="f22c5-679">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="f22c5-679">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="f22c5-680">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f22c5-680">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="f22c5-681">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f22c5-681">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="f22c5-682">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="f22c5-682">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="f22c5-683">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="f22c5-683">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="f22c5-684">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="f22c5-684">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f22c5-685">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f22c5-685">Az.TrafficManager</span></span>
* <span data-ttu-id="f22c5-686">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="f22c5-686">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-687">Az.Websites</span></span>
* <span data-ttu-id="f22c5-688">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-688">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="f22c5-689">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-689">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="f22c5-690">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="f22c5-690">Highlights since the last release</span></span>
* <span data-ttu-id="f22c5-691">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="f22c5-691">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-692">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-693">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="f22c5-693">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-694">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-694">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-695">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="f22c5-695">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f22c5-696">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="f22c5-696">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22c5-697">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-697">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-698">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="f22c5-698">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-699">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-699">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-700">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="f22c5-700">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-701">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-701">Az.Compute</span></span>
* <span data-ttu-id="f22c5-702">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-702">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="f22c5-703">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="f22c5-703">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-704">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-705">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-705">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-706">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f22c5-706">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="f22c5-707">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="f22c5-707">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="f22c5-708">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="f22c5-708">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="f22c5-709">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-709">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-710">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f22c5-710">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="f22c5-711">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="f22c5-711">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="f22c5-712">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="f22c5-712">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="f22c5-713">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-713">New cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-714">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-714">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f22c5-715">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-715">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f22c5-716">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-716">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="f22c5-717">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-717">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="f22c5-718">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="f22c5-718">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-719">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-719">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-720">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="f22c5-720">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="f22c5-721">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="f22c5-721">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="f22c5-722">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="f22c5-722">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="f22c5-723">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-723">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="f22c5-724">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="f22c5-724">Az.Maintenance</span></span>
* <span data-ttu-id="f22c5-725">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-725">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-726">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-726">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-727">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-727">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="f22c5-728">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f22c5-728">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f22c5-729">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f22c5-729">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f22c5-730">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f22c5-730">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f22c5-731">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="f22c5-731">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="f22c5-732">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f22c5-732">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f22c5-733">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f22c5-733">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="f22c5-734">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="f22c5-734">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-735">Az.Network</span></span>
* <span data-ttu-id="f22c5-736">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="f22c5-736">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="f22c5-737">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f22c5-737">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f22c5-738">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f22c5-738">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="f22c5-739">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-739">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="f22c5-740">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-740">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="f22c5-741">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="f22c5-741">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="f22c5-742">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="f22c5-742">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="f22c5-743">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="f22c5-743">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="f22c5-744">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="f22c5-744">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="f22c5-745">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-745">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f22c5-746">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="f22c5-746">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="f22c5-747">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="f22c5-747">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="f22c5-748">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="f22c5-748">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="f22c5-749">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="f22c5-749">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="f22c5-750">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-750">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="f22c5-751">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-751">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-752">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-752">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-753">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="f22c5-753">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="f22c5-754">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="f22c5-754">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-755">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-755">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-756">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="f22c5-756">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-757">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-757">Az.Sql</span></span>
* <span data-ttu-id="f22c5-758">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-758">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="f22c5-759">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="f22c5-759">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-760">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-760">Az.Storage</span></span>
* <span data-ttu-id="f22c5-761">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="f22c5-761">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="f22c5-762">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-762">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="f22c5-763">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-763">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="f22c5-764">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-764">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="f22c5-765">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="f22c5-765">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="f22c5-766">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f22c5-766">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f22c5-767">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f22c5-767">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f22c5-768">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="f22c5-768">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="f22c5-769">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f22c5-769">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f22c5-770">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="f22c5-770">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="f22c5-771">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f22c5-771">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="f22c5-772">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-772">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="f22c5-773">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="f22c5-773">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="f22c5-774">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-774">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="f22c5-775">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-775">General</span></span>
* <span data-ttu-id="f22c5-776">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="f22c5-776">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="f22c5-777">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="f22c5-777">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="f22c5-778">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="f22c5-778">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="f22c5-779">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="f22c5-779">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="f22c5-780">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f22c5-780">Az.Billing</span></span>
  - <span data-ttu-id="f22c5-781">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-781">Az.Compute</span></span>
  - <span data-ttu-id="f22c5-782">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f22c5-782">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="f22c5-783">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-783">Az.EventHub</span></span>
  - <span data-ttu-id="f22c5-784">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-784">Az.IotHub</span></span>
  - <span data-ttu-id="f22c5-785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-785">Az.KeyVault</span></span>
  - <span data-ttu-id="f22c5-786">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-786">Az.Monitor</span></span>
  - <span data-ttu-id="f22c5-787">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-787">Az.Network</span></span>
  - <span data-ttu-id="f22c5-788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-788">Az.Resources</span></span>
  - <span data-ttu-id="f22c5-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-789">Az.Storage</span></span>
  - <span data-ttu-id="f22c5-790">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-790">Az.Websites</span></span>
* <span data-ttu-id="f22c5-791">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-791">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="f22c5-792">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="f22c5-792">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="f22c5-793">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="f22c5-793">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="f22c5-794">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-794">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-795">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-796">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="f22c5-796">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-797">Az.Compute</span></span>
* <span data-ttu-id="f22c5-798">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="f22c5-798">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="f22c5-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="f22c5-799">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="f22c5-800">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-800">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="f22c5-801">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-801">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="f22c5-802">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="f22c5-802">[#11354]</span></span>
* <span data-ttu-id="f22c5-803">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="f22c5-803">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="f22c5-804">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f22c5-804">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f22c5-805">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f22c5-805">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f22c5-806">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f22c5-806">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="f22c5-807">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="f22c5-807">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="f22c5-808">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-808">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="f22c5-809">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="f22c5-809">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="f22c5-810">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-810">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="f22c5-811">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="f22c5-811">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-812">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-813">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-813">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="f22c5-814">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="f22c5-814">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-815">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-815">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-816">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="f22c5-816">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="f22c5-817">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-817">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-818">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-818">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-819">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="f22c5-819">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-820">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-820">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-821">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f22c5-821">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="f22c5-822">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-822">New Cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-823">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="f22c5-823">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="f22c5-824">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="f22c5-824">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-825">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-825">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-826">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="f22c5-826">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-827">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-827">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-828">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="f22c5-828">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-829">Az.Network</span></span>
* <span data-ttu-id="f22c5-830">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="f22c5-830">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="f22c5-831">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-831">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f22c5-832">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="f22c5-832">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="f22c5-833">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="f22c5-833">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="f22c5-834">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="f22c5-834">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="f22c5-835">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="f22c5-835">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-836">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-836">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-837">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="f22c5-837">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-838">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-838">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-839">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="f22c5-839">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="f22c5-840">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="f22c5-840">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="f22c5-841">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="f22c5-841">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="f22c5-842">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="f22c5-842">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="f22c5-843">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-843">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="f22c5-844">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="f22c5-844">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-845">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-845">Az.Resources</span></span>
* <span data-ttu-id="f22c5-846">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="f22c5-846">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="f22c5-847">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="f22c5-847">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="f22c5-848">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-848">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="f22c5-849">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-849">Added example.</span></span>
* <span data-ttu-id="f22c5-850">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="f22c5-850">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="f22c5-851">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="f22c5-851">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-852">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-852">Az.Sql</span></span>
* <span data-ttu-id="f22c5-853">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="f22c5-853">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="f22c5-854">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-854">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="f22c5-855">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-855">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="f22c5-856">Az.Support</span><span class="sxs-lookup"><span data-stu-id="f22c5-856">Az.Support</span></span>
* <span data-ttu-id="f22c5-857">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="f22c5-857">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-858">Az.Websites</span></span>
* <span data-ttu-id="f22c5-859">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="f22c5-859">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="f22c5-860">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f22c5-860">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f22c5-861">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f22c5-861">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f22c5-862">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f22c5-862">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="f22c5-863">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="f22c5-863">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="f22c5-864">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-864">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-865">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-866">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="f22c5-866">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="f22c5-867">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="f22c5-867">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="f22c5-868">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="f22c5-868">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-869">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-870">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="f22c5-870">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="f22c5-871">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="f22c5-871">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="f22c5-872">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="f22c5-872">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="f22c5-873">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="f22c5-873">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-874">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-875">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="f22c5-875">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-876">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-876">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-877">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="f22c5-877">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f22c5-878">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-878">New Cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-879">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-879">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f22c5-880">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-880">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f22c5-881">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-881">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f22c5-882">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-882">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="f22c5-883">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="f22c5-883">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="f22c5-884">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-884">New Cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-885">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f22c5-885">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="f22c5-886">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f22c5-886">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="f22c5-887">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f22c5-887">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="f22c5-888">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="f22c5-888">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="f22c5-889">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="f22c5-889">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f22c5-890">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="f22c5-890">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="f22c5-891">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="f22c5-891">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="f22c5-892">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-892">New Cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-893">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-893">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="f22c5-894">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="f22c5-894">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="f22c5-895">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f22c5-895">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-896">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-896">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-897">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="f22c5-897">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-898">Az.Network</span></span>
* <span data-ttu-id="f22c5-899">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="f22c5-899">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="f22c5-900">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="f22c5-900">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="f22c5-901">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="f22c5-901">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="f22c5-902">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-902">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-903">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-903">Az.Resources</span></span>
* <span data-ttu-id="f22c5-904">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-904">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="f22c5-905">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="f22c5-905">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="f22c5-906">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="f22c5-906">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="f22c5-907">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="f22c5-907">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="f22c5-908">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="f22c5-908">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="f22c5-909">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="f22c5-909">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="f22c5-910">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="f22c5-910">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="f22c5-911">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22c5-911">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="f22c5-912">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22c5-912">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f22c5-913">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22c5-913">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="f22c5-914">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22c5-914">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="f22c5-915">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-915">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="f22c5-916">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22c5-916">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="f22c5-917">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-917">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-918">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-918">Az.Sql</span></span>
* <span data-ttu-id="f22c5-919">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-919">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="f22c5-920">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="f22c5-920">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="f22c5-921">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="f22c5-921">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="f22c5-922">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="f22c5-922">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="f22c5-923">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="f22c5-923">Remove an LTR backup</span></span>
    - <span data-ttu-id="f22c5-924">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="f22c5-924">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="f22c5-925">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="f22c5-925">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="f22c5-926">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-926">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="f22c5-927">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-927">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-928">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-928">Az.Storage</span></span>
* <span data-ttu-id="f22c5-929">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-929">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="f22c5-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-930">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="f22c5-931">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="f22c5-931">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="f22c5-932">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="f22c5-932">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="f22c5-933">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="f22c5-933">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-934">Az.Websites</span></span>
* <span data-ttu-id="f22c5-935">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="f22c5-935">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="f22c5-936">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="f22c5-936">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="f22c5-937">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f22c5-937">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="f22c5-938">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="f22c5-938">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="f22c5-939">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f22c5-939">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="f22c5-940">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-940">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22c5-941">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f22c5-941">Highlights since the last major release</span></span>
* <span data-ttu-id="f22c5-942">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-942">Updated client side telemetry.</span></span>
* <span data-ttu-id="f22c5-943">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-943">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="f22c5-944">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="f22c5-944">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-945">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-946">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="f22c5-946">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-947">Az.Automation</span></span>
* <span data-ttu-id="f22c5-948">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="f22c5-948">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-949">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-949">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-950">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-950">Updated SDK to 7.0</span></span>
* <span data-ttu-id="f22c5-951">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="f22c5-951">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-952">Az.Compute</span></span>
* <span data-ttu-id="f22c5-953">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="f22c5-953">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-954">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-954">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-955">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="f22c5-955">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-956">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-956">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-957">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="f22c5-957">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="f22c5-958">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-958">New Cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-959">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-959">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f22c5-960">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-960">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f22c5-961">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-961">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="f22c5-962">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="f22c5-962">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-963">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-963">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-964">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="f22c5-964">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-965">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-965">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-966">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="f22c5-966">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="f22c5-967">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-967">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="f22c5-968">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="f22c5-968">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-969">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-969">Az.Network</span></span>
* <span data-ttu-id="f22c5-970">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-970">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="f22c5-971">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f22c5-971">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f22c5-972">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="f22c5-972">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="f22c5-973">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="f22c5-973">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="f22c5-974">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-974">No new cmdlets are added.</span></span> <span data-ttu-id="f22c5-975">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="f22c5-975">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-976">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-976">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-977">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f22c5-977">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-978">Az.Resources</span></span>
* <span data-ttu-id="f22c5-979">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="f22c5-979">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="f22c5-980">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f22c5-980">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="f22c5-981">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="f22c5-981">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="f22c5-982">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="f22c5-982">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="f22c5-983">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f22c5-983">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="f22c5-984">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="f22c5-984">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="f22c5-985">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="f22c5-985">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="f22c5-986">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-986">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-987">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-987">Az.Sql</span></span>
* <span data-ttu-id="f22c5-988">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-988">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="f22c5-989">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="f22c5-989">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="f22c5-990">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="f22c5-990">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f22c5-991">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f22c5-991">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f22c5-992">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="f22c5-992">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f22c5-993">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f22c5-993">Az.StorageSync</span></span>
* <span data-ttu-id="f22c5-994">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-994">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="f22c5-995">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-995">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22c5-996">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f22c5-996">Highlights since the last major release</span></span>
* <span data-ttu-id="f22c5-997">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f22c5-997">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="f22c5-998">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-998">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-999">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-999">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1000">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="f22c5-1000">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="f22c5-1001">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="f22c5-1001">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-1002">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-1002">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-1003">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="f22c5-1003">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="f22c5-1004">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="f22c5-1004">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="f22c5-1005">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="f22c5-1005">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="f22c5-1006">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1006">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1007">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1007">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1008">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1008">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="f22c5-1009">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1009">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="f22c5-1010">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1010">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="f22c5-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1011">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="f22c5-1012">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1012">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1013">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1013">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1014">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1014">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f22c5-1015">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f22c5-1015">Az.DeploymentManager</span></span>
* <span data-ttu-id="f22c5-1016">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1016">Adds LIST operations for resources</span></span>
* <span data-ttu-id="f22c5-1017">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="f22c5-1017">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-1018">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-1018">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-1019">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1019">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-1020">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-1020">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-1021">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1021">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1022">Az.Network</span></span>
* <span data-ttu-id="f22c5-1023">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1023">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="f22c5-1024">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-1024">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="f22c5-1025">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1025">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f22c5-1026">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="f22c5-1026">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="f22c5-1027">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1027">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="f22c5-1028">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1028">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="f22c5-1029">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1029">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="f22c5-1030">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1030">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="f22c5-1031">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1031">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-1032">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="f22c5-1033">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-1033">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="f22c5-1034">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1034">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="f22c5-1035">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="f22c5-1035">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-1036">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1036">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-1037">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="f22c5-1037">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="f22c5-1038">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="f22c5-1038">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="f22c5-1039">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="f22c5-1039">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="f22c5-1040">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="f22c5-1040">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1041">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1041">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1042">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1042">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="f22c5-1043">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1043">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1044">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1044">Az.Resources</span></span>
* <span data-ttu-id="f22c5-1045">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="f22c5-1045">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="f22c5-1046">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="f22c5-1046">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1047">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1047">Az.Sql</span></span>
<span data-ttu-id="f22c5-1048">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1048">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1049">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1049">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1050">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-1050">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="f22c5-1051">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1051">New-AzStorageAccount</span></span>
* <span data-ttu-id="f22c5-1052">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="f22c5-1052">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="f22c5-1053">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1053">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-1054">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-1054">Az.Websites</span></span>
* <span data-ttu-id="f22c5-1055">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="f22c5-1055">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="f22c5-1056">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="f22c5-1056">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="f22c5-1057">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="f22c5-1057">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1058">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1058">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1059">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f22c5-1059">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22c5-1060">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-1060">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-1061">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22c5-1061">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1062">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1062">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1063">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1063">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f22c5-1064">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-1064">Az.ContainerInstance</span></span>
* <span data-ttu-id="f22c5-1065">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1065">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f22c5-1066">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1066">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f22c5-1067">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1067">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f22c5-1068">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1068">Get the Edge Storage Container</span></span>
* <span data-ttu-id="f22c5-1069">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1069">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f22c5-1070">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1070">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="f22c5-1071">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1071">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f22c5-1072">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1072">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="f22c5-1073">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1073">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="f22c5-1074">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1074">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="f22c5-1075">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1075">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f22c5-1076">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1076">Get the Edge Storage Account</span></span>
* <span data-ttu-id="f22c5-1077">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1077">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f22c5-1078">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1078">Create new Edge Storage Account</span></span>
* <span data-ttu-id="f22c5-1079">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1079">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="f22c5-1080">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1080">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="f22c5-1081">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1081">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="f22c5-1082">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-1082">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="f22c5-1083">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1083">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="f22c5-1084">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1084">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1085">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1085">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1086">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f22c5-1086">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="f22c5-1087">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1087">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="f22c5-1088">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1088">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="f22c5-1089">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="f22c5-1089">Az.DevTestLabs</span></span>
* <span data-ttu-id="f22c5-1090">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="f22c5-1090">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1091">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-1092">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="f22c5-1092">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-1093">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-1093">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-1094">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1094">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f22c5-1095">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f22c5-1095">Az.MachineLearning</span></span>
* <span data-ttu-id="f22c5-1096">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="f22c5-1096">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="f22c5-1097">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f22c5-1097">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="f22c5-1098">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="f22c5-1098">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="f22c5-1099">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f22c5-1099">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="f22c5-1100">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f22c5-1100">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="f22c5-1101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="f22c5-1101">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="f22c5-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="f22c5-1102">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="f22c5-1103">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1103">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1104">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1104">Az.Network</span></span>
* <span data-ttu-id="f22c5-1105">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="f22c5-1105">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1106">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1106">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1107">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1107">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="f22c5-1108">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1108">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f22c5-1109">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1109">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="f22c5-1110">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1110">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1111">Az.Resources</span></span>
* <span data-ttu-id="f22c5-1112">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1112">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1113">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1114">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1114">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="f22c5-1115">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="f22c5-1115">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="f22c5-1116">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f22c5-1116">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="f22c5-1117">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="f22c5-1117">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1118">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1118">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1119">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="f22c5-1119">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="f22c5-1120">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1120">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="f22c5-1121">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="f22c5-1121">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="f22c5-1122">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1122">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="f22c5-1123">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1123">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="f22c5-1124">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-1124">General</span></span>
* <span data-ttu-id="f22c5-1125">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1125">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1126">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1127">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="f22c5-1127">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="f22c5-1128">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="f22c5-1128">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22c5-1129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-1129">Az.Batch</span></span>
* <span data-ttu-id="f22c5-1130">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1130">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1131">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1132">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1132">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-1133">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1133">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-1134">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="f22c5-1134">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="f22c5-1135">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="f22c5-1135">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f22c5-1136">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f22c5-1136">Az.HealthcareApis</span></span>
* <span data-ttu-id="f22c5-1137">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="f22c5-1137">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-1138">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-1138">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-1139">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="f22c5-1139">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="f22c5-1140">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="f22c5-1140">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="f22c5-1141">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1141">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-1142">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1142">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-1143">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1143">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="f22c5-1144">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="f22c5-1144">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="f22c5-1145">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1145">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1146">Az.Network</span></span>
* <span data-ttu-id="f22c5-1147">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1147">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1148">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1148">Az.Resources</span></span>
* <span data-ttu-id="f22c5-1149">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1149">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="f22c5-1150">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1150">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1151">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1152">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="f22c5-1152">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1153">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1153">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1154">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="f22c5-1154">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="f22c5-1155">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f22c5-1155">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="f22c5-1156">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f22c5-1156">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="f22c5-1157">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1157">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="f22c5-1158">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="f22c5-1158">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="f22c5-1159">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1159">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="f22c5-1160">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1160">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="f22c5-1161">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-1161">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="f22c5-1162">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-1162">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="f22c5-1163">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1163">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="f22c5-1164">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="f22c5-1164">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="f22c5-1165">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="f22c5-1165">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="f22c5-1166">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="f22c5-1166">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="f22c5-1167">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1167">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22c5-1168">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f22c5-1168">Highlights since the last major release</span></span>
* <span data-ttu-id="f22c5-1169">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1169">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="f22c5-1170">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1170">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1171">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1172">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="f22c5-1172">VM Reapply feature</span></span>
    - <span data-ttu-id="f22c5-1173">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="f22c5-1173">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="f22c5-1174">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1174">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="f22c5-1175">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-1175">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="f22c5-1176">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f22c5-1176">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="f22c5-1177">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-1177">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f22c5-1178">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f22c5-1178">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="f22c5-1179">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="f22c5-1179">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="f22c5-1180">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f22c5-1180">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="f22c5-1181">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="f22c5-1181">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="f22c5-1182">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-1182">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="f22c5-1183">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="f22c5-1183">Az.DataBoxEdge</span></span>
* <span data-ttu-id="f22c5-1184">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1184">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f22c5-1185">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="f22c5-1185">Get the Order</span></span>
* <span data-ttu-id="f22c5-1186">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1186">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f22c5-1187">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="f22c5-1187">Create new Order</span></span>
* <span data-ttu-id="f22c5-1188">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1188">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="f22c5-1189">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="f22c5-1189">Remove the Order</span></span>
* <span data-ttu-id="f22c5-1190">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="f22c5-1190">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="f22c5-1191">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="f22c5-1191">Now creates Local Share</span></span>
* <span data-ttu-id="f22c5-1192">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1192">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="f22c5-1193">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="f22c5-1193">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="f22c5-1194">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1194">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="f22c5-1195">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1195">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="f22c5-1196">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1196">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f22c5-1197">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1197">Gets the information about Triggers</span></span>
* <span data-ttu-id="f22c5-1198">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1198">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f22c5-1199">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1199">Create new Triggers</span></span>
* <span data-ttu-id="f22c5-1200">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1200">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="f22c5-1201">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1201">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1202">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1202">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1203">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1203">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="f22c5-1204">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1204">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-1205">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-1205">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-1206">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f22c5-1206">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-1207">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1207">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-1208">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="f22c5-1208">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-1209">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1209">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-1210">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-1210">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="f22c5-1211">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-1211">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="f22c5-1212">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="f22c5-1212">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="f22c5-1213">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-1213">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1214">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1214">Az.Network</span></span>
* <span data-ttu-id="f22c5-1215">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1215">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="f22c5-1216">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="f22c5-1216">Az.PrivateDns</span></span>
* <span data-ttu-id="f22c5-1217">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1217">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1218">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1218">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1219">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1219">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="f22c5-1220">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1220">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="f22c5-1221">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1221">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f22c5-1222">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f22c5-1222">Az.RedisCache</span></span>
* <span data-ttu-id="f22c5-1223">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1223">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="f22c5-1224">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1224">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="f22c5-1225">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1225">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1226">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1226">Az.Resources</span></span>
- <span data-ttu-id="f22c5-1227">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1227">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="f22c5-1228">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1228">Updated create policy definition help example</span></span>
- <span data-ttu-id="f22c5-1229">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1229">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="f22c5-1230">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1230">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="f22c5-1231">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1231">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1232">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1232">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1233">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1233">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="f22c5-1234">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="f22c5-1234">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="f22c5-1235">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1235">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="f22c5-1236">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-1236">General</span></span>
* <span data-ttu-id="f22c5-1237">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1237">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1238">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1238">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1239">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1239">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f22c5-1240">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1240">Az.Advisor</span></span>
* <span data-ttu-id="f22c5-1241">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1241">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22c5-1242">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-1242">Az.Batch</span></span>
* <span data-ttu-id="f22c5-1243">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1243">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="f22c5-1244">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1244">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="f22c5-1245">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1245">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="f22c5-1246">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1246">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="f22c5-1247">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1247">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="f22c5-1248">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1248">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="f22c5-1249">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1249">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="f22c5-1250">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1250">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="f22c5-1251">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1251">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="f22c5-1252">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1252">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f22c5-1253">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1253">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="f22c5-1254">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1254">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="f22c5-1255">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1255">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="f22c5-1256">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1256">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="f22c5-1257">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1257">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="f22c5-1258">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1258">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="f22c5-1259">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1259">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="f22c5-1260">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1260">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="f22c5-1261">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1261">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="f22c5-1262">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1262">This operation is no longer supported.</span></span>
* <span data-ttu-id="f22c5-1263">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1263">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f22c5-1264">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1264">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="f22c5-1265">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1265">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="f22c5-1266">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1266">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="f22c5-1267">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1267">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="f22c5-1268">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1268">New non-verified images are also now returned.</span></span> <span data-ttu-id="f22c5-1269">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1269">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="f22c5-1270">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1270">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="f22c5-1271">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1271">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="f22c5-1272">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1272">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="f22c5-1273">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1273">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="f22c5-1274">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1274">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="f22c5-1275">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1275">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="f22c5-1276">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1276">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="f22c5-1277">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="f22c5-1277">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="f22c5-1278">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="f22c5-1278">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22c5-1279">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-1279">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-1280">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1280">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="f22c5-1281">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1281">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1282">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1282">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1283">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="f22c5-1283">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="f22c5-1284">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1284">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="f22c5-1285">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f22c5-1285">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="f22c5-1286">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1286">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f22c5-1287">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1287">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="f22c5-1288">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="f22c5-1288">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="f22c5-1289">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-1289">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="f22c5-1290">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="f22c5-1290">Breaking changes</span></span>
    - <span data-ttu-id="f22c5-1291">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1291">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="f22c5-1292">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f22c5-1292">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1293">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1293">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1294">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1294">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-1295">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-1295">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-1296">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="f22c5-1296">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="f22c5-1297">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1297">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="f22c5-1298">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="f22c5-1298">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="f22c5-1299">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="f22c5-1299">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="f22c5-1300">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="f22c5-1300">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="f22c5-1301">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="f22c5-1301">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-1303">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1303">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-1304">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-1304">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-1305">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1305">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="f22c5-1306">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1306">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="f22c5-1307">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1307">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="f22c5-1308">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1308">Removed five cmdlets:</span></span>
    - <span data-ttu-id="f22c5-1309">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f22c5-1309">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f22c5-1310">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f22c5-1310">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f22c5-1311">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="f22c5-1311">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="f22c5-1312">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f22c5-1312">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="f22c5-1313">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f22c5-1313">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="f22c5-1314">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1314">Added three cmdlets:</span></span>
    - <span data-ttu-id="f22c5-1315">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1315">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f22c5-1316">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1316">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="f22c5-1317">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1317">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="f22c5-1318">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1318">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="f22c5-1319">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1319">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="f22c5-1320">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1320">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="f22c5-1321">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1321">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="f22c5-1322">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1322">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="f22c5-1323">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1323">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="f22c5-1324">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1324">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="f22c5-1325">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1325">Added some scenario test cases.</span></span>
* <span data-ttu-id="f22c5-1326">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1326">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1327">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-1328">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1328">Breaking changes:</span></span>
    - <span data-ttu-id="f22c5-1329">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1329">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f22c5-1330">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1330">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f22c5-1331">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1331">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f22c5-1332">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1332">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f22c5-1333">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1333">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="f22c5-1334">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1334">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="f22c5-1335">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1335">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="f22c5-1336">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1336">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="f22c5-1337">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1337">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f22c5-1338">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1338">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="f22c5-1339">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1339">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="f22c5-1340">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1340">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1341">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1341">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1342">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1342">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="f22c5-1343">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1343">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="f22c5-1344">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1344">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="f22c5-1345">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1345">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="f22c5-1346">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1346">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="f22c5-1347">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1347">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="f22c5-1348">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1348">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="f22c5-1349">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1349">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="f22c5-1350">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="f22c5-1350">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1351">Az.Resources</span></span>
* <span data-ttu-id="f22c5-1352">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="f22c5-1352">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1353">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1353">Az.Network</span></span>
* <span data-ttu-id="f22c5-1354">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1354">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="f22c5-1355">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1355">Updated cmdlet:</span></span>
        - <span data-ttu-id="f22c5-1356">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1356">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1357">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1357">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1358">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1358">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1359">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1359">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1360">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1360">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f22c5-1361">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1361">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="f22c5-1362">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1362">New cmdlet:</span></span>
        - <span data-ttu-id="f22c5-1363">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="f22c5-1363">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="f22c5-1364">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1364">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="f22c5-1365">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1365">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="f22c5-1366">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1366">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="f22c5-1367">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1367">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="f22c5-1368">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1368">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="f22c5-1369">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-1369">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="f22c5-1370">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1370">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="f22c5-1371">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1371">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-1372">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1372">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="f22c5-1373">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-1373">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f22c5-1374">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-1374">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f22c5-1375">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-1375">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="f22c5-1376">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1376">Set-AzVirtualHub</span></span>
* <span data-ttu-id="f22c5-1377">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="f22c5-1377">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="f22c5-1378">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1378">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f22c5-1379">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1379">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f22c5-1380">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1380">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="f22c5-1381">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1381">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="f22c5-1382">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1382">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="f22c5-1383">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1383">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="f22c5-1384">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1384">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-1385">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1385">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="f22c5-1386">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f22c5-1387">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1387">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f22c5-1388">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1388">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f22c5-1389">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1389">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f22c5-1390">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1390">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="f22c5-1391">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1391">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="f22c5-1392">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="f22c5-1392">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="f22c5-1393">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1393">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-1394">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="f22c5-1394">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="f22c5-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="f22c5-1395">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="f22c5-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f22c5-1396">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="f22c5-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f22c5-1397">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="f22c5-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-1398">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="f22c5-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1399">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="f22c5-1400">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1400">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f22c5-1401">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1401">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="f22c5-1402">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-1402">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="f22c5-1403">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="f22c5-1403">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="f22c5-1404">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="f22c5-1404">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="f22c5-1405">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1405">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="f22c5-1406">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1406">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="f22c5-1407">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1407">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="f22c5-1408">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="f22c5-1408">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="f22c5-1409">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-1409">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="f22c5-1410">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1410">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="f22c5-1411">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1411">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-1412">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1412">New-AzIpGroup</span></span>
        - <span data-ttu-id="f22c5-1413">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1413">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="f22c5-1414">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1414">Get-AzIpGroup</span></span>
        - <span data-ttu-id="f22c5-1415">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1415">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-1416">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-1416">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-1417">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1417">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1418">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1419">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1419">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="f22c5-1420">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1420">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="f22c5-1421">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1421">Removed deprecated aliases:</span></span>
* <span data-ttu-id="f22c5-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1422">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="f22c5-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1423">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="f22c5-1424">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1424">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f22c5-1425">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1425">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="f22c5-1426">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="f22c5-1426">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="f22c5-1427">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1427">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1428">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1429">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-1429">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="f22c5-1430">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1430">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f22c5-1431">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1431">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f22c5-1432">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="f22c5-1432">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="f22c5-1433">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f22c5-1433">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="f22c5-1434">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f22c5-1434">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="f22c5-1435">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1435">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="f22c5-1436">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-1436">General</span></span>
* <span data-ttu-id="f22c5-1437">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1437">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1438">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1438">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1439">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1439">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-1440">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-1440">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-1441">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1441">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="f22c5-1442">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="f22c5-1442">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-1443">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-1443">Az.Automation</span></span>
* <span data-ttu-id="f22c5-1444">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1444">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22c5-1445">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-1445">Az.Batch</span></span>
* <span data-ttu-id="f22c5-1446">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1446">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1447">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1447">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1448">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-1448">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="f22c5-1449">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f22c5-1449">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="f22c5-1450">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1450">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="f22c5-1451">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1451">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1452">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1452">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1453">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1453">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="f22c5-1454">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1454">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="f22c5-1455">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1455">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-1456">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-1456">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-1457">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="f22c5-1457">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="f22c5-1458">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="f22c5-1458">Az.HealthcareApis</span></span>
* <span data-ttu-id="f22c5-1459">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1459">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="f22c5-1460">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="f22c5-1460">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="f22c5-1461">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="f22c5-1461">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="f22c5-1462">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1462">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-1463">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1463">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-1464">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="f22c5-1464">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="f22c5-1465">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="f22c5-1465">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-1466">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1466">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-1467">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="f22c5-1467">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="f22c5-1468">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1468">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="f22c5-1469">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="f22c5-1469">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="f22c5-1470">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1470">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1471">Az.Network</span></span>
* <span data-ttu-id="f22c5-1472">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1472">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="f22c5-1473">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="f22c5-1473">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="f22c5-1474">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1474">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-1475">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1475">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="f22c5-1476">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1476">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f22c5-1477">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="f22c5-1477">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="f22c5-1478">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1478">Updated cmdlets:</span></span>
        - <span data-ttu-id="f22c5-1479">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1479">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f22c5-1480">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1480">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f22c5-1481">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1481">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f22c5-1482">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="f22c5-1482">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="f22c5-1483">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="f22c5-1483">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="f22c5-1484">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1484">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="f22c5-1485">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1485">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f22c5-1486">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f22c5-1486">Az.RedisCache</span></span>
* <span data-ttu-id="f22c5-1487">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1487">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1488">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1488">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1489">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="f22c5-1489">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1490">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1490">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1491">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-1491">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="f22c5-1492">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f22c5-1492">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f22c5-1493">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f22c5-1493">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="f22c5-1494">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="f22c5-1494">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="f22c5-1495">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1495">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f22c5-1496">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f22c5-1496">Az.StorageSync</span></span>
* <span data-ttu-id="f22c5-1497">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1497">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-1498">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-1498">Az.Websites</span></span>
* <span data-ttu-id="f22c5-1499">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="f22c5-1499">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="f22c5-1500">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1500">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-1501">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-1501">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-1502">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1502">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="f22c5-1503">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1503">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="f22c5-1504">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1504">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-1505">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-1505">Az.Automation</span></span>
* <span data-ttu-id="f22c5-1506">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1506">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="f22c5-1507">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="f22c5-1507">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="f22c5-1508">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1508">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1509">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1510">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1510">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="f22c5-1511">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1511">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f22c5-1512">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1512">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="f22c5-1513">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1513">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="f22c5-1514">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1514">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="f22c5-1515">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1515">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="f22c5-1516">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1516">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="f22c5-1517">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1517">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="f22c5-1518">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1518">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1519">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1520">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f22c5-1520">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="f22c5-1521">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="f22c5-1521">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-1522">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-1522">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-1523">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="f22c5-1523">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-1524">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1524">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-1525">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1525">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="f22c5-1526">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1526">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="f22c5-1527">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1527">New cmdlets are:</span></span>
    - <span data-ttu-id="f22c5-1528">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f22c5-1528">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f22c5-1529">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f22c5-1529">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f22c5-1530">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f22c5-1530">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="f22c5-1531">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="f22c5-1531">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-1532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1532">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-1533">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="f22c5-1533">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="f22c5-1534">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1534">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="f22c5-1535">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1535">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="f22c5-1536">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1536">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="f22c5-1537">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1537">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="f22c5-1538">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1538">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="f22c5-1539">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1539">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="f22c5-1540">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1540">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="f22c5-1541">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1541">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f22c5-1542">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1542">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="f22c5-1543">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1543">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="f22c5-1544">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1544">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="f22c5-1545">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="f22c5-1545">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="f22c5-1546">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="f22c5-1546">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="f22c5-1547">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="f22c5-1547">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="f22c5-1548">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1548">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="f22c5-1549">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1549">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="f22c5-1550">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-1550">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="f22c5-1551">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1551">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="f22c5-1552">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-1552">Overall improved help files</span></span>
* <span data-ttu-id="f22c5-1553">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1553">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1554">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1554">Az.Network</span></span>
* <span data-ttu-id="f22c5-1555">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1555">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="f22c5-1556">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="f22c5-1556">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="f22c5-1557">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="f22c5-1557">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="f22c5-1558">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="f22c5-1558">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="f22c5-1559">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="f22c5-1559">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="f22c5-1560">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="f22c5-1560">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="f22c5-1561">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1561">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="f22c5-1562">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f22c5-1562">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="f22c5-1563">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-1563">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="f22c5-1564">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="f22c5-1564">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="f22c5-1565">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-1565">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="f22c5-1566">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="f22c5-1566">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="f22c5-1567">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f22c5-1567">New cmdlets</span></span>
        - <span data-ttu-id="f22c5-1568">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f22c5-1568">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="f22c5-1569">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1569">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="f22c5-1570">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1570">Updated cmdlet:</span></span>
        - <span data-ttu-id="f22c5-1571">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f22c5-1571">New-VpnSite</span></span>
        - <span data-ttu-id="f22c5-1572">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="f22c5-1572">Update-VpnSite</span></span>
        - <span data-ttu-id="f22c5-1573">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1573">New-VpnConnection</span></span>
        - <span data-ttu-id="f22c5-1574">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1574">Update-VpnConnection</span></span>
* <span data-ttu-id="f22c5-1575">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="f22c5-1575">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1576">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1577">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1577">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="f22c5-1578">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="f22c5-1578">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1579">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1579">Az.Resources</span></span>
* <span data-ttu-id="f22c5-1580">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1580">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-1581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-1581">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-1582">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1582">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="f22c5-1583">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1583">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="f22c5-1584">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f22c5-1584">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f22c5-1585">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f22c5-1585">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f22c5-1586">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f22c5-1586">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f22c5-1587">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1587">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="f22c5-1588">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f22c5-1588">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f22c5-1589">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f22c5-1589">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f22c5-1590">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f22c5-1590">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f22c5-1591">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f22c5-1591">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f22c5-1592">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1592">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="f22c5-1593">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="f22c5-1593">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="f22c5-1594">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="f22c5-1594">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="f22c5-1595">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="f22c5-1595">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="f22c5-1596">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="f22c5-1596">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="f22c5-1597">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1597">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f22c5-1598">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f22c5-1598">Az.SignalR</span></span>
* <span data-ttu-id="f22c5-1599">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1599">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1600">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1601">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1601">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="f22c5-1602">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="f22c5-1602">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="f22c5-1603">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1603">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="f22c5-1604">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1604">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="f22c5-1605">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="f22c5-1605">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1606">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1606">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1607">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1607">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="f22c5-1608">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="f22c5-1608">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="f22c5-1609">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-1609">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="f22c5-1610">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-1610">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="f22c5-1611">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1611">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="f22c5-1612">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-1612">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="f22c5-1613">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-1613">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="f22c5-1614">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-1614">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f22c5-1615">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-1615">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f22c5-1616">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-1616">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="f22c5-1617">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-1617">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-1618">Az.Websites</span></span>
* <span data-ttu-id="f22c5-1619">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="f22c5-1619">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="f22c5-1620">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="f22c5-1620">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="f22c5-1621">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1621">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="f22c5-1622">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1622">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="f22c5-1623">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-1623">General</span></span>
* <span data-ttu-id="f22c5-1624">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1624">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1625">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1625">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1626">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1626">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="f22c5-1627">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f22c5-1627">Az.Aks</span></span>
* <span data-ttu-id="f22c5-1628">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1628">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="f22c5-1629">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="f22c5-1629">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-1630">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-1630">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-1631">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="f22c5-1631">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="f22c5-1632">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="f22c5-1632">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="f22c5-1633">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1633">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="f22c5-1634">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="f22c5-1634">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="f22c5-1635">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1635">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22c5-1636">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-1636">Az.Batch</span></span>
* <span data-ttu-id="f22c5-1637">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="f22c5-1637">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22c5-1638">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-1638">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-1639">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="f22c5-1639">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1640">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1640">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1641">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1641">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="f22c5-1642">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-1642">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="f22c5-1643">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="f22c5-1643">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="f22c5-1644">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1644">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="f22c5-1645">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="f22c5-1645">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="f22c5-1646">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f22c5-1646">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="f22c5-1647">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="f22c5-1647">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="f22c5-1648">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1648">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1649">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1649">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1650">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1650">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="f22c5-1651">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="f22c5-1651">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="f22c5-1652">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="f22c5-1652">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="f22c5-1653">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="f22c5-1653">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-1654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-1654">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-1655">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1655">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-1656">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1656">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-1657">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1657">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="f22c5-1658">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="f22c5-1658">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="f22c5-1659">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f22c5-1659">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="f22c5-1660">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="f22c5-1660">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="f22c5-1661">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f22c5-1661">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f22c5-1662">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="f22c5-1662">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-1663">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1663">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-1664">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-1664">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1665">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1665">Az.Network</span></span>
* <span data-ttu-id="f22c5-1666">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1666">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="f22c5-1667">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1667">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="f22c5-1668">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1668">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="f22c5-1669">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="f22c5-1669">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="f22c5-1670">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1670">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="f22c5-1671">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1671">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="f22c5-1672">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f22c5-1672">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-1673">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1673">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-1674">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1674">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="f22c5-1675">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1675">Added example</span></span>
    - <span data-ttu-id="f22c5-1676">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1676">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="f22c5-1677">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f22c5-1677">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="f22c5-1678">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="f22c5-1678">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1679">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1679">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1680">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1680">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1681">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1681">Az.Resources</span></span>
* <span data-ttu-id="f22c5-1682">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="f22c5-1682">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="f22c5-1683">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="f22c5-1683">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="f22c5-1684">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1684">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="f22c5-1685">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-1685">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22c5-1686">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22c5-1686">Az.ServiceBus</span></span>
* <span data-ttu-id="f22c5-1687">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-1687">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="f22c5-1688">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="f22c5-1688">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="f22c5-1689">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="f22c5-1689">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-1690">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-1690">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-1691">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1691">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="f22c5-1692">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1692">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="f22c5-1693">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="f22c5-1693">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="f22c5-1694">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1694">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="f22c5-1695">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="f22c5-1695">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="f22c5-1696">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="f22c5-1696">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1697">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1697">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1698">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1698">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1699">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1700">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="f22c5-1700">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="f22c5-1701">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="f22c5-1701">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="f22c5-1702">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-1702">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="f22c5-1703">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1703">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="f22c5-1704">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="f22c5-1704">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="f22c5-1705">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1705">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-1706">Az.Websites</span></span>
* <span data-ttu-id="f22c5-1707">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f22c5-1707">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="f22c5-1708">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1708">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1709">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1709">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1710">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f22c5-1710">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="f22c5-1711">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1711">Az.ApplicationInsights</span></span>
* <span data-ttu-id="f22c5-1712">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1712">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-1713">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-1713">Az.Automation</span></span>
* <span data-ttu-id="f22c5-1714">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1714">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-1715">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1715">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-1716">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1716">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1717">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1717">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1718">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1718">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f22c5-1719">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f22c5-1719">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f22c5-1720">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="f22c5-1720">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="f22c5-1721">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="f22c5-1721">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1722">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1722">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1723">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-1723">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="f22c5-1724">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="f22c5-1724">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-1725">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1725">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-1726">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f22c5-1726">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f22c5-1727">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="f22c5-1727">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-1728">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-1728">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-1729">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1729">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f22c5-1730">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-1730">Az.LogicApp</span></span>
* <span data-ttu-id="f22c5-1731">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="f22c5-1731">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="f22c5-1732">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="f22c5-1732">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="f22c5-1733">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1733">Az.ManagedServices</span></span>
* <span data-ttu-id="f22c5-1734">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1734">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1735">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1735">Az.Network</span></span>
* <span data-ttu-id="f22c5-1736">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1736">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="f22c5-1737">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f22c5-1737">New cmdlets</span></span>
        - <span data-ttu-id="f22c5-1738">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22c5-1738">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f22c5-1739">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1739">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f22c5-1740">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1740">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1741">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1741">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1742">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1742">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1743">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1743">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="f22c5-1744">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="f22c5-1744">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="f22c5-1745">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1745">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="f22c5-1746">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="f22c5-1746">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="f22c5-1747">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="f22c5-1747">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="f22c5-1748">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1748">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="f22c5-1749">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1749">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="f22c5-1750">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="f22c5-1750">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="f22c5-1751">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="f22c5-1751">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="f22c5-1752">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1752">Updated cmdlets</span></span>
        - <span data-ttu-id="f22c5-1753">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1753">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f22c5-1754">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1754">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="f22c5-1755">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1755">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="f22c5-1756">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1756">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="f22c5-1757">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-1757">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="f22c5-1758">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1758">Updated cmdlet:</span></span>
        - <span data-ttu-id="f22c5-1759">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1759">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f22c5-1760">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1760">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="f22c5-1761">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1761">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="f22c5-1762">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="f22c5-1762">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="f22c5-1763">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1763">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="f22c5-1764">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1764">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-1765">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1765">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-1766">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1766">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="f22c5-1767">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="f22c5-1767">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1768">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1768">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1769">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1769">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f22c5-1770">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1770">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="f22c5-1771">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1771">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="f22c5-1772">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1772">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="f22c5-1773">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1773">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="f22c5-1774">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1774">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f22c5-1775">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1775">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="f22c5-1776">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1776">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="f22c5-1777">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-1777">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="f22c5-1778">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1778">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1779">Az.Resources</span></span>
- <span data-ttu-id="f22c5-1780">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1780">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="f22c5-1781">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f22c5-1781">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22c5-1782">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22c5-1782">Az.ServiceBus</span></span>
* <span data-ttu-id="f22c5-1783">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="f22c5-1783">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="f22c5-1784">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="f22c5-1784">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1785">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1786">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f22c5-1786">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="f22c5-1787">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="f22c5-1787">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="f22c5-1788">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1788">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1789">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1790">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="f22c5-1790">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f22c5-1791">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f22c5-1791">Az.StorageSync</span></span>
* <span data-ttu-id="f22c5-1792">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1792">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="f22c5-1793">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="f22c5-1793">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-1794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-1794">Az.Websites</span></span>
* <span data-ttu-id="f22c5-1795">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-1795">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="f22c5-1796">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-1796">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="f22c5-1797">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="f22c5-1797">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="f22c5-1798">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1798">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1799">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1799">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1800">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="f22c5-1800">Add support for profile cmdlets</span></span>
* <span data-ttu-id="f22c5-1801">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1801">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="f22c5-1802">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="f22c5-1802">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="f22c5-1803">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1803">Az.Advisor</span></span>
* <span data-ttu-id="f22c5-1804">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1804">GA release of Az.Advisor</span></span>
* <span data-ttu-id="f22c5-1805">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1805">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-1806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-1806">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-1807">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="f22c5-1807">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="f22c5-1808">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f22c5-1808">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="f22c5-1809">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="f22c5-1809">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="f22c5-1810">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1810">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="f22c5-1811">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="f22c5-1811">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="f22c5-1812">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f22c5-1812">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="f22c5-1813">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="f22c5-1813">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-1814">Az.Automation</span></span>
* <span data-ttu-id="f22c5-1815">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1815">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1816">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1816">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1817">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1817">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-1818">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-1818">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-1819">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1819">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22c5-1820">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22c5-1820">Az.EventGrid</span></span>
* <span data-ttu-id="f22c5-1821">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1821">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-1822">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1822">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-1823">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1823">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1824">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1824">Az.Network</span></span>
* <span data-ttu-id="f22c5-1825">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="f22c5-1825">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="f22c5-1826">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1826">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-1827">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1827">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-1828">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="f22c5-1828">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="f22c5-1829">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="f22c5-1829">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-1830">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1830">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-1831">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f22c5-1831">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1832">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1833">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="f22c5-1833">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1834">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1834">Az.Resources</span></span>
    - <span data-ttu-id="f22c5-1835">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="f22c5-1835">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="f22c5-1836">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="f22c5-1836">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="f22c5-1837">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-1837">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="f22c5-1838">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1838">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22c5-1839">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22c5-1839">Az.ServiceBus</span></span>
* <span data-ttu-id="f22c5-1840">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="f22c5-1840">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1841">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1842">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="f22c5-1842">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="f22c5-1843">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1843">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="f22c5-1844">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f22c5-1844">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f22c5-1845">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f22c5-1845">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f22c5-1846">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="f22c5-1846">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="f22c5-1847">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f22c5-1847">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f22c5-1848">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f22c5-1848">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="f22c5-1849">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f22c5-1849">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="f22c5-1850">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="f22c5-1850">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1851">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1851">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1852">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1852">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="f22c5-1853">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f22c5-1853">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="f22c5-1854">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1854">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="f22c5-1855">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="f22c5-1855">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="f22c5-1856">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-1856">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="f22c5-1857">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1857">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="f22c5-1858">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1858">Set-AzStorageAccount</span></span>
* <span data-ttu-id="f22c5-1859">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1859">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="f22c5-1860">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f22c5-1860">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="f22c5-1861">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="f22c5-1861">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="f22c5-1862">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="f22c5-1862">Az.StorageSync</span></span>
* <span data-ttu-id="f22c5-1863">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1863">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="f22c5-1864">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1864">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-1865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-1865">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-1866">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="f22c5-1866">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="f22c5-1867">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="f22c5-1867">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="f22c5-1868">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="f22c5-1868">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="f22c5-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f22c5-1869">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="f22c5-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="f22c5-1870">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1871">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1871">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1872">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1872">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="f22c5-1873">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1873">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="f22c5-1874">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f22c5-1874">Az.Dns</span></span>
* <span data-ttu-id="f22c5-1875">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1875">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22c5-1876">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22c5-1876">Az.EventGrid</span></span>
* <span data-ttu-id="f22c5-1877">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1877">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="f22c5-1878">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1878">New cmdlets:</span></span>
    - <span data-ttu-id="f22c5-1879">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f22c5-1879">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f22c5-1880">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1880">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f22c5-1881">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f22c5-1881">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f22c5-1882">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1882">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="f22c5-1883">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="f22c5-1883">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="f22c5-1884">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1884">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f22c5-1885">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f22c5-1885">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f22c5-1886">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1886">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="f22c5-1887">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f22c5-1887">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="f22c5-1888">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1888">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="f22c5-1889">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1889">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f22c5-1890">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1890">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="f22c5-1891">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="f22c5-1891">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="f22c5-1892">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="f22c5-1892">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="f22c5-1893">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1893">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="f22c5-1894">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1894">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="f22c5-1895">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1895">Updated cmdlets:</span></span>
    - <span data-ttu-id="f22c5-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1896">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="f22c5-1897">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1897">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f22c5-1898">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1898">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="f22c5-1899">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="f22c5-1899">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="f22c5-1900">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1900">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="f22c5-1901">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="f22c5-1901">Event subscription expiration date,</span></span>
            - <span data-ttu-id="f22c5-1902">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1902">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="f22c5-1903">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1903">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="f22c5-1904">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="f22c5-1904">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="f22c5-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1905">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="f22c5-1906">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1906">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="f22c5-1907">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="f22c5-1907">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="f22c5-1908">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1908">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="f22c5-1909">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1909">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-1910">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-1910">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-1911">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-1911">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="f22c5-1912">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="f22c5-1912">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="f22c5-1913">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-1913">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="f22c5-1914">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="f22c5-1914">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1915">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1915">Az.Network</span></span>
* <span data-ttu-id="f22c5-1916">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="f22c5-1916">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="f22c5-1917">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f22c5-1917">New cmdlets</span></span>
        - <span data-ttu-id="f22c5-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="f22c5-1918">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="f22c5-1919">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f22c5-1919">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="f22c5-1920">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f22c5-1920">New cmdlets</span></span>
        - <span data-ttu-id="f22c5-1921">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="f22c5-1921">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="f22c5-1922">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1922">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="f22c5-1923">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f22c5-1923">New cmdlets</span></span>
        - <span data-ttu-id="f22c5-1924">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1924">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f22c5-1925">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1925">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f22c5-1926">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="f22c5-1926">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="f22c5-1927">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-1927">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="f22c5-1928">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1928">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="f22c5-1929">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22c5-1929">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="f22c5-1930">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f22c5-1930">New cmdlets</span></span>
        - <span data-ttu-id="f22c5-1931">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22c5-1931">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f22c5-1932">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22c5-1932">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f22c5-1933">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f22c5-1933">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="f22c5-1934">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1934">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="f22c5-1935">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="f22c5-1935">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="f22c5-1936">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1936">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="f22c5-1937">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1937">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="f22c5-1938">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1938">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="f22c5-1939">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1939">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="f22c5-1940">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f22c5-1940">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="f22c5-1941">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-1941">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="f22c5-1942">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1942">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="f22c5-1943">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-1943">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="f22c5-1944">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="f22c5-1944">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="f22c5-1945">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="f22c5-1945">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="f22c5-1946">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="f22c5-1946">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="f22c5-1947">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="f22c5-1947">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="f22c5-1948">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-1948">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="f22c5-1949">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="f22c5-1949">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="f22c5-1950">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="f22c5-1950">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="f22c5-1951">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="f22c5-1951">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="f22c5-1952">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="f22c5-1952">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="f22c5-1953">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f22c5-1953">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="f22c5-1954">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1954">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="f22c5-1955">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1955">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f22c5-1956">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1956">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="f22c5-1957">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1957">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-1958">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1958">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-1959">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="f22c5-1959">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-1960">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-1960">Az.Resources</span></span>
* <span data-ttu-id="f22c5-1961">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="f22c5-1961">Support for additional Template Export options</span></span>
    - <span data-ttu-id="f22c5-1962">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1962">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f22c5-1963">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-1963">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="f22c5-1964">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="f22c5-1964">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-1965">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-1965">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-1966">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="f22c5-1966">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-1967">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-1967">Az.Sql</span></span>
* <span data-ttu-id="f22c5-1968">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="f22c5-1968">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="f22c5-1969">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="f22c5-1969">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="f22c5-1970">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="f22c5-1970">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="f22c5-1971">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f22c5-1971">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f22c5-1972">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f22c5-1972">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f22c5-1973">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f22c5-1973">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="f22c5-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f22c5-1974">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="f22c5-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="f22c5-1975">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-1976">Az.Storage</span></span>
* <span data-ttu-id="f22c5-1977">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-1977">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="f22c5-1978">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-1978">New-AzStorageAccount</span></span>
* <span data-ttu-id="f22c5-1979">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="f22c5-1979">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="f22c5-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-1980">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-1981">Az.Websites</span></span>
* <span data-ttu-id="f22c5-1982">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="f22c5-1982">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="f22c5-1983">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="f22c5-1983">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="f22c5-1984">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-1984">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="f22c5-1985">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-1985">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-1986">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1986">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-1987">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-1987">Az.Compute</span></span>
* <span data-ttu-id="f22c5-1988">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="f22c5-1988">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="f22c5-1989">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f22c5-1989">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-1990">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-1990">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-1991">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="f22c5-1991">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="f22c5-1992">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22c5-1992">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-1993">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-1993">Az.Network</span></span>
* <span data-ttu-id="f22c5-1994">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="f22c5-1994">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="f22c5-1995">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="f22c5-1995">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-1996">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-1996">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-1997">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="f22c5-1997">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-1998">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-1998">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-1999">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="f22c5-1999">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22c5-2000">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22c5-2000">Az.ServiceBus</span></span>
* <span data-ttu-id="f22c5-2001">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22c5-2001">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-2002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2002">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-2003">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2003">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="f22c5-2004">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2004">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2005">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2005">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2006">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2006">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="f22c5-2007">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2007">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="f22c5-2008">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="f22c5-2008">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="f22c5-2009">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2009">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2010">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2010">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2011">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2011">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="f22c5-2012">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2012">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="f22c5-2013">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-2013">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-2014">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2014">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="f22c5-2015">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2015">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="f22c5-2016">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2016">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="f22c5-2017">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2017">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="f22c5-2018">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2018">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="f22c5-2019">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="f22c5-2019">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="f22c5-2020">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2020">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="f22c5-2021">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2021">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="f22c5-2022">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-2022">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="f22c5-2023">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="f22c5-2023">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="f22c5-2024">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2024">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="f22c5-2025">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="f22c5-2025">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="f22c5-2026">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="f22c5-2026">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="f22c5-2027">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2027">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="f22c5-2028">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2028">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="f22c5-2029">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2029">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="f22c5-2030">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2030">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="f22c5-2031">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="f22c5-2031">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="f22c5-2032">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2032">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="f22c5-2033">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="f22c5-2033">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="f22c5-2034">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="f22c5-2034">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="f22c5-2035">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2035">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="f22c5-2036">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2036">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="f22c5-2037">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-2037">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="f22c5-2038">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2038">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="f22c5-2039">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2039">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="f22c5-2040">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2040">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="f22c5-2041">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2041">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="f22c5-2042">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2042">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="f22c5-2043">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="f22c5-2043">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="f22c5-2044">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2044">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="f22c5-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="f22c5-2045">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="f22c5-2046">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2046">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="f22c5-2047">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f22c5-2047">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f22c5-2048">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2048">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="f22c5-2049">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="f22c5-2049">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="f22c5-2050">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2050">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="f22c5-2051">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2051">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="f22c5-2052">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2052">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="f22c5-2053">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f22c5-2053">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f22c5-2054">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2054">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f22c5-2055">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2055">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f22c5-2056">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2056">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="f22c5-2057">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2057">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f22c5-2058">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="f22c5-2058">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="f22c5-2059">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2059">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="f22c5-2060">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2060">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="f22c5-2061">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2061">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="f22c5-2062">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="f22c5-2062">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="f22c5-2063">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2063">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="f22c5-2064">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2064">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="f22c5-2065">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2065">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="f22c5-2066">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2066">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="f22c5-2067">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="f22c5-2067">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="f22c5-2068">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2068">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="f22c5-2069">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2069">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="f22c5-2070">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f22c5-2070">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f22c5-2071">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2071">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f22c5-2072">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2072">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f22c5-2073">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2073">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f22c5-2074">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="f22c5-2074">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="f22c5-2075">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2075">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="f22c5-2076">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2076">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="f22c5-2077">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2077">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="f22c5-2078">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="f22c5-2078">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="f22c5-2079">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2079">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="f22c5-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="f22c5-2080">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="f22c5-2081">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2081">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="f22c5-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="f22c5-2082">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="f22c5-2083">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2083">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="f22c5-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="f22c5-2084">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="f22c5-2085">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2085">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="f22c5-2086">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2086">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="f22c5-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2087">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="f22c5-2088">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2088">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="f22c5-2089">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2089">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="f22c5-2090">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2090">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-2091">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2091">Az.Automation</span></span>
* <span data-ttu-id="f22c5-2092">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2092">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="f22c5-2093">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="f22c5-2093">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="f22c5-2094">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="f22c5-2094">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="f22c5-2095">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2095">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="f22c5-2096">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="f22c5-2096">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="f22c5-2097">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2097">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="f22c5-2098">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2098">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2099">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2099">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2100">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2100">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="f22c5-2101">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2101">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2102">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2102">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-2103">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2103">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-2104">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-2104">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-2105">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-2105">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2106">Az.Network</span></span>
* <span data-ttu-id="f22c5-2107">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2107">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="f22c5-2108">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f22c5-2108">Updated cmdlet:</span></span>
        - <span data-ttu-id="f22c5-2109">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-2109">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="f22c5-2110">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f22c5-2110">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2111">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2111">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2112">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="f22c5-2112">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2113">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2113">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2114">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="f22c5-2114">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="f22c5-2115">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2115">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2116">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2116">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2117">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="f22c5-2117">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-2118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2118">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-2119">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2119">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="f22c5-2120">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2120">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2121">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2121">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2122">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2122">Proximity placement group feature.</span></span>
    - <span data-ttu-id="f22c5-2123">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-2123">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="f22c5-2124">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-2124">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="f22c5-2125">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2125">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="f22c5-2126">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2126">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="f22c5-2127">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-2127">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="f22c5-2128">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="f22c5-2128">Breaking changes</span></span>
    - <span data-ttu-id="f22c5-2129">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2129">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="f22c5-2130">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2130">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="f22c5-2131">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="f22c5-2131">Az.DeploymentManager</span></span>
* <span data-ttu-id="f22c5-2132">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2132">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="f22c5-2133">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="f22c5-2133">Az.Dns</span></span>
* <span data-ttu-id="f22c5-2134">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="f22c5-2134">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="f22c5-2135">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2135">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="f22c5-2136">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2136">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-2137">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-2137">Az.FrontDoor</span></span>
* <span data-ttu-id="f22c5-2138">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2138">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="f22c5-2139">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2139">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-2140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-2140">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-2141">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="f22c5-2141">Removed two cmdlets:</span></span>
    - <span data-ttu-id="f22c5-2142">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f22c5-2142">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="f22c5-2143">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f22c5-2143">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f22c5-2144">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f22c5-2144">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="f22c5-2145">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="f22c5-2145">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="f22c5-2146">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2146">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="f22c5-2147">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2147">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-2148">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-2148">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-2149">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="f22c5-2149">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="f22c5-2150">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="f22c5-2150">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="f22c5-2151">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-2151">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="f22c5-2152">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f22c5-2152">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="f22c5-2153">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2153">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="f22c5-2154">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="f22c5-2154">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="f22c5-2155">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f22c5-2155">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="f22c5-2156">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2156">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22c5-2157">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2157">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22c5-2158">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2158">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22c5-2159">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2159">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22c5-2160">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2160">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="f22c5-2161">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="f22c5-2161">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="f22c5-2162">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="f22c5-2162">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2163">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2163">Az.Network</span></span>
* <span data-ttu-id="f22c5-2164">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="f22c5-2164">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="f22c5-2165">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="f22c5-2165">New cmdlets</span></span>
        - <span data-ttu-id="f22c5-2166">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22c5-2166">New-AzNatGateway</span></span>
        - <span data-ttu-id="f22c5-2167">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22c5-2167">Get-AzNatGateway</span></span>
        - <span data-ttu-id="f22c5-2168">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22c5-2168">Set-AzNatGateway</span></span>
        - <span data-ttu-id="f22c5-2169">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f22c5-2169">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="f22c5-2170">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2170">Updated cmdlets</span></span>
        - <span data-ttu-id="f22c5-2171">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f22c5-2171">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="f22c5-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="f22c5-2172">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="f22c5-2173">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2173">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="f22c5-2174">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2174">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="f22c5-2175">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2175">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-2176">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-2176">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-2177">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2177">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="f22c5-2178">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2178">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="f22c5-2179">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2179">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2180">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2180">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-2181">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2181">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="f22c5-2182">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2182">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="f22c5-2183">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2183">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="f22c5-2184">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2184">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="f22c5-2185">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2185">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="f22c5-2186">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2186">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="f22c5-2187">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f22c5-2187">Az.Relay</span></span>
* <span data-ttu-id="f22c5-2188">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="f22c5-2188">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22c5-2189">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22c5-2189">Az.ServiceBus</span></span>
* <span data-ttu-id="f22c5-2190">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="f22c5-2190">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-2191">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2191">Az.Storage</span></span>
* <span data-ttu-id="f22c5-2192">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="f22c5-2192">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="f22c5-2193">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2193">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="f22c5-2194">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2194">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="f22c5-2195">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2195">New-AzStorageAccount</span></span>
* <span data-ttu-id="f22c5-2196">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2196">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="f22c5-2197">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2197">New-AzStorageAccount</span></span>
    - <span data-ttu-id="f22c5-2198">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2198">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="f22c5-2199">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2199">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2200">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2200">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2201">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-2201">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="f22c5-2202">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2202">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="f22c5-2203">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2203">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22c5-2204">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f22c5-2204">Highlights since the last major release</span></span>
* <span data-ttu-id="f22c5-2205">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f22c5-2205">General availability of `Az` module</span></span>
* <span data-ttu-id="f22c5-2206">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f22c5-2206">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f22c5-2207">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f22c5-2207">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f22c5-2208">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2208">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f22c5-2209">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f22c5-2209">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22c5-2210">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2210">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f22c5-2211">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="f22c5-2211">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2212">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2212">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2213">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="f22c5-2213">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="f22c5-2214">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-2214">Az.Batch</span></span>
* <span data-ttu-id="f22c5-2215">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2215">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22c5-2216">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-2216">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-2217">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2217">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-2218">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2218">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-2219">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2219">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2220">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2220">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2221">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2221">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="f22c5-2222">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2222">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22c5-2223">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f22c5-2223">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-2224">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-2224">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-2225">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2225">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2226">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2226">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-2227">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2227">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22c5-2228">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22c5-2228">Az.EventGrid</span></span>
* <span data-ttu-id="f22c5-2229">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2229">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-2230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-2230">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-2231">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="f22c5-2231">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="f22c5-2232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="f22c5-2232">Az.HDInsight</span></span>
* <span data-ttu-id="f22c5-2233">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-2234">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-2234">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-2235">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2235">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-2236">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-2236">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-2237">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2237">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22c5-2238">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f22c5-2238">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="f22c5-2239">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f22c5-2239">Az.MachineLearning</span></span>
* <span data-ttu-id="f22c5-2240">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="f22c5-2241">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f22c5-2241">Az.Media</span></span>
* <span data-ttu-id="f22c5-2242">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-2243">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-2243">Az.Monitor</span></span>
  * <span data-ttu-id="f22c5-2244">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="f22c5-2244">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="f22c5-2245">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="f22c5-2245">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="f22c5-2246">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="f22c5-2246">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="f22c5-2247">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f22c5-2247">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f22c5-2248">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f22c5-2248">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="f22c5-2249">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="f22c5-2249">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="f22c5-2250">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="f22c5-2250">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2251">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2251">Az.Network</span></span>
* <span data-ttu-id="f22c5-2252">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22c5-2253">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f22c5-2253">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="f22c5-2254">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="f22c5-2254">Az.NotificationHubs</span></span>
* <span data-ttu-id="f22c5-2255">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2255">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-2256">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-2256">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-2257">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2257">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="f22c5-2258">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="f22c5-2258">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="f22c5-2259">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2259">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-2261">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2261">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22c5-2262">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2262">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="f22c5-2263">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="f22c5-2263">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="f22c5-2264">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="f22c5-2264">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f22c5-2265">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f22c5-2265">Az.RedisCache</span></span>
* <span data-ttu-id="f22c5-2266">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2266">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2267">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2267">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2268">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f22c5-2268">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2269">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2270">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="f22c5-2270">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="f22c5-2271">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2271">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22c5-2272">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2272">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="f22c5-2273">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2273">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="f22c5-2274">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2274">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="f22c5-2275">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2275">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="f22c5-2276">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="f22c5-2276">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2277">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2277">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2278">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="f22c5-2278">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="f22c5-2279">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2279">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="f22c5-2280">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2280">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="f22c5-2281">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2281">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="f22c5-2282">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2282">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22c5-2283">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f22c5-2283">Highlights since the last major release</span></span>
* <span data-ttu-id="f22c5-2284">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f22c5-2284">General availability of `Az` module</span></span>
* <span data-ttu-id="f22c5-2285">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f22c5-2285">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f22c5-2286">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f22c5-2286">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f22c5-2287">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2287">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f22c5-2288">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f22c5-2288">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22c5-2289">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2289">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f22c5-2290">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="f22c5-2290">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2291">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2291">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2292">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f22c5-2292">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22c5-2293">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2293">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22c5-2294">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="f22c5-2294">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="f22c5-2295">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="f22c5-2295">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-2296">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2296">Az.Automation</span></span>
* <span data-ttu-id="f22c5-2297">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2297">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="f22c5-2298">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2298">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="f22c5-2299">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2299">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2300">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2300">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2301">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-2301">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="f22c5-2302">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2302">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="f22c5-2303">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-2303">Az.ContainerInstance</span></span>
* <span data-ttu-id="f22c5-2304">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="f22c5-2304">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-2305">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-2305">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-2306">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="f22c5-2306">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="f22c5-2307">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2307">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2308">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2308">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2309">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="f22c5-2309">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="f22c5-2310">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2310">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="f22c5-2311">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="f22c5-2311">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="f22c5-2312">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f22c5-2312">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="f22c5-2313">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="f22c5-2313">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="f22c5-2314">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="f22c5-2314">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2315">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2316">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2316">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-2317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2317">Az.Storage</span></span>
* <span data-ttu-id="f22c5-2318">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2318">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="f22c5-2319">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f22c5-2319">New-AzStorageContext</span></span>
* <span data-ttu-id="f22c5-2320">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-2320">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="f22c5-2321">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f22c5-2321">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f22c5-2322">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f22c5-2322">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="f22c5-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2323">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="f22c5-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2324">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="f22c5-2325">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2325">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="f22c5-2326">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-2326">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f22c5-2327">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-2327">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="f22c5-2328">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-2328">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="f22c5-2329">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f22c5-2329">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="f22c5-2330">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2330">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="f22c5-2331">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="f22c5-2331">Highlights since the last major release</span></span>
* <span data-ttu-id="f22c5-2332">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="f22c5-2332">General availability of `Az` module</span></span>
* <span data-ttu-id="f22c5-2333">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="f22c5-2333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="f22c5-2334">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="f22c5-2334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="f22c5-2335">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="f22c5-2336">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f22c5-2336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22c5-2337">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="f22c5-2338">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="f22c5-2338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-2339">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2339">Az.Automation</span></span>
* <span data-ttu-id="f22c5-2340">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="f22c5-2340">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="f22c5-2341">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="f22c5-2341">Dynamic grouping</span></span>
    * <span data-ttu-id="f22c5-2342">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="f22c5-2342">Pre-Post script</span></span>
    * <span data-ttu-id="f22c5-2343">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="f22c5-2343">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2344">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2345">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="f22c5-2345">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="f22c5-2346">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2346">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-2347">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-2347">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-2348">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-2348">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2349">Az.Network</span></span>
* <span data-ttu-id="f22c5-2350">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2350">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="f22c5-2351">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2351">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2352">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-2353">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2353">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="f22c5-2354">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="f22c5-2354">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2355">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2356">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f22c5-2356">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="f22c5-2357">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="f22c5-2357">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2358">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2359">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2359">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-2360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2360">Az.Storage</span></span>
* <span data-ttu-id="f22c5-2361">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-2361">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="f22c5-2362">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2362">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f22c5-2363">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2363">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f22c5-2364">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2364">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="f22c5-2365">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="f22c5-2365">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="f22c5-2366">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="f22c5-2366">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="f22c5-2367">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2367">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2368">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2368">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2369">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="f22c5-2369">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="f22c5-2370">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2370">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2371">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2371">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2372">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="f22c5-2372">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="f22c5-2373">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2373">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-2374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2374">Az.Automation</span></span>
* <span data-ttu-id="f22c5-2375">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2375">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="f22c5-2376">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2376">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="f22c5-2377">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="f22c5-2377">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22c5-2378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-2378">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-2379">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2379">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2380">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2381">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="f22c5-2381">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-2382">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-2382">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-2383">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="f22c5-2383">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f22c5-2384">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-2384">Az.LogicApp</span></span>
* <span data-ttu-id="f22c5-2385">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2385">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2386">Az.Network</span></span>
* <span data-ttu-id="f22c5-2387">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2387">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2388">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2388">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-2389">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2389">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="f22c5-2390">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="f22c5-2390">SDK Update</span></span>
* <span data-ttu-id="f22c5-2391">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f22c5-2391">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="f22c5-2392">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f22c5-2392">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2393">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2393">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2394">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="f22c5-2394">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="f22c5-2395">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="f22c5-2395">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="f22c5-2396">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f22c5-2396">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="f22c5-2397">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="f22c5-2397">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="f22c5-2398">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="f22c5-2398">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="f22c5-2399">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="f22c5-2399">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2400">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2400">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2401">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2401">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="f22c5-2402">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2402">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-2403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2403">Az.Storage</span></span>
* <span data-ttu-id="f22c5-2404">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2404">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="f22c5-2405">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2405">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="f22c5-2406">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2406">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22c5-2407">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2407">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-2408">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2408">Az.Automation</span></span>
* <span data-ttu-id="f22c5-2409">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2409">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="f22c5-2410">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2410">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="f22c5-2411">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2411">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-2412">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2412">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-2413">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2413">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2414">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2414">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2415">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="f22c5-2415">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="f22c5-2416">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="f22c5-2416">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="f22c5-2417">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2417">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="f22c5-2418">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2418">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2419">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-2420">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2420">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="f22c5-2421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-2421">Az.EventHub</span></span>
* <span data-ttu-id="f22c5-2422">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-2422">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-2423">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-2423">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-2424">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f22c5-2424">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f22c5-2425">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-2425">Az.LogicApp</span></span>
* <span data-ttu-id="f22c5-2426">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="f22c5-2426">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="f22c5-2427">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="f22c5-2427">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="f22c5-2428">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="f22c5-2428">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="f22c5-2429">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f22c5-2429">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f22c5-2430">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f22c5-2430">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f22c5-2431">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f22c5-2431">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="f22c5-2432">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f22c5-2432">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="f22c5-2433">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="f22c5-2433">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="f22c5-2434">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2434">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f22c5-2435">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2435">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f22c5-2436">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2436">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="f22c5-2437">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2437">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="f22c5-2438">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-2438">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="f22c5-2439">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-2439">Az.Monitor</span></span>
* <span data-ttu-id="f22c5-2440">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2440">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2441">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2441">Az.Network</span></span>
* <span data-ttu-id="f22c5-2442">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f22c5-2442">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-2443">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-2443">Az.OperationalInsights</span></span>
* <span data-ttu-id="f22c5-2444">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2444">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="f22c5-2445">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2445">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="f22c5-2446">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2446">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2447">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2448">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f22c5-2448">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f22c5-2449">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f22c5-2449">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="f22c5-2450">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="f22c5-2450">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="f22c5-2451">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="f22c5-2451">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2452">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2452">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2453">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="f22c5-2453">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="f22c5-2454">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="f22c5-2454">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2455">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2455">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2456">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="f22c5-2456">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="f22c5-2457">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2457">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2458">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2458">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2459">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f22c5-2459">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22c5-2460">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2460">Az.AnalysisServices</span></span>
<span data-ttu-id="f22c5-2461">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2461">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2462">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2463">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="f22c5-2463">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="f22c5-2464">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f22c5-2464">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="f22c5-2465">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2465">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2466">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2466">Az.RecoveryServices</span></span>
<span data-ttu-id="f22c5-2467">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2467">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2468">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2468">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2469">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2469">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="f22c5-2470">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="f22c5-2470">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="f22c5-2471">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="f22c5-2471">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="f22c5-2472">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="f22c5-2472">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2473">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2473">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2474">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2474">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="f22c5-2475">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="f22c5-2475">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="f22c5-2476">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="f22c5-2476">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="f22c5-2477">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2477">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2478">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2479">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="f22c5-2479">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="f22c5-2480">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2480">Az.AnalysisServices</span></span>
* <span data-ttu-id="f22c5-2481">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-2481">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2482">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2482">Az.RecoveryServices</span></span>
* <span data-ttu-id="f22c5-2483">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-2483">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="f22c5-2484">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2484">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2485">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2485">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2486">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="f22c5-2486">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="f22c5-2487">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2487">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22c5-2488">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="f22c5-2488">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="f22c5-2489">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="f22c5-2489">Az.Aks</span></span>
* <span data-ttu-id="f22c5-2490">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2490">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="f22c5-2491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2491">Az.Automation</span></span>
* <span data-ttu-id="f22c5-2492">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="f22c5-2492">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="f22c5-2493">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2493">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="f22c5-2494">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="f22c5-2494">Az.Cdn</span></span>
* <span data-ttu-id="f22c5-2495">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2495">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2496">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2497">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2497">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="f22c5-2498">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f22c5-2498">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="f22c5-2499">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f22c5-2499">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="f22c5-2500">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f22c5-2500">Az.ContainerRegistry</span></span>
* <span data-ttu-id="f22c5-2501">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2501">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="f22c5-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f22c5-2502">Az.DataFactory</span></span>
* <span data-ttu-id="f22c5-2503">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="f22c5-2503">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2504">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-2505">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="f22c5-2505">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="f22c5-2506">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="f22c5-2506">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="f22c5-2507">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2507">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-2508">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-2508">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-2509">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2509">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="f22c5-2510">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-2510">Az.KeyVault</span></span>
* <span data-ttu-id="f22c5-2511">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2511">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2512">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2512">Az.Network</span></span>
* <span data-ttu-id="f22c5-2513">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2513">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2514">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2514">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2515">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2515">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="f22c5-2516">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2516">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="f22c5-2517">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="f22c5-2517">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="f22c5-2518">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="f22c5-2518">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="f22c5-2519">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="f22c5-2519">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="f22c5-2520">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2520">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="f22c5-2521">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="f22c5-2521">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-2522">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2522">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-2523">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="f22c5-2523">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="f22c5-2524">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2524">Fix some error messages.</span></span>
* <span data-ttu-id="f22c5-2525">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2525">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="f22c5-2526">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2526">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f22c5-2527">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f22c5-2527">Az.SignalR</span></span>
* <span data-ttu-id="f22c5-2528">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2528">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2529">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2530">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2530">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22c5-2531">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="f22c5-2531">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="f22c5-2532">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="f22c5-2532">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="f22c5-2533">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2533">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-2534">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2534">Az.Storage</span></span>
* <span data-ttu-id="f22c5-2535">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22c5-2536">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2536">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="f22c5-2537">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="f22c5-2537">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="f22c5-2538">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f22c5-2538">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="f22c5-2539">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f22c5-2539">Az.TrafficManager</span></span>
* <span data-ttu-id="f22c5-2540">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2540">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2541">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2541">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2542">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="f22c5-2542">Update incorrect online help URLs</span></span>
* <span data-ttu-id="f22c5-2543">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2543">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="f22c5-2544">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2544">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="f22c5-2545">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="f22c5-2545">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="f22c5-2546">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2546">Az.Accounts</span></span>
* <span data-ttu-id="f22c5-2547">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f22c5-2547">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2548">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2548">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2549">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2549">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="f22c5-2550">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="f22c5-2550">Updated the description of ID in help files</span></span>
* <span data-ttu-id="f22c5-2551">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2551">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2552">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-2553">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2553">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="f22c5-2554">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="f22c5-2554">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="f22c5-2555">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f22c5-2555">Az.EventGrid</span></span>
* <span data-ttu-id="f22c5-2556">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2556">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="f22c5-2557">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="f22c5-2557">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="f22c5-2558">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="f22c5-2558">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f22c5-2559">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="f22c5-2559">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f22c5-2560">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2560">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f22c5-2561">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2561">Dead letter endpoint.</span></span>
    - <span data-ttu-id="f22c5-2562">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="f22c5-2562">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="f22c5-2563">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="f22c5-2563">Event Time-To-Live,</span></span>
        - <span data-ttu-id="f22c5-2564">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2564">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="f22c5-2565">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="f22c5-2565">Dead letter endpoint.</span></span>
* <span data-ttu-id="f22c5-2566">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2566">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="f22c5-2567">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2567">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="f22c5-2568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-2568">Az.IotHub</span></span>
* <span data-ttu-id="f22c5-2569">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="f22c5-2569">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="f22c5-2570">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="f22c5-2570">Az.LogicApp</span></span>
* <span data-ttu-id="f22c5-2571">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="f22c5-2571">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2572">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2572">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2573">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2573">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="f22c5-2574">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="f22c5-2574">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="f22c5-2575">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f22c5-2575">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f22c5-2576">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f22c5-2576">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="f22c5-2577">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2577">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="f22c5-2578">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="f22c5-2578">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="f22c5-2579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="f22c5-2579">Az.SignalR</span></span>
* <span data-ttu-id="f22c5-2580">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2580">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2581">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2582">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2582">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="f22c5-2583">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2583">Az.Storage</span></span>
* <span data-ttu-id="f22c5-2584">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="f22c5-2584">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="f22c5-2585">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f22c5-2585">New-AzStorageContext</span></span>
* <span data-ttu-id="f22c5-2586">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2586">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="f22c5-2587">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f22c5-2587">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2588">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2588">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2589">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="f22c5-2589">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="f22c5-2590">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2590">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="f22c5-2591">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f22c5-2591">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="f22c5-2592">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-2592">General</span></span>

- <span data-ttu-id="f22c5-2593">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="f22c5-2593">General Availability of Az Module</span></span>
- <span data-ttu-id="f22c5-2594">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2594">Online help for each module</span></span>
- <span data-ttu-id="f22c5-2595">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="f22c5-2595">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="f22c5-2596">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="f22c5-2596">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="f22c5-2597">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2597">Az.Accounts</span></span>
- <span data-ttu-id="f22c5-2598">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2598">Changed from Az.Profile</span></span>
- <span data-ttu-id="f22c5-2599">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="f22c5-2599">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f22c5-2600">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-2600">Az.ApiManagement</span></span>
- <span data-ttu-id="f22c5-2601">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="f22c5-2601">Fixes for #7002</span></span>
- <span data-ttu-id="f22c5-2602">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2602">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="f22c5-2603">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="f22c5-2603">Az.Batch</span></span>
- <span data-ttu-id="f22c5-2604">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2604">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="f22c5-2605">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2605">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="f22c5-2606">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2606">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="f22c5-2607">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f22c5-2607">Az.Billing</span></span>
- <span data-ttu-id="f22c5-2608">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2608">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="f22c5-2609">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2609">Az.CognitivServices</span></span>
- <span data-ttu-id="f22c5-2610">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2610">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="f22c5-2611">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f22c5-2611">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f22c5-2612">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-2612">Az.ContainerInstance</span></span>
- <span data-ttu-id="f22c5-2613">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="f22c5-2613">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="f22c5-2614">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="f22c5-2614">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="f22c5-2615">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2615">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2616">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2616">Az.DataLakeStore</span></span>
- <span data-ttu-id="f22c5-2617">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2617">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="f22c5-2618">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f22c5-2618">Az.Monitor</span></span>
- <span data-ttu-id="f22c5-2619">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2619">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="f22c5-2620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f22c5-2620">Az.KeyVault</span></span>
- <span data-ttu-id="f22c5-2621">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="f22c5-2621">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="f22c5-2622">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f22c5-2622">Az.MachineLearning</span></span>
- <span data-ttu-id="f22c5-2623">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2623">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="f22c5-2624">Az.Media</span><span class="sxs-lookup"><span data-stu-id="f22c5-2624">Az.Media</span></span>
- <span data-ttu-id="f22c5-2625">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f22c5-2625">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f22c5-2626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2626">Az.Network</span></span>
<span data-ttu-id="f22c5-2627">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2627">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="f22c5-2628">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="f22c5-2628">New cmdlets added:</span></span>
        - <span data-ttu-id="f22c5-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2629">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22c5-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2630">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22c5-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2631">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22c5-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2632">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22c5-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2633">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="f22c5-2634">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2634">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="f22c5-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2635">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="f22c5-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f22c5-2636">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="f22c5-2637">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2637">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="f22c5-2638">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f22c5-2638">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="f22c5-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2639">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f22c5-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f22c5-2640">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="f22c5-2641">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-2641">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="f22c5-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-2642">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="f22c5-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2643">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="f22c5-2644">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f22c5-2644">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="f22c5-2645">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f22c5-2645">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f22c5-2646">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f22c5-2646">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="f22c5-2647">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f22c5-2647">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="f22c5-2648">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f22c5-2648">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="f22c5-2649">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="f22c5-2650">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-2650">Az.OperationalInsights</span></span>
- <span data-ttu-id="f22c5-2651">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="f22c5-2652">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2652">Az.Profile</span></span>
- <span data-ttu-id="f22c5-2653">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f22c5-2653">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2654">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2654">Az.RecoveryServices</span></span>
- <span data-ttu-id="f22c5-2655">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2655">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="f22c5-2656">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2656">Az.Resources</span></span>
- <span data-ttu-id="f22c5-2657">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2657">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f22c5-2658">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2658">Az.ServiceFabric</span></span>
- <span data-ttu-id="f22c5-2659">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="f22c5-2659">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="f22c5-2660">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2660">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="f22c5-2661">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f22c5-2661">Az.SIgnalR</span></span>
- <span data-ttu-id="f22c5-2662">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="f22c5-2662">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="f22c5-2663">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2663">Az.Sql</span></span>
- <span data-ttu-id="f22c5-2664">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="f22c5-2664">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="f22c5-2665">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="f22c5-2665">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="f22c5-2666">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2666">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="f22c5-2667">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2667">Az.Storage</span></span>
- <span data-ttu-id="f22c5-2668">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2668">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f22c5-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2669">Az.Websites</span></span>
- <span data-ttu-id="f22c5-2670">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="f22c5-2670">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="f22c5-2671">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f22c5-2671">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="f22c5-2672">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-2672">General</span></span>

* <span data-ttu-id="f22c5-2673">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="f22c5-2673">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="f22c5-2674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2674">Az.Compute</span></span>

* <span data-ttu-id="f22c5-2675">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2675">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2676">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2676">Az.DataLakeStore</span></span>

* <span data-ttu-id="f22c5-2677">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="f22c5-2677">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="f22c5-2678">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="f22c5-2678">Az.FrontDoor</span></span>

* <span data-ttu-id="f22c5-2679">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="f22c5-2679">Fixed some broken links</span></span>
    - <span data-ttu-id="f22c5-2680">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2680">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="f22c5-2681">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2681">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="f22c5-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2682">Az.RecoveryServices</span></span>

* <span data-ttu-id="f22c5-2683">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2683">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="f22c5-2684">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2684">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="f22c5-2685">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2685">Az.Resources</span></span>

* <span data-ttu-id="f22c5-2686">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="f22c5-2686">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="f22c5-2687">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2687">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="f22c5-2688">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2688">Az.Sql</span></span>

* <span data-ttu-id="f22c5-2689">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="f22c5-2689">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="f22c5-2690">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="f22c5-2690">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="f22c5-2691">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2691">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="f22c5-2692">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2692">Az.Storage</span></span>

* <span data-ttu-id="f22c5-2693">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2693">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="f22c5-2694">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="f22c5-2694">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="f22c5-2695">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2695">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f22c5-2696">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="f22c5-2696">Support Static Website configuration</span></span>
    - <span data-ttu-id="f22c5-2697">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f22c5-2697">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="f22c5-2698">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="f22c5-2698">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="f22c5-2699">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2699">Az.Websites</span></span>

* <span data-ttu-id="f22c5-2700">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f22c5-2700">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="f22c5-2701">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2701">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="f22c5-2702">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2702">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="f22c5-2703">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f22c5-2703">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="f22c5-2704">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f22c5-2704">Az.ApiManagement</span></span>
* <span data-ttu-id="f22c5-2705">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2705">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="f22c5-2706">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="f22c5-2706">Az.Automation</span></span>
* <span data-ttu-id="f22c5-2707">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="f22c5-2707">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="f22c5-2708">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2708">Added Update Management cmdlets</span></span>
* <span data-ttu-id="f22c5-2709">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2709">Added Source Control cmdlets</span></span>
* <span data-ttu-id="f22c5-2710">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="f22c5-2710">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="f22c5-2711">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="f22c5-2711">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="f22c5-2712">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2712">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2713">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="f22c5-2713">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="f22c5-2714">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2714">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="f22c5-2715">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-2715">Az.ContainerInstance</span></span>
* <span data-ttu-id="f22c5-2716">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2716">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="f22c5-2717">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="f22c5-2717">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="f22c5-2718">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="f22c5-2718">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="f22c5-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2719">Az.Network</span></span>
* <span data-ttu-id="f22c5-2720">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2720">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="f22c5-2721">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="f22c5-2721">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="f22c5-2722">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2722">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="f22c5-2723">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f22c5-2723">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="f22c5-2724">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f22c5-2724">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f22c5-2725">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2725">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="f22c5-2726">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2726">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="f22c5-2727">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f22c5-2727">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="f22c5-2728">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f22c5-2728">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="f22c5-2729">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="f22c5-2729">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="f22c5-2730">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="f22c5-2730">Az.Relay</span></span>
* <span data-ttu-id="f22c5-2731">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2731">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="f22c5-2732">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2732">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2733">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f22c5-2733">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="f22c5-2734">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="f22c5-2734">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="f22c5-2735">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="f22c5-2735">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="f22c5-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-2737">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="f22c5-2737">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="f22c5-2738">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2738">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2739">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="f22c5-2739">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="f22c5-2740">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-2740">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22c5-2741">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-2741">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22c5-2742">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-2742">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22c5-2743">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="f22c5-2743">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="f22c5-2744">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f22c5-2744">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f22c5-2745">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f22c5-2745">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f22c5-2746">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f22c5-2746">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="f22c5-2747">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="f22c5-2747">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="f22c5-2748">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2748">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="f22c5-2749">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2749">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="f22c5-2750">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2750">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="f22c5-2751">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2751">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f22c5-2752">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2752">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="f22c5-2753">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2753">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="f22c5-2754">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2754">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="f22c5-2755">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f22c5-2755">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="f22c5-2756">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f22c5-2756">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="f22c5-2757">Geral</span><span class="sxs-lookup"><span data-stu-id="f22c5-2757">General</span></span>
* <span data-ttu-id="f22c5-2758">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="f22c5-2758">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="f22c5-2759">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2759">Az.Profile</span></span>
* <span data-ttu-id="f22c5-2760">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f22c5-2760">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="f22c5-2761">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="f22c5-2761">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="f22c5-2762">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f22c5-2762">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="f22c5-2763">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="f22c5-2763">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="f22c5-2764">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="f22c5-2764">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="f22c5-2765">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="f22c5-2765">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="f22c5-2766">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="f22c5-2766">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-2767">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2767">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-2768">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2768">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2769">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2770">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f22c5-2770">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="f22c5-2771">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="f22c5-2771">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="f22c5-2772">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2772">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2773">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-2774">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2774">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="f22c5-2775">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2775">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="f22c5-2776">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="f22c5-2776">Az.Insights</span></span>
* <span data-ttu-id="f22c5-2777">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="f22c5-2777">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="f22c5-2778">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="f22c5-2778">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="f22c5-2779">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="f22c5-2779">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="f22c5-2780">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="f22c5-2780">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2781">Az.Network</span></span>
* <span data-ttu-id="f22c5-2782">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="f22c5-2782">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="f22c5-2783">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-2783">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="f22c5-2784">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-2784">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="f22c5-2785">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f22c5-2785">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="f22c5-2786">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-2786">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="f22c5-2787">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f22c5-2787">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="f22c5-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f22c5-2788">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="f22c5-2789">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f22c5-2789">Az.PolicyInsights</span></span>
* <span data-ttu-id="f22c5-2790">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="f22c5-2790">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2791">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2792">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="f22c5-2792">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="f22c5-2793">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="f22c5-2793">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="f22c5-2794">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="f22c5-2794">Az.ServiceBus</span></span>
* <span data-ttu-id="f22c5-2795">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2795">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="f22c5-2796">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f22c5-2796">Az.ServiceFabric</span></span>
* <span data-ttu-id="f22c5-2797">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2797">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="f22c5-2798">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="f22c5-2798">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="f22c5-2799">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="f22c5-2799">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="f22c5-2800">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="f22c5-2800">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="f22c5-2801">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2801">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="f22c5-2802">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="f22c5-2802">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="f22c5-2803">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2803">Az.Profile</span></span>
* <span data-ttu-id="f22c5-2804">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="f22c5-2804">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="f22c5-2805">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="f22c5-2805">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2806">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2807">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="f22c5-2807">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="f22c5-2808">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2808">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="f22c5-2809">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f22c5-2809">Az.DataLakeStore</span></span>
* <span data-ttu-id="f22c5-2810">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="f22c5-2810">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="f22c5-2811">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2811">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="f22c5-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2812">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f22c5-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2813">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="f22c5-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2814">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2815">Az.Network</span></span>
* <span data-ttu-id="f22c5-2816">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2816">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="f22c5-2817">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2817">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2818">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2819">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2819">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="f22c5-2820">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2820">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="f22c5-2821">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="f22c5-2821">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="f22c5-2822">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2822">Azure.Storage</span></span>
* <span data-ttu-id="f22c5-2823">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2823">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="f22c5-2824">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2824">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="f22c5-2825">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f22c5-2825">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="f22c5-2826">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2826">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="f22c5-2827">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="f22c5-2827">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="f22c5-2828">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="f22c5-2828">Az.CognitiveServices</span></span>
* <span data-ttu-id="f22c5-2829">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2829">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="f22c5-2830">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="f22c5-2830">Az.Compute</span></span>
* <span data-ttu-id="f22c5-2831">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="f22c5-2831">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="f22c5-2832">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2832">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="f22c5-2833">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="f22c5-2833">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="f22c5-2834">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f22c5-2834">Az.DataFactoryV2</span></span>
* <span data-ttu-id="f22c5-2835">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2835">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="f22c5-2836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="f22c5-2836">Az.Network</span></span>
* <span data-ttu-id="f22c5-2837">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2837">Added NetworkProfile functionality.</span></span> <span data-ttu-id="f22c5-2838">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="f22c5-2838">new cmdlets added</span></span>
    - <span data-ttu-id="f22c5-2839">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2839">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22c5-2840">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2840">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22c5-2841">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2841">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22c5-2842">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f22c5-2842">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="f22c5-2843">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-2843">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="f22c5-2844">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-2844">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="f22c5-2845">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="f22c5-2845">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="f22c5-2846">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f22c5-2846">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="f22c5-2847">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="f22c5-2847">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="f22c5-2848">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="f22c5-2848">Az.RedisCache</span></span>
* <span data-ttu-id="f22c5-2849">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="f22c5-2849">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="f22c5-2850">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="f22c5-2850">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="f22c5-2851">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f22c5-2851">Az.Resources</span></span>
* <span data-ttu-id="f22c5-2852">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f22c5-2852">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="f22c5-2853">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="f22c5-2853">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="f22c5-2854">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="f22c5-2854">Az.Sql</span></span>
* <span data-ttu-id="f22c5-2855">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="f22c5-2855">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="f22c5-2856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="f22c5-2856">Az.Websites</span></span>
* <span data-ttu-id="f22c5-2857">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="f22c5-2857">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="f22c5-2858">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="f22c5-2858">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="f22c5-2859">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="f22c5-2859">0.2.0 - September 2018</span></span>
 <span data-ttu-id="f22c5-2860">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="f22c5-2860">Initial Release</span></span>
