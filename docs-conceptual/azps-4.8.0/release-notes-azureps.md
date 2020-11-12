---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ea374b23e85c16393e5de16b043ae0c28545cb61
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408064"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="44422-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="44422-103">Azure PowerShell release notes</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="44422-104">4.8.0 – Outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-104">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-105">Az.Accounts</span></span>
* <span data-ttu-id="44422-106">Foi corrigido um problema de análise de datetime em bibliotecas comuns [#13045]</span><span class="sxs-lookup"><span data-stu-id="44422-106">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-107">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-107">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-108">Foi adicionado o cmdlet 'New-AzCognitiveServicesAccountApiProperty'.</span><span class="sxs-lookup"><span data-stu-id="44422-108">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="44422-109">Parâmetro 'ApiProperty' compatível com 'New-AzCognitiveServicesAccount' e 'Set-AzCognitiveServicesAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-109">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-110">Az.Compute</span></span>
* <span data-ttu-id="44422-111">Foi corrigido o problema em 'Update-ASRRecoveryPlan' populando o FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="44422-111">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="44422-112">Foram adicionados os parâmetros opcionais '-Top' e '-OrderBy' ao cmdlet 'Get-AzVmImage'.</span><span class="sxs-lookup"><span data-stu-id="44422-112">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="44422-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="44422-113">Az.Databricks</span></span>
* <span data-ttu-id="44422-114">Disponibilidade geral do módulo 'Az.Databricks'</span><span class="sxs-lookup"><span data-stu-id="44422-114">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="44422-115">Foi adicionado suporte para emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="44422-115">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-116">Az.DataFactory</span></span>
* <span data-ttu-id="44422-117">Foi corrigido erro de digitação nas mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="44422-117">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-118">Az.EventHub</span></span>
* <span data-ttu-id="44422-119">Foi adicionado o parâmetro de opção opcional 'TrustedServiceAccessEnabled' ao cmdlet 'Set-AzEventHubNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="44422-119">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-120">Az.HDInsight</span></span>
* <span data-ttu-id="44422-121">Foi adicionada uma mensagem de aviso para planejamento do preterimento dos parâmetros 'PublicNetworkAccessType' e 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="44422-121">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="44422-122">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="44422-122">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="44422-123">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="44422-123">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="44422-124">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="44422-124">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="44422-125">Adicionada mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageContainer' por 'StorageContainer'</span><span class="sxs-lookup"><span data-stu-id="44422-125">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="44422-126">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageRootPath' por 'StorageRootPath'</span><span class="sxs-lookup"><span data-stu-id="44422-126">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-127">Az.IotHub</span></span>
* <span data-ttu-id="44422-128">O SDK de dispositivos foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="44422-128">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-129">Az.KeyVault</span></span>
* <span data-ttu-id="44422-130">A data detalhada da remoção da propriedade SecretValueText foi fornecida</span><span class="sxs-lookup"><span data-stu-id="44422-130">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="44422-131">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="44422-131">Az.ManagedServices</span></span>
* <span data-ttu-id="44422-132">Os avisos de alteração da falha nos cmdlets de definição e atribuição de serviços gerenciados foram atualizados</span><span class="sxs-lookup"><span data-stu-id="44422-132">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-133">Az.Monitor</span></span>
* <span data-ttu-id="44422-134">Foi corrigido o bug que fazia com que a mensagem de aviso não pudesse ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="44422-134">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="44422-135">[#12889]</span><span class="sxs-lookup"><span data-stu-id="44422-135">[#12889]</span></span>
* <span data-ttu-id="44422-136">Parâmetro 'SkipMetricValidation' com suporte nos critérios da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="44422-136">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="44422-137">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação da métrica seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="44422-137">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-138">Az.Network</span></span>
* <span data-ttu-id="44422-139">Política do Office365 adicionada ao recurso VPNSite</span><span class="sxs-lookup"><span data-stu-id="44422-139">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="44422-140">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-140">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-141">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-142">Foi adicionada a validação do nome do contêiner para backup da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="44422-142">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="44422-143">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="44422-143">Az.RedisCache</span></span>
* <span data-ttu-id="44422-144">Correção dos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache' para não falharem devido a um problema de permissão relacionado ao registro do RP do Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="44422-144">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-145">Az.Sql</span></span>
* <span data-ttu-id="44422-146">Foi adicionado BackupStorageRedundancy ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="44422-146">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="44422-147">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="44422-147">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="44422-148">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="44422-148">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="44422-149">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="44422-149">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="44422-150">Foi removida a diferenciação de maiúsculas e minúsculas para o parâmetro BackupStorageRedundancy em todas as referências de Banco de Dados SQL</span><span class="sxs-lookup"><span data-stu-id="44422-150">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="44422-151">Foram atualizados os nomes das mensagens de aviso do BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="44422-151">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-152">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-152">Az.Storage</span></span>
* <span data-ttu-id="44422-153">Suporte para habilitar/desabilitar/obter propriedades de exclusão reversível de compartilhamento no serviço de arquivo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-153">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="44422-154">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-154">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="44422-155">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-155">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="44422-156">Os compartilhamentos de arquivos de lista com suporte incluem os excluídos de uma conta de armazenamento e obtêm uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="44422-156">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="44422-157">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-157">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="44422-158">Suporte para restauração de um compartilhamento de arquivo excluído</span><span class="sxs-lookup"><span data-stu-id="44422-158">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="44422-159">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="44422-159">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="44422-160">Foram alterados os cmdlets para modificar as propriedades do serviço blobs, não obtendo as propriedades originais do servidor, mas apenas definindo as propriedades modificadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="44422-160">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="44422-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="44422-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="44422-163">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-163">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="44422-164">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-164">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="44422-165">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-165">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="44422-166">Foi corrigido o problema de ajuda para o valor padrão do tipo do parâmetro New-AzStorageAccount [#12189]</span><span class="sxs-lookup"><span data-stu-id="44422-166">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="44422-167">Foi corrigido o problema adicionando exemplo para mostrar como definir o ContentType correto no upload do blob [#12989]</span><span class="sxs-lookup"><span data-stu-id="44422-167">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="44422-168">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-168">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-169">Az.Accounts</span></span>
* <span data-ttu-id="44422-170">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="44422-170">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="44422-171">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="44422-171">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="44422-172">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="44422-172">Az.Aks</span></span>
* <span data-ttu-id="44422-173">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="44422-173">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="44422-174">[#12372]</span><span class="sxs-lookup"><span data-stu-id="44422-174">[#12372]</span></span>
* <span data-ttu-id="44422-175">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-175">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="44422-176">[#11239]</span><span class="sxs-lookup"><span data-stu-id="44422-176">[#11239]</span></span>
* <span data-ttu-id="44422-177">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="44422-177">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="44422-178">[#11239]</span><span class="sxs-lookup"><span data-stu-id="44422-178">[#11239]</span></span>
* <span data-ttu-id="44422-179">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-179">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="44422-180">[#12371]</span><span class="sxs-lookup"><span data-stu-id="44422-180">[#12371]</span></span>
* <span data-ttu-id="44422-181">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="44422-181">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-182">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-183">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="44422-183">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-184">Az.Compute</span></span>
* <span data-ttu-id="44422-185">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-185">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="44422-186">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="44422-186">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="44422-187">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-187">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="44422-188">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-188">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="44422-189">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="44422-189">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="44422-190">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="44422-190">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="44422-191">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="44422-191">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="44422-192">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="44422-192">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="44422-193">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-193">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="44422-194">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="44422-194">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-195">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-195">Az.DataFactory</span></span>
* <span data-ttu-id="44422-196">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="44422-196">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-197">Az.EventHub</span></span>
* <span data-ttu-id="44422-198">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="44422-198">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="44422-199">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="44422-199">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="44422-200">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="44422-200">Az.Functions</span></span>
* <span data-ttu-id="44422-201">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="44422-201">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="44422-202">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="44422-202">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="44422-203">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="44422-203">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-204">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-204">Az.HDInsight</span></span>
* <span data-ttu-id="44422-205">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="44422-205">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="44422-206">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="44422-206">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="44422-207">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="44422-207">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="44422-208">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-208">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="44422-209">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-209">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="44422-210">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-210">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="44422-211">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-211">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="44422-212">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="44422-212">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-213">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-213">Az.KeyVault</span></span>
* <span data-ttu-id="44422-214">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="44422-214">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="44422-215">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="44422-215">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="44422-216">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="44422-216">Az.Kusto</span></span>
* <span data-ttu-id="44422-217">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="44422-217">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-218">Az.Network</span></span>
* <span data-ttu-id="44422-219">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="44422-219">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="44422-220">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="44422-220">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="44422-221">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="44422-221">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="44422-222">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="44422-222">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="44422-223">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="44422-223">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="44422-224">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-224">Added subscription level parameter set</span></span>
    - <span data-ttu-id="44422-225">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="44422-225">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="44422-226">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="44422-226">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="44422-227">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="44422-227">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="44422-228">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="44422-228">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="44422-229">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-229">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="44422-230">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="44422-230">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="44422-231">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44422-231">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="44422-232">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="44422-232">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="44422-233">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="44422-233">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="44422-234">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="44422-234">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="44422-235">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="44422-235">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="44422-236">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="44422-236">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="44422-237">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="44422-237">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="44422-238">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="44422-238">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="44422-239">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="44422-239">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="44422-240">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="44422-240">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="44422-241">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="44422-241">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="44422-242">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="44422-242">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-243">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-243">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-244">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="44422-244">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-245">Az.Resources</span></span>
* <span data-ttu-id="44422-246">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="44422-246">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="44422-247">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="44422-247">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="44422-248">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="44422-248">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="44422-249">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="44422-249">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-250">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-250">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-251">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="44422-251">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="44422-252">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="44422-252">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="44422-253">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="44422-253">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="44422-254">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="44422-254">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="44422-255">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="44422-255">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="44422-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="44422-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="44422-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="44422-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="44422-258">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="44422-258">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="44422-259">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="44422-259">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="44422-260">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="44422-260">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="44422-261">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="44422-261">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="44422-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="44422-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="44422-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="44422-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="44422-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="44422-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="44422-265">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="44422-265">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="44422-266">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="44422-266">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-267">Az.Sql</span></span>
* <span data-ttu-id="44422-268">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="44422-268">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="44422-269">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-269">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="44422-270">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-270">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="44422-271">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="44422-271">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="44422-272">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-272">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="44422-273">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="44422-273">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="44422-274">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="44422-274">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="44422-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="44422-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="44422-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="44422-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="44422-277">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-277">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="44422-278">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-278">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="44422-279">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-279">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="44422-280">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="44422-280">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="44422-281">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-281">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="44422-282">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="44422-282">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="44422-283">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="44422-283">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="44422-284">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="44422-284">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="44422-285">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="44422-285">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-286">Az.Storage</span></span>
* <span data-ttu-id="44422-287">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="44422-287">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="44422-288">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="44422-288">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="44422-289">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-289">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="44422-290">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-290">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="44422-291">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="44422-291">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="44422-292">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="44422-292">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="44422-293">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="44422-293">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="44422-294">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-294">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="44422-295">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="44422-295">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="44422-296">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-296">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="44422-297">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-297">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="44422-298">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-298">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="44422-299">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-299">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="44422-300">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="44422-300">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="44422-301">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="44422-301">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="44422-302">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="44422-302">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="44422-303">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="44422-303">Thanks to our community contributors</span></span>
* <span data-ttu-id="44422-304">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="44422-304">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="44422-305">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="44422-305">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="44422-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="44422-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="44422-307">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="44422-307">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="44422-308">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="44422-308">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="44422-309">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="44422-309">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="44422-310">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="44422-310">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="44422-311">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="44422-311">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="44422-312">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="44422-312">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="44422-313">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="44422-313">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="44422-314">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="44422-314">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="44422-315">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-315">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="44422-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-316">Az.Compute</span></span>
* <span data-ttu-id="44422-317">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="44422-317">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="44422-318">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-318">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-319">Az.Accounts</span></span>
* <span data-ttu-id="44422-320">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="44422-320">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="44422-321">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="44422-321">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-322">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-322">Az.Automation</span></span>
* <span data-ttu-id="44422-323">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="44422-323">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-324">Az.Compute</span></span>
* <span data-ttu-id="44422-325">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="44422-325">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="44422-326">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="44422-326">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="44422-327">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-327">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="44422-328">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="44422-328">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-329">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-329">Az.DataFactory</span></span>
* <span data-ttu-id="44422-330">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="44422-330">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-331">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-331">Az.HDInsight</span></span>
* <span data-ttu-id="44422-332">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="44422-332">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-333">Az.KeyVault</span></span>
* <span data-ttu-id="44422-334">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="44422-334">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="44422-335">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="44422-335">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="44422-336">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="44422-336">Az.Maintenance</span></span>
* <span data-ttu-id="44422-337">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-337">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="44422-338">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-338">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="44422-339">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="44422-339">Az.ManagedServices</span></span>
* <span data-ttu-id="44422-340">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="44422-340">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-341">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-341">Az.Monitor</span></span>
* <span data-ttu-id="44422-342">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="44422-342">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="44422-343">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="44422-343">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-344">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-344">Az.Resources</span></span>
* <span data-ttu-id="44422-345">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="44422-345">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="44422-346">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="44422-346">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="44422-347">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="44422-347">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="44422-348">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="44422-348">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="44422-349">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="44422-349">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="44422-350">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="44422-350">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="44422-351">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="44422-351">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="44422-352">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="44422-352">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="44422-353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="44422-353">Az.SignalR</span></span>
* <span data-ttu-id="44422-354">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="44422-354">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="44422-355">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="44422-355">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-356">Az.Storage</span></span>
* <span data-ttu-id="44422-357">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="44422-357">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="44422-358">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="44422-358">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="44422-359">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-359">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="44422-360">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="44422-360">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="44422-361">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="44422-361">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="44422-362">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="44422-362">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="44422-363">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="44422-363">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="44422-364">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="44422-364">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="44422-365">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-365">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="44422-366">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="44422-366">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="44422-367">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-367">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="44422-368">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-368">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="44422-369">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-369">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="44422-370">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-370">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="44422-371">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-371">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="44422-372">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-372">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-373">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-373">Az.Accounts</span></span>
* <span data-ttu-id="44422-374">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="44422-374">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="44422-375">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="44422-375">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="44422-376">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="44422-376">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="44422-377">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="44422-377">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="44422-378">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="44422-378">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="44422-379">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="44422-379">Az.Aks</span></span>
* <span data-ttu-id="44422-380">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="44422-380">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="44422-381">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="44422-381">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-382">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-382">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-383">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-383">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="44422-384">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-384">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="44422-385">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="44422-385">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="44422-386">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="44422-386">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="44422-387">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-387">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="44422-388">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="44422-388">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="44422-389">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="44422-389">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="44422-390">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-390">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="44422-391">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-391">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="44422-392">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="44422-392">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="44422-393">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-393">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="44422-394">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="44422-394">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-395">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-395">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-396">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="44422-396">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-397">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-397">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-398">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="44422-398">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-399">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-399">Az.HDInsight</span></span>
* <span data-ttu-id="44422-400">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="44422-400">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="44422-401">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="44422-401">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="44422-402">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="44422-402">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="44422-403">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="44422-403">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="44422-404">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="44422-404">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="44422-405">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="44422-405">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="44422-406">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="44422-406">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-407">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-407">Az.Network</span></span>
* <span data-ttu-id="44422-408">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-408">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="44422-409">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="44422-409">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="44422-410">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="44422-410">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="44422-411">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="44422-411">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-412">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-412">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-413">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="44422-413">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="44422-414">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="44422-414">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="44422-415">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="44422-415">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-417">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-417">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-418">Az.Resources</span></span>
* <span data-ttu-id="44422-419">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="44422-419">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="44422-420">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="44422-420">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-421">Az.Sql</span></span>
* <span data-ttu-id="44422-422">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="44422-422">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="44422-423">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="44422-423">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-424">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-424">Az.Storage</span></span>
* <span data-ttu-id="44422-425">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="44422-425">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="44422-426">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="44422-426">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="44422-427">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="44422-427">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="44422-428">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="44422-428">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="44422-429">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="44422-429">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="44422-430">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="44422-430">Supported get single file share usage</span></span>
    - <span data-ttu-id="44422-431">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-431">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="44422-432">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-432">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-433">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-433">Az.Accounts</span></span>
* <span data-ttu-id="44422-434">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-434">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="44422-435">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="44422-435">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="44422-436">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="44422-436">Az.Aks</span></span>
* <span data-ttu-id="44422-437">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="44422-437">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="44422-438">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="44422-438">Az.AnalysisServices</span></span>
* <span data-ttu-id="44422-439">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="44422-439">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-440">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-440">Az.Automation</span></span>
* <span data-ttu-id="44422-441">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="44422-441">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-442">Az.Compute</span></span>
* <span data-ttu-id="44422-443">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="44422-443">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-444">Az.DataFactory</span></span>
* <span data-ttu-id="44422-445">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="44422-445">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="44422-446">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="44422-446">Az.EventGrid</span></span>
* <span data-ttu-id="44422-447">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="44422-447">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="44422-448">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-448">Added new features:</span></span>
    - <span data-ttu-id="44422-449">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="44422-449">Input mapping</span></span>
    - <span data-ttu-id="44422-450">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="44422-450">Event Delivery Schema</span></span>
    - <span data-ttu-id="44422-451">Link Privado</span><span class="sxs-lookup"><span data-stu-id="44422-451">Private Link</span></span>
    - <span data-ttu-id="44422-452">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="44422-452">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="44422-453">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="44422-453">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="44422-454">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="44422-454">Azure Function As Destination</span></span>
    - <span data-ttu-id="44422-455">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="44422-455">WebHook Batching</span></span>
    - <span data-ttu-id="44422-456">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="44422-456">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="44422-457">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="44422-457">IpFiltering</span></span>
* <span data-ttu-id="44422-458">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="44422-458">Updated cmdlets:</span></span>
    - <span data-ttu-id="44422-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="44422-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="44422-460">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="44422-460">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="44422-461">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="44422-461">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="44422-462">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="44422-462">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="44422-463">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="44422-463">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="44422-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="44422-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="44422-465">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="44422-465">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="44422-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="44422-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="44422-467">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="44422-467">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-468">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-468">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-469">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="44422-469">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="44422-470">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="44422-470">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-471">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-471">Az.HDInsight</span></span>
* <span data-ttu-id="44422-472">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="44422-472">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-473">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-473">Az.Monitor</span></span>
* <span data-ttu-id="44422-474">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="44422-474">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-475">Az.Network</span></span>
* <span data-ttu-id="44422-476">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="44422-476">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="44422-477">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-477">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="44422-478">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="44422-478">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="44422-479">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="44422-479">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="44422-480">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="44422-480">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="44422-481">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="44422-481">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="44422-482">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-482">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="44422-483">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-483">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="44422-484">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="44422-484">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="44422-485">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="44422-485">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="44422-486">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="44422-486">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="44422-487">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="44422-487">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="44422-488">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="44422-488">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="44422-489">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-489">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="44422-490">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="44422-490">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="44422-491">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="44422-491">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="44422-492">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="44422-492">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-493">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-493">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-494">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="44422-494">Removed project reference to Authentication</span></span>
* <span data-ttu-id="44422-495">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="44422-495">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="44422-496">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="44422-496">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-497">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-497">Az.Resources</span></span>
* <span data-ttu-id="44422-498">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="44422-498">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="44422-499">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-499">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-500">Az.Sql</span></span>
* <span data-ttu-id="44422-501">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="44422-501">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="44422-502">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="44422-502">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="44422-503">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="44422-503">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-504">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-504">Az.Storage</span></span>
* <span data-ttu-id="44422-505">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="44422-505">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="44422-506">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="44422-506">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="44422-507">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-507">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="44422-508">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-508">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="44422-509">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-509">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="44422-510">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="44422-510">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="44422-511">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="44422-511">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="44422-512">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="44422-512">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="44422-513">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="44422-513">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="44422-514">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="44422-514">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="44422-515">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="44422-515">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="44422-516">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="44422-516">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="44422-517">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="44422-517">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="44422-518">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="44422-518">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="44422-519">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="44422-519">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="44422-520">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="44422-520">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="44422-521">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="44422-521">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="44422-522">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="44422-522">Az.StorageSync</span></span>
* <span data-ttu-id="44422-523">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="44422-523">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="44422-524">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-524">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="44422-525">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="44422-525">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="44422-526">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="44422-526">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-527">Az.Websites</span></span>
* <span data-ttu-id="44422-528">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="44422-528">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="44422-529">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-529">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-530">Az.Accounts</span></span>
* <span data-ttu-id="44422-531">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="44422-531">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="44422-532">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="44422-532">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="44422-533">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="44422-533">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="44422-534">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="44422-534">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="44422-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="44422-535">Az.Aks</span></span>
* <span data-ttu-id="44422-536">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="44422-536">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="44422-537">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-537">Az.Batch</span></span>
* <span data-ttu-id="44422-538">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="44422-538">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="44422-539">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-539">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-540">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-540">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-541">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="44422-541">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="44422-542">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="44422-542">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-543">Az.Compute</span></span>
* <span data-ttu-id="44422-544">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="44422-544">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="44422-545">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="44422-545">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="44422-546">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="44422-546">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="44422-547">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="44422-547">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="44422-548">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="44422-548">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-549">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-549">Az.DataFactory</span></span>
* <span data-ttu-id="44422-550">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="44422-550">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-551">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-551">Az.EventHub</span></span>
* <span data-ttu-id="44422-552">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="44422-552">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="44422-553">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="44422-553">Az.Functions</span></span>
* <span data-ttu-id="44422-554">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="44422-554">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-555">Az.HDInsight</span></span>
* <span data-ttu-id="44422-556">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="44422-556">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="44422-557">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="44422-557">Az.HealthcareApis</span></span>
* <span data-ttu-id="44422-558">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="44422-558">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="44422-559">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="44422-559">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-560">Az.Monitor</span></span>
* <span data-ttu-id="44422-561">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="44422-561">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="44422-562">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="44422-562">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-563">Az.Network</span></span>
* <span data-ttu-id="44422-564">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="44422-565">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-565">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="44422-566">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="44422-566">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="44422-567">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="44422-567">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="44422-568">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="44422-568">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="44422-569">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-569">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="44422-570">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="44422-570">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="44422-571">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="44422-571">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="44422-572">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="44422-572">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="44422-573">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="44422-573">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="44422-574">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-574">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="44422-575">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-575">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="44422-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="44422-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="44422-577">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-577">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="44422-578">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="44422-578">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="44422-579">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="44422-579">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="44422-580">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="44422-580">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="44422-581">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="44422-581">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="44422-582">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="44422-582">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="44422-583">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="44422-583">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="44422-584">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="44422-584">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="44422-585">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="44422-585">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="44422-586">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="44422-586">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="44422-587">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="44422-587">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="44422-588">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="44422-588">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="44422-589">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="44422-589">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="44422-590">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="44422-590">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="44422-591">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="44422-591">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="44422-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="44422-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="44422-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="44422-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="44422-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="44422-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="44422-598">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="44422-598">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="44422-599">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="44422-599">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="44422-600">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="44422-600">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="44422-601">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="44422-601">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="44422-602">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="44422-602">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="44422-603">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="44422-603">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="44422-604">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="44422-604">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="44422-605">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-605">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="44422-606">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-606">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="44422-607">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-607">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="44422-608">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-608">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="44422-609">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-609">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="44422-610">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-610">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="44422-611">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="44422-611">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="44422-612">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="44422-612">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-613">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-613">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-614">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="44422-614">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="44422-615">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="44422-615">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="44422-616">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="44422-616">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="44422-617">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="44422-617">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="44422-618">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="44422-618">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-619">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-620">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-620">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="44422-621">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="44422-621">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-622">Az.Resources</span></span>
* <span data-ttu-id="44422-623">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="44422-623">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="44422-624">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="44422-624">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="44422-625">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="44422-625">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="44422-626">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-626">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="44422-627">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="44422-627">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="44422-628">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="44422-628">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-629">Az.Sql</span></span>
* <span data-ttu-id="44422-630">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="44422-630">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="44422-631">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="44422-631">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="44422-632">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="44422-632">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-633">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-633">Az.Storage</span></span>
* <span data-ttu-id="44422-634">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="44422-634">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="44422-635">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-635">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="44422-636">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-636">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-637">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-637">Az.Websites</span></span>
* <span data-ttu-id="44422-638">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="44422-638">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="44422-639">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="44422-639">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="44422-640">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="44422-640">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="44422-641">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44422-641">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="44422-642">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="44422-642">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="44422-643">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="44422-643">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="44422-644">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-644">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-645">Az.Accounts</span></span>
* <span data-ttu-id="44422-646">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="44422-646">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="44422-647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="44422-647">Az.AnalysisServices</span></span>
* <span data-ttu-id="44422-648">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-648">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-649">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-649">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-650">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-650">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="44422-651">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="44422-651">Az.Billing</span></span>
* <span data-ttu-id="44422-652">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-652">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-653">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-654">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="44422-654">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="44422-655">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-655">Az.DataFactory</span></span>
* <span data-ttu-id="44422-656">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-656">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="44422-657">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="44422-657">Az.DataShare</span></span>
* <span data-ttu-id="44422-658">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="44422-658">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="44422-659">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="44422-659">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="44422-660">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="44422-660">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-661">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-661">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-662">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="44422-662">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="44422-663">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="44422-663">Added optional parameters to</span></span> 
    - <span data-ttu-id="44422-664">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="44422-664">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="44422-665">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="44422-665">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-667">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="44422-667">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="44422-668">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="44422-668">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="44422-669">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-669">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="44422-670">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="44422-670">Az.PrivateDns</span></span>
* <span data-ttu-id="44422-671">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="44422-671">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-673">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="44422-673">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="44422-674">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="44422-674">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-675">Az.Resources</span></span>
* <span data-ttu-id="44422-676">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="44422-676">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="44422-677">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="44422-677">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="44422-678">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="44422-678">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="44422-679">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44422-679">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="44422-680">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-680">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-681">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-681">Az.Sql</span></span>
* <span data-ttu-id="44422-682">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="44422-682">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="44422-683">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="44422-683">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="44422-684">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="44422-684">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-685">Az.Storage</span></span>
* <span data-ttu-id="44422-686">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-686">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="44422-687">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-687">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="44422-688">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="44422-688">Highlights since the last release</span></span>
* <span data-ttu-id="44422-689">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="44422-689">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="44422-690">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="44422-690">General availability of Az.Functions</span></span> 
* <span data-ttu-id="44422-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="44422-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-692">Az.Accounts</span></span>
* <span data-ttu-id="44422-693">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="44422-693">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="44422-694">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="44422-694">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="44422-695">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="44422-695">Az.Aks</span></span>
* <span data-ttu-id="44422-696">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="44422-696">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="44422-697">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="44422-697">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="44422-698">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="44422-698">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-699">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-699">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-700">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="44422-700">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="44422-701">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="44422-701">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="44422-702">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="44422-702">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="44422-703">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="44422-703">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="44422-704">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="44422-704">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="44422-705">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="44422-705">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="44422-706">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="44422-706">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="44422-707">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="44422-707">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="44422-708">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="44422-708">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="44422-709">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="44422-709">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="44422-710">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="44422-710">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="44422-711">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="44422-711">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="44422-712">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="44422-712">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="44422-713">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="44422-713">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="44422-714">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="44422-714">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="44422-715">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="44422-715">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="44422-716">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="44422-716">Az.ApplicationInsights</span></span>
* <span data-ttu-id="44422-717">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="44422-717">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="44422-718">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="44422-718">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="44422-719">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="44422-719">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="44422-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-720">Az.Batch</span></span>
* <span data-ttu-id="44422-721">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="44422-721">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="44422-722">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="44422-722">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="44422-723">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="44422-723">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="44422-724">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="44422-724">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="44422-725">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="44422-725">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="44422-726">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="44422-726">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="44422-727">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="44422-727">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="44422-728">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="44422-728">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="44422-729">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="44422-729">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-730">Az.Compute</span></span>
* <span data-ttu-id="44422-731">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="44422-731">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="44422-732">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="44422-732">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="44422-733">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="44422-733">Breaking changes</span></span>
    - <span data-ttu-id="44422-734">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="44422-734">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="44422-735">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="44422-735">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="44422-736">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="44422-736">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="44422-737">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="44422-737">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="44422-738">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="44422-738">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="44422-739">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="44422-739">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="44422-740">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="44422-740">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="44422-741">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-741">Az.DataFactory</span></span>
* <span data-ttu-id="44422-742">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="44422-742">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-743">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-744">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="44422-744">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="44422-745">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="44422-745">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="44422-746">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="44422-746">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="44422-747">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="44422-747">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="44422-748">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="44422-748">Az.Functions</span></span>
* <span data-ttu-id="44422-749">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="44422-749">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-750">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-750">Az.HDInsight</span></span>
* <span data-ttu-id="44422-751">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="44422-751">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="44422-752">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="44422-752">Az.HealthcareApis</span></span>
* <span data-ttu-id="44422-753">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="44422-753">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-754">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-754">Az.IotHub</span></span>
* <span data-ttu-id="44422-755">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="44422-755">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="44422-756">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="44422-756">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="44422-757">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="44422-757">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="44422-758">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="44422-758">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="44422-759">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="44422-759">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="44422-760">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-760">New cmdlets are:</span></span>
    - <span data-ttu-id="44422-761">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-761">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="44422-762">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-762">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="44422-763">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-763">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="44422-764">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-764">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="44422-765">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="44422-765">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="44422-766">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="44422-766">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-767">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-767">Az.KeyVault</span></span>
* <span data-ttu-id="44422-768">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="44422-768">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="44422-769">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="44422-769">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="44422-770">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="44422-770">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="44422-771">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="44422-771">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="44422-772">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="44422-772">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="44422-773">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="44422-773">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="44422-774">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="44422-774">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-775">Az.Monitor</span></span>
* <span data-ttu-id="44422-776">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="44422-776">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="44422-777">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="44422-777">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="44422-778">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="44422-778">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="44422-779">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="44422-779">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="44422-780">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="44422-780">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="44422-781">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="44422-781">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="44422-782">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="44422-782">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-783">Az.Network</span></span>
* <span data-ttu-id="44422-784">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="44422-784">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="44422-785">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="44422-785">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="44422-786">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="44422-786">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="44422-787">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-787">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="44422-788">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44422-788">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="44422-789">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-789">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-790">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44422-790">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="44422-791">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44422-791">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="44422-792">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44422-792">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="44422-793">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44422-793">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="44422-794">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-794">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="44422-795">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="44422-795">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="44422-796">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="44422-796">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="44422-797">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="44422-797">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="44422-798">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="44422-798">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="44422-799">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="44422-799">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="44422-800">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="44422-800">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="44422-801">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-801">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="44422-802">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-802">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="44422-803">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-803">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="44422-804">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-804">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="44422-805">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="44422-805">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="44422-806">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="44422-806">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="44422-807">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="44422-807">Updated cmdlet:</span></span>
        - <span data-ttu-id="44422-808">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="44422-808">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-809">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-809">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-810">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="44422-810">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="44422-811">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="44422-811">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="44422-812">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="44422-812">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="44422-813">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="44422-813">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="44422-814">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="44422-814">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="44422-815">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="44422-815">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="44422-816">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="44422-816">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="44422-817">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="44422-817">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-818">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-818">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-819">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-819">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="44422-820">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="44422-820">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="44422-821">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="44422-821">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="44422-822">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="44422-822">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="44422-823">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="44422-823">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-824">Az.Resources</span></span>
* <span data-ttu-id="44422-825">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="44422-825">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="44422-826">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="44422-826">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="44422-827">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="44422-827">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="44422-828">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="44422-828">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="44422-829">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="44422-829">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="44422-830">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="44422-830">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="44422-831">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="44422-831">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="44422-832">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="44422-832">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="44422-833">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="44422-833">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="44422-834">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="44422-834">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="44422-835">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="44422-835">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="44422-836">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="44422-836">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="44422-837">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="44422-837">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="44422-838">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="44422-838">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="44422-839">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="44422-839">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="44422-840">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="44422-840">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="44422-841">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-841">'New-AzDeployment'</span></span>
    - <span data-ttu-id="44422-842">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-842">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="44422-843">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-843">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="44422-844">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-844">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-845">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-845">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-846">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="44422-846">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-847">Az.Sql</span></span>
* <span data-ttu-id="44422-848">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="44422-848">Enhance performance of:</span></span>
    - <span data-ttu-id="44422-849">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="44422-849">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="44422-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="44422-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="44422-851">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="44422-851">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="44422-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="44422-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="44422-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="44422-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="44422-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="44422-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="44422-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="44422-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="44422-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="44422-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="44422-857">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-857">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="44422-858">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="44422-858">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-859">Az.Storage</span></span>
* <span data-ttu-id="44422-860">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-860">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="44422-861">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="44422-861">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="44422-862">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-862">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="44422-863">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="44422-863">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="44422-864">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="44422-864">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="44422-865">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="44422-865">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="44422-866">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="44422-866">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="44422-867">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="44422-867">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="44422-868">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="44422-868">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="44422-869">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="44422-869">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="44422-870">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="44422-870">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="44422-871">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="44422-871">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="44422-872">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="44422-872">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="44422-873">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-873">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="44422-874">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-874">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="44422-875">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-875">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="44422-876">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-876">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="44422-877">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="44422-877">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="44422-878">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="44422-878">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="44422-879">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="44422-879">Supported failover Storage account</span></span>
    - <span data-ttu-id="44422-880">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="44422-880">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="44422-881">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-881">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="44422-882">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-882">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="44422-883">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="44422-883">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="44422-884">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="44422-884">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="44422-885">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="44422-885">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="44422-886">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="44422-886">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="44422-887">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="44422-887">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="44422-888">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="44422-888">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="44422-889">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="44422-889">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="44422-890">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="44422-890">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="44422-891">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="44422-891">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="44422-892">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="44422-892">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="44422-893">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="44422-893">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="44422-894">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="44422-894">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="44422-895">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="44422-895">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="44422-896">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="44422-896">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="44422-897">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="44422-897">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="44422-898">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="44422-898">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="44422-899">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="44422-899">Az.TrafficManager</span></span>
* <span data-ttu-id="44422-900">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="44422-900">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-901">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-901">Az.Websites</span></span>
* <span data-ttu-id="44422-902">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="44422-902">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="44422-903">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-903">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="44422-904">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="44422-904">Highlights since the last release</span></span>
* <span data-ttu-id="44422-905">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="44422-905">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-906">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-906">Az.Accounts</span></span>
* <span data-ttu-id="44422-907">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="44422-907">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-908">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-908">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-909">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="44422-909">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="44422-910">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="44422-910">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="44422-911">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-911">Az.Cdn</span></span>
* <span data-ttu-id="44422-912">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="44422-912">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-913">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-913">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-914">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="44422-914">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-915">Az.Compute</span></span>
* <span data-ttu-id="44422-916">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-916">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="44422-917">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="44422-917">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-918">Az.IotHub</span></span>
* <span data-ttu-id="44422-919">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-919">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="44422-920">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="44422-920">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="44422-921">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="44422-921">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="44422-922">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="44422-922">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="44422-923">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-923">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="44422-924">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="44422-924">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="44422-925">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="44422-925">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="44422-926">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="44422-926">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="44422-927">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-927">New cmdlets are:</span></span>
    - <span data-ttu-id="44422-928">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-928">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="44422-929">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-929">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="44422-930">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-930">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="44422-931">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-931">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="44422-932">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="44422-932">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-933">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-933">Az.KeyVault</span></span>
* <span data-ttu-id="44422-934">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="44422-934">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="44422-935">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="44422-935">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="44422-936">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="44422-936">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="44422-937">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="44422-937">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="44422-938">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="44422-938">Az.Maintenance</span></span>
* <span data-ttu-id="44422-939">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="44422-939">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-940">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-940">Az.Monitor</span></span>
* <span data-ttu-id="44422-941">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="44422-941">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="44422-942">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="44422-942">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="44422-943">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="44422-943">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="44422-944">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="44422-944">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="44422-945">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="44422-945">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="44422-946">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="44422-946">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="44422-947">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="44422-947">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="44422-948">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="44422-948">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-949">Az.Network</span></span>
* <span data-ttu-id="44422-950">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="44422-950">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="44422-951">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="44422-951">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="44422-952">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="44422-952">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="44422-953">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-953">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="44422-954">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-954">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="44422-955">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="44422-955">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="44422-956">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="44422-956">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="44422-957">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="44422-957">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="44422-958">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="44422-958">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="44422-959">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-959">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="44422-960">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="44422-960">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="44422-961">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="44422-961">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="44422-962">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="44422-962">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="44422-963">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="44422-963">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="44422-964">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="44422-964">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="44422-965">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="44422-965">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-966">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-966">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-967">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="44422-967">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="44422-968">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="44422-968">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-969">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-969">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-970">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="44422-970">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-971">Az.Sql</span></span>
* <span data-ttu-id="44422-972">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-972">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="44422-973">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="44422-973">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-974">Az.Storage</span></span>
* <span data-ttu-id="44422-975">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="44422-975">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="44422-976">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-976">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="44422-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-977">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="44422-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="44422-979">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="44422-979">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="44422-980">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="44422-980">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="44422-981">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="44422-981">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="44422-982">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="44422-982">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="44422-983">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="44422-983">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="44422-984">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="44422-984">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="44422-985">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="44422-985">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="44422-986">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="44422-986">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="44422-987">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="44422-987">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="44422-988">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-988">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="44422-989">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-989">General</span></span>
* <span data-ttu-id="44422-990">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="44422-990">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="44422-991">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="44422-991">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="44422-992">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="44422-992">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="44422-993">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="44422-993">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="44422-994">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="44422-994">Az.Billing</span></span>
  - <span data-ttu-id="44422-995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-995">Az.Compute</span></span>
  - <span data-ttu-id="44422-996">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="44422-996">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="44422-997">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-997">Az.EventHub</span></span>
  - <span data-ttu-id="44422-998">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-998">Az.IotHub</span></span>
  - <span data-ttu-id="44422-999">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-999">Az.KeyVault</span></span>
  - <span data-ttu-id="44422-1000">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1000">Az.Monitor</span></span>
  - <span data-ttu-id="44422-1001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1001">Az.Network</span></span>
  - <span data-ttu-id="44422-1002">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1002">Az.Resources</span></span>
  - <span data-ttu-id="44422-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1003">Az.Storage</span></span>
  - <span data-ttu-id="44422-1004">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-1004">Az.Websites</span></span>
* <span data-ttu-id="44422-1005">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-1005">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="44422-1006">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="44422-1006">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="44422-1007">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="44422-1007">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="44422-1008">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-1008">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-1009">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1009">Az.Accounts</span></span>
* <span data-ttu-id="44422-1010">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="44422-1010">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1011">Az.Compute</span></span>
* <span data-ttu-id="44422-1012">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="44422-1012">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="44422-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="44422-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="44422-1014">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="44422-1014">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="44422-1015">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="44422-1015">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="44422-1016">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="44422-1016">[#11354]</span></span>
* <span data-ttu-id="44422-1017">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="44422-1017">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="44422-1018">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="44422-1018">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="44422-1019">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="44422-1019">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="44422-1020">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="44422-1020">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="44422-1021">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="44422-1021">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="44422-1022">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-1022">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="44422-1023">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="44422-1023">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="44422-1024">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="44422-1024">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="44422-1025">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="44422-1025">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1026">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1026">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1027">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="44422-1027">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="44422-1028">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="44422-1028">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-1029">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-1029">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-1030">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="44422-1030">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="44422-1031">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="44422-1031">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-1032">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-1032">Az.HDInsight</span></span>
* <span data-ttu-id="44422-1033">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="44422-1033">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-1034">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-1034">Az.IotHub</span></span>
* <span data-ttu-id="44422-1035">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44422-1035">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="44422-1036">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-1036">New Cmdlets are:</span></span>
    - <span data-ttu-id="44422-1037">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="44422-1037">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="44422-1038">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="44422-1038">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-1039">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-1039">Az.KeyVault</span></span>
* <span data-ttu-id="44422-1040">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="44422-1040">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1041">Az.Monitor</span></span>
* <span data-ttu-id="44422-1042">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="44422-1042">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1043">Az.Network</span></span>
* <span data-ttu-id="44422-1044">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="44422-1044">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="44422-1045">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-1045">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="44422-1046">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="44422-1046">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="44422-1047">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="44422-1047">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="44422-1048">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="44422-1048">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="44422-1049">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="44422-1049">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-1050">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-1050">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-1051">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="44422-1051">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1053">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="44422-1053">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="44422-1054">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="44422-1054">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="44422-1055">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="44422-1055">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="44422-1056">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="44422-1056">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="44422-1057">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="44422-1057">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="44422-1058">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="44422-1058">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1059">Az.Resources</span></span>
* <span data-ttu-id="44422-1060">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="44422-1060">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="44422-1061">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="44422-1061">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="44422-1062">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="44422-1062">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="44422-1063">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-1063">Added example.</span></span>
* <span data-ttu-id="44422-1064">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="44422-1064">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="44422-1065">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="44422-1065">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1066">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1066">Az.Sql</span></span>
* <span data-ttu-id="44422-1067">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="44422-1067">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="44422-1068">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1068">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="44422-1069">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="44422-1069">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="44422-1070">Az.Support</span><span class="sxs-lookup"><span data-stu-id="44422-1070">Az.Support</span></span>
* <span data-ttu-id="44422-1071">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="44422-1071">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-1072">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-1072">Az.Websites</span></span>
* <span data-ttu-id="44422-1073">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="44422-1073">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="44422-1074">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="44422-1074">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="44422-1075">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="44422-1075">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="44422-1076">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="44422-1076">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="44422-1077">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="44422-1077">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="44422-1078">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-1078">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1079">Az.Accounts</span></span>
* <span data-ttu-id="44422-1080">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="44422-1080">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="44422-1081">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="44422-1081">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="44422-1082">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="44422-1082">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-1083">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-1083">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-1084">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="44422-1084">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="44422-1085">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="44422-1085">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="44422-1086">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="44422-1086">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="44422-1087">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="44422-1087">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-1088">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-1088">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-1089">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="44422-1089">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-1090">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-1090">Az.IotHub</span></span>
* <span data-ttu-id="44422-1091">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="44422-1091">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="44422-1092">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-1092">New Cmdlets are:</span></span>
    - <span data-ttu-id="44422-1093">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1093">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="44422-1094">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1094">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="44422-1095">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1095">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="44422-1096">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1096">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="44422-1097">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="44422-1097">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="44422-1098">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-1098">New Cmdlets are:</span></span>
    - <span data-ttu-id="44422-1099">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="44422-1099">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="44422-1100">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="44422-1100">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="44422-1101">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="44422-1101">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="44422-1102">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="44422-1102">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="44422-1103">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="44422-1103">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="44422-1104">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="44422-1104">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="44422-1105">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="44422-1105">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="44422-1106">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-1106">New Cmdlets are:</span></span>
    - <span data-ttu-id="44422-1107">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="44422-1107">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="44422-1108">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="44422-1108">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="44422-1109">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44422-1109">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1110">Az.Monitor</span></span>
* <span data-ttu-id="44422-1111">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="44422-1111">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1112">Az.Network</span></span>
* <span data-ttu-id="44422-1113">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="44422-1113">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="44422-1114">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="44422-1114">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="44422-1115">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="44422-1115">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="44422-1116">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="44422-1116">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1117">Az.Resources</span></span>
* <span data-ttu-id="44422-1118">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="44422-1118">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="44422-1119">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="44422-1119">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="44422-1120">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="44422-1120">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="44422-1121">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="44422-1121">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="44422-1122">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="44422-1122">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="44422-1123">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="44422-1123">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="44422-1124">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="44422-1124">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="44422-1125">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="44422-1125">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="44422-1126">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="44422-1126">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="44422-1127">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="44422-1127">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="44422-1128">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="44422-1128">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="44422-1129">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1129">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="44422-1130">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="44422-1130">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="44422-1131">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="44422-1131">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1132">Az.Sql</span></span>
* <span data-ttu-id="44422-1133">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="44422-1133">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="44422-1134">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="44422-1134">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="44422-1135">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="44422-1135">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="44422-1136">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="44422-1136">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="44422-1137">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="44422-1137">Remove an LTR backup</span></span>
    - <span data-ttu-id="44422-1138">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="44422-1138">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="44422-1139">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="44422-1139">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="44422-1140">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="44422-1140">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="44422-1141">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1141">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1142">Az.Storage</span></span>
* <span data-ttu-id="44422-1143">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-1143">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="44422-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="44422-1145">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="44422-1145">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="44422-1146">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="44422-1146">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="44422-1147">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="44422-1147">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-1148">Az.Websites</span></span>
* <span data-ttu-id="44422-1149">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="44422-1149">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="44422-1150">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="44422-1150">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="44422-1151">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="44422-1151">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="44422-1152">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="44422-1152">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="44422-1153">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="44422-1153">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="44422-1154">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-1154">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="44422-1155">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="44422-1155">Highlights since the last major release</span></span>
* <span data-ttu-id="44422-1156">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="44422-1156">Updated client side telemetry.</span></span>
* <span data-ttu-id="44422-1157">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="44422-1157">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="44422-1158">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="44422-1158">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-1159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1159">Az.Accounts</span></span>
* <span data-ttu-id="44422-1160">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="44422-1160">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-1161">Az.Automation</span></span>
* <span data-ttu-id="44422-1162">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="44422-1162">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-1163">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-1163">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-1164">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="44422-1164">Updated SDK to 7.0</span></span>
* <span data-ttu-id="44422-1165">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="44422-1165">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1166">Az.Compute</span></span>
* <span data-ttu-id="44422-1167">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="44422-1167">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-1168">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-1168">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-1169">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="44422-1169">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-1170">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-1170">Az.IotHub</span></span>
* <span data-ttu-id="44422-1171">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="44422-1171">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="44422-1172">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-1172">New Cmdlets are:</span></span>
    - <span data-ttu-id="44422-1173">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1173">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="44422-1174">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1174">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="44422-1175">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1175">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="44422-1176">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="44422-1176">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-1177">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-1177">Az.KeyVault</span></span>
* <span data-ttu-id="44422-1178">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="44422-1178">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-1179">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1179">Az.Monitor</span></span>
* <span data-ttu-id="44422-1180">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="44422-1180">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="44422-1181">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="44422-1181">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="44422-1182">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="44422-1182">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1183">Az.Network</span></span>
* <span data-ttu-id="44422-1184">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="44422-1184">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="44422-1185">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="44422-1185">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="44422-1186">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="44422-1186">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="44422-1187">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="44422-1187">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="44422-1188">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-1188">No new cmdlets are added.</span></span> <span data-ttu-id="44422-1189">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="44422-1189">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1190">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1190">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1191">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="44422-1191">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1192">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1192">Az.Resources</span></span>
* <span data-ttu-id="44422-1193">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="44422-1193">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="44422-1194">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="44422-1194">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="44422-1195">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="44422-1195">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="44422-1196">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="44422-1196">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="44422-1197">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="44422-1197">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="44422-1198">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="44422-1198">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="44422-1199">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="44422-1199">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="44422-1200">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-1200">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1201">Az.Sql</span></span>
* <span data-ttu-id="44422-1202">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="44422-1202">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="44422-1203">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="44422-1203">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="44422-1204">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="44422-1204">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="44422-1205">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="44422-1205">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="44422-1206">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="44422-1206">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="44422-1207">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="44422-1207">Az.StorageSync</span></span>
* <span data-ttu-id="44422-1208">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="44422-1208">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="44422-1209">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-1209">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="44422-1210">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="44422-1210">Highlights since the last major release</span></span>
* <span data-ttu-id="44422-1211">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="44422-1211">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="44422-1212">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1212">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-1213">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1213">Az.Accounts</span></span>
* <span data-ttu-id="44422-1214">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="44422-1214">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="44422-1215">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="44422-1215">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-1216">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-1216">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-1217">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="44422-1217">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="44422-1218">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="44422-1218">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="44422-1219">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="44422-1219">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="44422-1220">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="44422-1220">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1221">Az.Compute</span></span>
* <span data-ttu-id="44422-1222">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="44422-1222">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="44422-1223">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="44422-1223">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="44422-1224">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="44422-1224">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="44422-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="44422-1226">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="44422-1226">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1227">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1228">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="44422-1228">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="44422-1229">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="44422-1229">Az.DeploymentManager</span></span>
* <span data-ttu-id="44422-1230">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="44422-1230">Adds LIST operations for resources</span></span>
* <span data-ttu-id="44422-1231">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="44422-1231">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-1232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-1232">Az.HDInsight</span></span>
* <span data-ttu-id="44422-1233">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="44422-1233">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-1234">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-1234">Az.KeyVault</span></span>
* <span data-ttu-id="44422-1235">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="44422-1235">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1236">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1236">Az.Network</span></span>
* <span data-ttu-id="44422-1237">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="44422-1237">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="44422-1238">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="44422-1238">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="44422-1239">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="44422-1239">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="44422-1240">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="44422-1240">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="44422-1241">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="44422-1241">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="44422-1242">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="44422-1242">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="44422-1243">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="44422-1243">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="44422-1244">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="44422-1244">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="44422-1245">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-1245">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="44422-1247">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-1247">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="44422-1248">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="44422-1248">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="44422-1249">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="44422-1249">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-1250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-1250">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-1251">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="44422-1251">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="44422-1252">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="44422-1252">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="44422-1253">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="44422-1253">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="44422-1254">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="44422-1254">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1255">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1256">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="44422-1256">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="44422-1257">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="44422-1257">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1258">Az.Resources</span></span>
* <span data-ttu-id="44422-1259">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="44422-1259">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="44422-1260">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="44422-1260">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1261">Az.Sql</span></span>
<span data-ttu-id="44422-1262">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="44422-1262">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1263">Az.Storage</span></span>
* <span data-ttu-id="44422-1264">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-1264">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="44422-1265">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-1265">New-AzStorageAccount</span></span>
* <span data-ttu-id="44422-1266">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="44422-1266">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="44422-1267">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="44422-1267">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-1268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-1268">Az.Websites</span></span>
* <span data-ttu-id="44422-1269">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="44422-1269">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="44422-1270">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="44422-1270">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="44422-1271">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="44422-1271">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1272">Az.Accounts</span></span>
* <span data-ttu-id="44422-1273">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="44422-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="44422-1274">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-1274">Az.Cdn</span></span>
* <span data-ttu-id="44422-1275">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="44422-1275">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1276">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1276">Az.Compute</span></span>
* <span data-ttu-id="44422-1277">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="44422-1277">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="44422-1278">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="44422-1278">Az.ContainerInstance</span></span>
* <span data-ttu-id="44422-1279">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="44422-1279">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="44422-1280">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="44422-1280">Az.DataBoxEdge</span></span>
* <span data-ttu-id="44422-1281">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="44422-1281">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="44422-1282">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="44422-1282">Get the Edge Storage Container</span></span>
* <span data-ttu-id="44422-1283">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="44422-1283">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="44422-1284">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="44422-1284">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="44422-1285">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="44422-1285">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="44422-1286">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="44422-1286">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="44422-1287">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="44422-1287">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="44422-1288">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="44422-1288">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="44422-1289">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-1289">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="44422-1290">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="44422-1290">Get the Edge Storage Account</span></span>
* <span data-ttu-id="44422-1291">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-1291">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="44422-1292">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="44422-1292">Create new Edge Storage Account</span></span>
* <span data-ttu-id="44422-1293">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="44422-1293">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="44422-1294">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="44422-1294">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="44422-1295">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="44422-1295">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="44422-1296">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="44422-1296">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="44422-1297">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="44422-1297">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="44422-1298">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="44422-1298">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1299">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1299">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1300">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="44422-1300">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="44422-1301">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="44422-1301">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="44422-1302">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="44422-1302">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="44422-1303">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="44422-1303">Az.DevTestLabs</span></span>
* <span data-ttu-id="44422-1304">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="44422-1304">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-1305">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-1305">Az.EventHub</span></span>
* <span data-ttu-id="44422-1306">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="44422-1306">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-1307">Az.HDInsight</span></span>
* <span data-ttu-id="44422-1308">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="44422-1308">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="44422-1309">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="44422-1309">Az.MachineLearning</span></span>
* <span data-ttu-id="44422-1310">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="44422-1310">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="44422-1311">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="44422-1311">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="44422-1312">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="44422-1312">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="44422-1313">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="44422-1313">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="44422-1314">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="44422-1314">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="44422-1315">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="44422-1315">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="44422-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="44422-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="44422-1317">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="44422-1317">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1318">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1318">Az.Network</span></span>
* <span data-ttu-id="44422-1319">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="44422-1319">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1320">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1320">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1321">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1321">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="44422-1322">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1322">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="44422-1323">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1323">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="44422-1324">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1324">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1325">Az.Resources</span></span>
* <span data-ttu-id="44422-1326">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="44422-1326">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1327">Az.Sql</span></span>
* <span data-ttu-id="44422-1328">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="44422-1328">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="44422-1329">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="44422-1329">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="44422-1330">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="44422-1330">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="44422-1331">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="44422-1331">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1332">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1332">Az.Storage</span></span>
* <span data-ttu-id="44422-1333">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="44422-1333">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="44422-1334">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-1334">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="44422-1335">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="44422-1335">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="44422-1336">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-1336">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="44422-1337">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-1337">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="44422-1338">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-1338">General</span></span>
* <span data-ttu-id="44422-1339">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="44422-1339">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1340">Az.Accounts</span></span>
* <span data-ttu-id="44422-1341">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="44422-1341">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="44422-1342">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="44422-1342">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="44422-1343">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-1343">Az.Batch</span></span>
* <span data-ttu-id="44422-1344">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="44422-1344">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1345">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1346">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="44422-1346">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-1347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-1347">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-1348">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="44422-1348">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="44422-1349">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="44422-1349">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="44422-1350">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="44422-1350">Az.HealthcareApis</span></span>
* <span data-ttu-id="44422-1351">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="44422-1351">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-1352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-1352">Az.KeyVault</span></span>
* <span data-ttu-id="44422-1353">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="44422-1353">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="44422-1354">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="44422-1354">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="44422-1355">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="44422-1355">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-1356">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1356">Az.Monitor</span></span>
* <span data-ttu-id="44422-1357">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="44422-1357">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="44422-1358">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="44422-1358">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="44422-1359">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="44422-1359">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1360">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1360">Az.Network</span></span>
* <span data-ttu-id="44422-1361">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="44422-1361">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1362">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1362">Az.Resources</span></span>
* <span data-ttu-id="44422-1363">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="44422-1363">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="44422-1364">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="44422-1364">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1365">Az.Sql</span></span>
* <span data-ttu-id="44422-1366">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="44422-1366">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1367">Az.Storage</span></span>
* <span data-ttu-id="44422-1368">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="44422-1368">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="44422-1369">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="44422-1369">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="44422-1370">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="44422-1370">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="44422-1371">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="44422-1371">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="44422-1372">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="44422-1372">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="44422-1373">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="44422-1373">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="44422-1374">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="44422-1374">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="44422-1375">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-1375">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="44422-1376">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-1376">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="44422-1377">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="44422-1377">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="44422-1378">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="44422-1378">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="44422-1379">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="44422-1379">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="44422-1380">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="44422-1380">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="44422-1381">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-1381">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="44422-1382">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="44422-1382">Highlights since the last major release</span></span>
* <span data-ttu-id="44422-1383">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="44422-1383">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="44422-1384">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="44422-1384">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1385">Az.Compute</span></span>
* <span data-ttu-id="44422-1386">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="44422-1386">VM Reapply feature</span></span>
    - <span data-ttu-id="44422-1387">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="44422-1387">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="44422-1388">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="44422-1388">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="44422-1389">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-1389">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="44422-1390">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="44422-1390">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="44422-1391">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-1391">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="44422-1392">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="44422-1392">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="44422-1393">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="44422-1393">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="44422-1394">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="44422-1394">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="44422-1395">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="44422-1395">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="44422-1396">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-1396">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="44422-1397">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="44422-1397">Az.DataBoxEdge</span></span>
* <span data-ttu-id="44422-1398">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1398">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="44422-1399">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="44422-1399">Get the Order</span></span>
* <span data-ttu-id="44422-1400">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1400">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="44422-1401">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="44422-1401">Create new Order</span></span>
* <span data-ttu-id="44422-1402">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1402">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="44422-1403">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="44422-1403">Remove the Order</span></span>
* <span data-ttu-id="44422-1404">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="44422-1404">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="44422-1405">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="44422-1405">Now creates Local Share</span></span>
* <span data-ttu-id="44422-1406">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1406">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="44422-1407">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="44422-1407">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="44422-1408">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1408">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="44422-1409">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="44422-1409">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="44422-1410">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1410">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="44422-1411">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="44422-1411">Gets the information about Triggers</span></span>
* <span data-ttu-id="44422-1412">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1412">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="44422-1413">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="44422-1413">Create new Triggers</span></span>
* <span data-ttu-id="44422-1414">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1414">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="44422-1415">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="44422-1415">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1416">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1416">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1417">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="44422-1417">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="44422-1418">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="44422-1418">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-1419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-1419">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-1420">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="44422-1420">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-1421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-1421">Az.EventHub</span></span>
* <span data-ttu-id="44422-1422">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="44422-1422">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-1423">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-1423">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-1424">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="44422-1424">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="44422-1425">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="44422-1425">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="44422-1426">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="44422-1426">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="44422-1427">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="44422-1427">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1428">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1428">Az.Network</span></span>
* <span data-ttu-id="44422-1429">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="44422-1429">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="44422-1430">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="44422-1430">Az.PrivateDns</span></span>
* <span data-ttu-id="44422-1431">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="44422-1431">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1432">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1433">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="44422-1433">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="44422-1434">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="44422-1434">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="44422-1435">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="44422-1435">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="44422-1436">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="44422-1436">Az.RedisCache</span></span>
* <span data-ttu-id="44422-1437">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="44422-1437">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="44422-1438">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="44422-1438">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="44422-1439">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="44422-1439">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1440">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1440">Az.Resources</span></span>
- <span data-ttu-id="44422-1441">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="44422-1441">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="44422-1442">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="44422-1442">Updated create policy definition help example</span></span>
- <span data-ttu-id="44422-1443">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="44422-1443">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="44422-1444">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="44422-1444">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="44422-1445">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="44422-1445">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1446">Az.Sql</span></span>
* <span data-ttu-id="44422-1447">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-1447">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="44422-1448">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="44422-1448">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="44422-1449">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-1449">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="44422-1450">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-1450">General</span></span>
* <span data-ttu-id="44422-1451">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="44422-1451">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1452">Az.Accounts</span></span>
* <span data-ttu-id="44422-1453">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="44422-1453">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="44422-1454">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="44422-1454">Az.Advisor</span></span>
* <span data-ttu-id="44422-1455">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44422-1455">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="44422-1456">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-1456">Az.Batch</span></span>
* <span data-ttu-id="44422-1457">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="44422-1457">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="44422-1458">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="44422-1458">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="44422-1459">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="44422-1459">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="44422-1460">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="44422-1460">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="44422-1461">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="44422-1461">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="44422-1462">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="44422-1462">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="44422-1463">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="44422-1463">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="44422-1464">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="44422-1464">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="44422-1465">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="44422-1465">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="44422-1466">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="44422-1466">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="44422-1467">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="44422-1467">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="44422-1468">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="44422-1468">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="44422-1469">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="44422-1469">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="44422-1470">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="44422-1470">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="44422-1471">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="44422-1471">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="44422-1472">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="44422-1472">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="44422-1473">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="44422-1473">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="44422-1474">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="44422-1474">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="44422-1475">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="44422-1475">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="44422-1476">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="44422-1476">This operation is no longer supported.</span></span>
* <span data-ttu-id="44422-1477">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="44422-1477">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="44422-1478">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="44422-1478">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="44422-1479">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="44422-1479">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="44422-1480">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="44422-1480">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="44422-1481">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku** , mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="44422-1481">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="44422-1482">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="44422-1482">New non-verified images are also now returned.</span></span> <span data-ttu-id="44422-1483">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="44422-1483">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="44422-1484">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="44422-1484">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="44422-1485">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="44422-1485">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="44422-1486">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="44422-1486">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="44422-1487">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="44422-1487">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="44422-1488">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="44422-1488">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="44422-1489">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="44422-1489">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="44422-1490">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="44422-1490">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="44422-1491">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="44422-1491">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="44422-1492">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="44422-1492">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="44422-1493">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-1493">Az.Cdn</span></span>
* <span data-ttu-id="44422-1494">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="44422-1494">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="44422-1495">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="44422-1495">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1496">Az.Compute</span></span>
* <span data-ttu-id="44422-1497">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="44422-1497">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="44422-1498">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="44422-1498">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="44422-1499">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="44422-1499">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="44422-1500">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1500">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="44422-1501">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1501">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="44422-1502">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="44422-1502">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="44422-1503">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-1503">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="44422-1504">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="44422-1504">Breaking changes</span></span>
    - <span data-ttu-id="44422-1505">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="44422-1505">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="44422-1506">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="44422-1506">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1507">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1507">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1508">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="44422-1508">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-1509">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-1509">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-1510">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="44422-1510">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="44422-1511">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="44422-1511">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="44422-1512">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="44422-1512">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="44422-1513">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="44422-1513">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="44422-1514">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="44422-1514">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="44422-1515">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="44422-1515">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-1516">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-1516">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-1517">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="44422-1517">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-1518">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-1518">Az.HDInsight</span></span>
* <span data-ttu-id="44422-1519">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="44422-1519">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="44422-1520">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="44422-1520">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="44422-1521">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="44422-1521">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="44422-1522">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="44422-1522">Removed five cmdlets:</span></span>
    - <span data-ttu-id="44422-1523">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="44422-1523">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="44422-1524">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="44422-1524">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="44422-1525">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="44422-1525">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="44422-1526">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="44422-1526">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="44422-1527">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="44422-1527">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="44422-1528">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-1528">Added three cmdlets:</span></span>
    - <span data-ttu-id="44422-1529">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="44422-1529">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="44422-1530">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="44422-1530">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="44422-1531">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="44422-1531">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="44422-1532">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="44422-1532">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="44422-1533">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="44422-1533">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="44422-1534">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="44422-1534">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="44422-1535">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="44422-1535">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="44422-1536">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="44422-1536">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="44422-1537">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="44422-1537">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="44422-1538">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="44422-1538">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="44422-1539">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="44422-1539">Added some scenario test cases.</span></span>
* <span data-ttu-id="44422-1540">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="44422-1540">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-1541">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-1541">Az.IotHub</span></span>
* <span data-ttu-id="44422-1542">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="44422-1542">Breaking changes:</span></span>
    - <span data-ttu-id="44422-1543">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="44422-1543">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="44422-1544">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="44422-1544">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="44422-1545">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="44422-1545">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="44422-1546">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="44422-1546">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="44422-1547">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="44422-1547">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="44422-1548">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="44422-1548">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="44422-1549">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="44422-1549">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="44422-1550">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="44422-1550">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="44422-1551">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="44422-1551">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="44422-1552">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="44422-1552">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="44422-1553">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="44422-1553">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="44422-1554">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="44422-1554">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1555">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1556">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1556">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="44422-1557">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1557">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="44422-1558">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1558">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="44422-1559">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1559">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="44422-1560">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1560">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="44422-1561">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1561">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="44422-1562">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1562">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="44422-1563">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-1563">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="44422-1564">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="44422-1564">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1565">Az.Resources</span></span>
* <span data-ttu-id="44422-1566">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="44422-1566">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1567">Az.Network</span></span>
* <span data-ttu-id="44422-1568">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="44422-1568">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="44422-1569">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="44422-1569">Updated cmdlet:</span></span>
        - <span data-ttu-id="44422-1570">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1570">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1571">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1571">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1572">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1572">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1573">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1573">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1574">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1574">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="44422-1575">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="44422-1575">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="44422-1576">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="44422-1576">New cmdlet:</span></span>
        - <span data-ttu-id="44422-1577">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="44422-1577">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="44422-1578">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="44422-1578">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="44422-1579">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="44422-1579">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="44422-1580">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1580">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="44422-1581">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="44422-1581">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="44422-1582">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="44422-1582">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="44422-1583">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-1583">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="44422-1584">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="44422-1584">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="44422-1585">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-1585">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-1586">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="44422-1586">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="44422-1587">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="44422-1587">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="44422-1588">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="44422-1588">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="44422-1589">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="44422-1589">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="44422-1590">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="44422-1590">Set-AzVirtualHub</span></span>
* <span data-ttu-id="44422-1591">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="44422-1591">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="44422-1592">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="44422-1592">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="44422-1593">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1593">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="44422-1594">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1594">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="44422-1595">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1595">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="44422-1596">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1596">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="44422-1597">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1597">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="44422-1598">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-1598">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-1599">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1599">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="44422-1600">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="44422-1600">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="44422-1601">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1601">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="44422-1602">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1602">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="44422-1603">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1603">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="44422-1604">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1604">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="44422-1605">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-1605">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="44422-1606">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="44422-1606">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="44422-1607">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-1607">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-1608">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="44422-1608">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="44422-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="44422-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="44422-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="44422-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="44422-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="44422-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="44422-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="44422-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="44422-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="44422-1614">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="44422-1614">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="44422-1615">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-1615">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="44422-1616">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="44422-1616">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="44422-1617">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="44422-1617">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="44422-1618">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="44422-1618">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="44422-1619">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="44422-1619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="44422-1620">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-1620">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="44422-1621">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-1621">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="44422-1622">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="44422-1622">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="44422-1623">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-1623">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="44422-1624">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="44422-1624">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="44422-1625">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-1625">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-1626">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="44422-1626">New-AzIpGroup</span></span>
        - <span data-ttu-id="44422-1627">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="44422-1627">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="44422-1628">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="44422-1628">Get-AzIpGroup</span></span>
        - <span data-ttu-id="44422-1629">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="44422-1629">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-1630">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-1630">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-1631">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="44422-1631">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1632">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1632">Az.Sql</span></span>
* <span data-ttu-id="44422-1633">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="44422-1633">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="44422-1634">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="44422-1634">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="44422-1635">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="44422-1635">Removed deprecated aliases:</span></span>
* <span data-ttu-id="44422-1636">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="44422-1636">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="44422-1637">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="44422-1637">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="44422-1638">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-1638">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="44422-1639">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="44422-1639">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="44422-1640">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="44422-1640">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="44422-1641">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="44422-1641">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1642">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1642">Az.Storage</span></span>
* <span data-ttu-id="44422-1643">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-1643">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="44422-1644">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-1644">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="44422-1645">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-1645">Set-AzStorageAccount</span></span>
* <span data-ttu-id="44422-1646">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="44422-1646">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="44422-1647">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="44422-1647">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="44422-1648">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="44422-1648">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="44422-1649">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-1649">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="44422-1650">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-1650">General</span></span>
* <span data-ttu-id="44422-1651">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="44422-1651">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-1652">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1652">Az.Accounts</span></span>
* <span data-ttu-id="44422-1653">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="44422-1653">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-1654">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-1654">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-1655">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="44422-1655">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="44422-1656">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="44422-1656">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-1657">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-1657">Az.Automation</span></span>
* <span data-ttu-id="44422-1658">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="44422-1658">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="44422-1659">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-1659">Az.Batch</span></span>
* <span data-ttu-id="44422-1660">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="44422-1660">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1661">Az.Compute</span></span>
* <span data-ttu-id="44422-1662">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-1662">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="44422-1663">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="44422-1663">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="44422-1664">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="44422-1664">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="44422-1665">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="44422-1665">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1666">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1666">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1667">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="44422-1667">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="44422-1668">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="44422-1668">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="44422-1669">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="44422-1669">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-1670">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-1670">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-1671">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="44422-1671">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="44422-1672">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="44422-1672">Az.HealthcareApis</span></span>
* <span data-ttu-id="44422-1673">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="44422-1673">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="44422-1674">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="44422-1674">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="44422-1675">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="44422-1675">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="44422-1676">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="44422-1676">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-1677">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-1677">Az.IotHub</span></span>
* <span data-ttu-id="44422-1678">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="44422-1678">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="44422-1679">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="44422-1679">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1680">Az.Monitor</span></span>
* <span data-ttu-id="44422-1681">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="44422-1681">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="44422-1682">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="44422-1682">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="44422-1683">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="44422-1683">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="44422-1684">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="44422-1684">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1685">Az.Network</span></span>
* <span data-ttu-id="44422-1686">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="44422-1686">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="44422-1687">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="44422-1687">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="44422-1688">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-1688">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-1689">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-1689">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="44422-1690">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1690">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="44422-1691">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="44422-1691">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="44422-1692">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="44422-1692">Updated cmdlets:</span></span>
        - <span data-ttu-id="44422-1693">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1693">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="44422-1694">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1694">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="44422-1695">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1695">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="44422-1696">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="44422-1696">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="44422-1697">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="44422-1697">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="44422-1698">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="44422-1698">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="44422-1699">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="44422-1699">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="44422-1700">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="44422-1700">Az.RedisCache</span></span>
* <span data-ttu-id="44422-1701">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="44422-1701">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1702">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1702">Az.Sql</span></span>
* <span data-ttu-id="44422-1703">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="44422-1703">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1704">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1704">Az.Storage</span></span>
* <span data-ttu-id="44422-1705">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="44422-1705">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="44422-1706">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="44422-1706">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="44422-1707">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="44422-1707">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="44422-1708">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="44422-1708">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="44422-1709">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-1709">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="44422-1710">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="44422-1710">Az.StorageSync</span></span>
* <span data-ttu-id="44422-1711">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="44422-1711">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-1712">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-1712">Az.Websites</span></span>
* <span data-ttu-id="44422-1713">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="44422-1713">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="44422-1714">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-1714">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="44422-1715">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-1715">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-1716">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-1716">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="44422-1717">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="44422-1717">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="44422-1718">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="44422-1718">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-1719">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-1719">Az.Automation</span></span>
* <span data-ttu-id="44422-1720">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="44422-1720">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="44422-1721">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="44422-1721">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="44422-1722">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="44422-1722">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1723">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1723">Az.Compute</span></span>
* <span data-ttu-id="44422-1724">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1724">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="44422-1725">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1725">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="44422-1726">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="44422-1726">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="44422-1727">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="44422-1727">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="44422-1728">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="44422-1728">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="44422-1729">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="44422-1729">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="44422-1730">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="44422-1730">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="44422-1731">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="44422-1731">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="44422-1732">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="44422-1732">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1733">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1733">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1734">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="44422-1734">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="44422-1735">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="44422-1735">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-1736">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-1736">Az.HDInsight</span></span>
* <span data-ttu-id="44422-1737">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="44422-1737">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-1738">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-1738">Az.IotHub</span></span>
* <span data-ttu-id="44422-1739">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="44422-1739">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="44422-1740">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="44422-1740">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="44422-1741">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="44422-1741">New cmdlets are:</span></span>
    - <span data-ttu-id="44422-1742">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="44422-1742">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="44422-1743">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="44422-1743">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="44422-1744">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="44422-1744">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="44422-1745">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="44422-1745">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-1746">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1746">Az.Monitor</span></span>
* <span data-ttu-id="44422-1747">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="44422-1747">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="44422-1748">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="44422-1748">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="44422-1749">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="44422-1749">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="44422-1750">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019** , antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="44422-1750">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="44422-1751">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="44422-1751">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="44422-1752">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="44422-1752">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="44422-1753">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="44422-1753">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="44422-1754">**OBSERVAÇÃO** : é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="44422-1754">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="44422-1755">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource** ) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="44422-1755">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="44422-1756">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="44422-1756">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="44422-1757">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource** ) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="44422-1757">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="44422-1758">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="44422-1758">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="44422-1759">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="44422-1759">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="44422-1760">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="44422-1760">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="44422-1761">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="44422-1761">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="44422-1762">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="44422-1762">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="44422-1763">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="44422-1763">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="44422-1764">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-1764">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="44422-1765">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="44422-1765">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="44422-1766">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-1766">Overall improved help files</span></span>
* <span data-ttu-id="44422-1767">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="44422-1767">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1768">Az.Network</span></span>
* <span data-ttu-id="44422-1769">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="44422-1769">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="44422-1770">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="44422-1770">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="44422-1771">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="44422-1771">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="44422-1772">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="44422-1772">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="44422-1773">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="44422-1773">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="44422-1774">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="44422-1774">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="44422-1775">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="44422-1775">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="44422-1776">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44422-1776">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="44422-1777">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-1777">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="44422-1778">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="44422-1778">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="44422-1779">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-1779">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="44422-1780">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="44422-1780">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="44422-1781">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="44422-1781">New cmdlets</span></span>
        - <span data-ttu-id="44422-1782">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="44422-1782">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="44422-1783">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1783">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="44422-1784">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="44422-1784">Updated cmdlet:</span></span>
        - <span data-ttu-id="44422-1785">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="44422-1785">New-VpnSite</span></span>
        - <span data-ttu-id="44422-1786">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="44422-1786">Update-VpnSite</span></span>
        - <span data-ttu-id="44422-1787">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1787">New-VpnConnection</span></span>
        - <span data-ttu-id="44422-1788">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1788">Update-VpnConnection</span></span>
* <span data-ttu-id="44422-1789">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="44422-1789">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1791">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="44422-1791">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="44422-1792">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="44422-1792">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1793">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1793">Az.Resources</span></span>
* <span data-ttu-id="44422-1794">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="44422-1794">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-1795">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-1795">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-1796">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="44422-1796">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="44422-1797">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="44422-1797">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="44422-1798">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="44422-1798">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="44422-1799">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="44422-1799">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="44422-1800">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="44422-1800">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="44422-1801">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="44422-1801">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="44422-1802">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="44422-1802">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="44422-1803">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="44422-1803">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="44422-1804">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="44422-1804">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="44422-1805">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="44422-1805">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="44422-1806">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="44422-1806">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="44422-1807">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="44422-1807">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="44422-1808">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="44422-1808">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="44422-1809">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="44422-1809">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="44422-1810">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="44422-1810">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="44422-1811">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="44422-1811">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="44422-1812">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="44422-1812">Az.SignalR</span></span>
* <span data-ttu-id="44422-1813">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="44422-1813">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1814">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1814">Az.Sql</span></span>
* <span data-ttu-id="44422-1815">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="44422-1815">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="44422-1816">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="44422-1816">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="44422-1817">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-1817">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="44422-1818">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="44422-1818">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="44422-1819">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="44422-1819">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1820">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1820">Az.Storage</span></span>
* <span data-ttu-id="44422-1821">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="44422-1821">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="44422-1822">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="44422-1822">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="44422-1823">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="44422-1823">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="44422-1824">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="44422-1824">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="44422-1825">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="44422-1825">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="44422-1826">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="44422-1826">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="44422-1827">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="44422-1827">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="44422-1828">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-1828">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="44422-1829">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-1829">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="44422-1830">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-1830">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="44422-1831">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="44422-1831">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-1832">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-1832">Az.Websites</span></span>
* <span data-ttu-id="44422-1833">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="44422-1833">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="44422-1834">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="44422-1834">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="44422-1835">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="44422-1835">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="44422-1836">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-1836">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="44422-1837">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-1837">General</span></span>
* <span data-ttu-id="44422-1838">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="44422-1838">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1839">Az.Accounts</span></span>
* <span data-ttu-id="44422-1840">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="44422-1840">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="44422-1841">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="44422-1841">Az.Aks</span></span>
* <span data-ttu-id="44422-1842">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="44422-1842">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="44422-1843">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="44422-1843">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-1844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-1844">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-1845">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="44422-1845">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="44422-1846">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="44422-1846">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="44422-1847">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="44422-1847">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="44422-1848">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="44422-1848">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="44422-1849">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="44422-1849">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="44422-1850">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-1850">Az.Batch</span></span>
* <span data-ttu-id="44422-1851">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="44422-1851">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="44422-1852">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-1852">Az.Cdn</span></span>
* <span data-ttu-id="44422-1853">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="44422-1853">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1854">Az.Compute</span></span>
* <span data-ttu-id="44422-1855">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1855">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="44422-1856">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-1856">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="44422-1857">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="44422-1857">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="44422-1858">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="44422-1858">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="44422-1859">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="44422-1859">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="44422-1860">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="44422-1860">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="44422-1861">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="44422-1861">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="44422-1862">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="44422-1862">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1863">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1863">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1864">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="44422-1864">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="44422-1865">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="44422-1865">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="44422-1866">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="44422-1866">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="44422-1867">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="44422-1867">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-1868">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-1868">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-1869">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="44422-1869">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-1870">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-1870">Az.EventHub</span></span>
* <span data-ttu-id="44422-1871">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-1871">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="44422-1872">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="44422-1872">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="44422-1873">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="44422-1873">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="44422-1874">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="44422-1874">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="44422-1875">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="44422-1875">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="44422-1876">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="44422-1876">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-1877">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-1877">Az.Monitor</span></span>
* <span data-ttu-id="44422-1878">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-1878">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1879">Az.Network</span></span>
* <span data-ttu-id="44422-1880">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1880">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="44422-1881">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="44422-1881">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="44422-1882">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="44422-1882">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="44422-1883">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="44422-1883">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="44422-1884">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="44422-1884">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="44422-1885">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="44422-1885">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="44422-1886">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="44422-1886">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-1888">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="44422-1888">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="44422-1889">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="44422-1889">Added example</span></span>
    - <span data-ttu-id="44422-1890">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="44422-1890">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="44422-1891">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="44422-1891">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="44422-1892">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="44422-1892">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1893">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1893">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1894">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1894">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1895">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1895">Az.Resources</span></span>
* <span data-ttu-id="44422-1896">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="44422-1896">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="44422-1897">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="44422-1897">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="44422-1898">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="44422-1898">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="44422-1899">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-1899">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="44422-1900">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="44422-1900">Az.ServiceBus</span></span>
* <span data-ttu-id="44422-1901">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-1901">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="44422-1902">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="44422-1902">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="44422-1903">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="44422-1903">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-1904">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-1904">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-1905">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="44422-1905">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="44422-1906">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="44422-1906">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="44422-1907">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="44422-1907">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="44422-1908">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="44422-1908">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="44422-1909">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="44422-1909">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="44422-1910">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="44422-1910">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1911">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1911">Az.Sql</span></span>
* <span data-ttu-id="44422-1912">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="44422-1912">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-1913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-1913">Az.Storage</span></span>
* <span data-ttu-id="44422-1914">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="44422-1914">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="44422-1915">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="44422-1915">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="44422-1916">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="44422-1916">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="44422-1917">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="44422-1917">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="44422-1918">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="44422-1918">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="44422-1919">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="44422-1919">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-1920">Az.Websites</span></span>
* <span data-ttu-id="44422-1921">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44422-1921">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="44422-1922">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-1922">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-1923">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-1923">Az.Accounts</span></span>
* <span data-ttu-id="44422-1924">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="44422-1924">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="44422-1925">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="44422-1925">Az.ApplicationInsights</span></span>
* <span data-ttu-id="44422-1926">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="44422-1926">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-1927">Az.Automation</span></span>
* <span data-ttu-id="44422-1928">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="44422-1928">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-1929">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-1929">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-1930">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="44422-1930">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-1931">Az.Compute</span></span>
* <span data-ttu-id="44422-1932">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="44422-1932">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="44422-1933">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="44422-1933">Az.ContainerRegistry</span></span>
* <span data-ttu-id="44422-1934">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="44422-1934">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="44422-1935">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="44422-1935">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-1936">Az.DataFactory</span></span>
* <span data-ttu-id="44422-1937">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-1937">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="44422-1938">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="44422-1938">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-1939">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-1939">Az.EventHub</span></span>
* <span data-ttu-id="44422-1940">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="44422-1940">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="44422-1941">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="44422-1941">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-1942">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-1942">Az.KeyVault</span></span>
* <span data-ttu-id="44422-1943">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="44422-1943">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="44422-1944">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="44422-1944">Az.LogicApp</span></span>
* <span data-ttu-id="44422-1945">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="44422-1945">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="44422-1946">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="44422-1946">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="44422-1947">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="44422-1947">Az.ManagedServices</span></span>
* <span data-ttu-id="44422-1948">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="44422-1948">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-1949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-1949">Az.Network</span></span>
* <span data-ttu-id="44422-1950">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="44422-1950">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="44422-1951">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="44422-1951">New cmdlets</span></span>
        - <span data-ttu-id="44422-1952">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44422-1952">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="44422-1953">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="44422-1953">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="44422-1954">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1954">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1955">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1955">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1956">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1956">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1957">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1957">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="44422-1958">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="44422-1958">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="44422-1959">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="44422-1959">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="44422-1960">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="44422-1960">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="44422-1961">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="44422-1961">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="44422-1962">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="44422-1962">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="44422-1963">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="44422-1963">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="44422-1964">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="44422-1964">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="44422-1965">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="44422-1965">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="44422-1966">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="44422-1966">Updated cmdlets</span></span>
        - <span data-ttu-id="44422-1967">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1967">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="44422-1968">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1968">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="44422-1969">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1969">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="44422-1970">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="44422-1970">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="44422-1971">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-1971">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="44422-1972">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="44422-1972">Updated cmdlet:</span></span>
        - <span data-ttu-id="44422-1973">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1973">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="44422-1974">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1974">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="44422-1975">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="44422-1975">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="44422-1976">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="44422-1976">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="44422-1977">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="44422-1977">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="44422-1978">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="44422-1978">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-1979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-1979">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-1980">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="44422-1980">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="44422-1981">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="44422-1981">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-1983">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1983">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="44422-1984">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1984">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="44422-1985">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1985">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="44422-1986">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1986">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="44422-1987">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1987">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="44422-1988">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1988">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="44422-1989">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1989">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="44422-1990">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1990">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="44422-1991">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-1991">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="44422-1992">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="44422-1992">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-1993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-1993">Az.Resources</span></span>
- <span data-ttu-id="44422-1994">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-1994">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="44422-1995">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="44422-1995">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="44422-1996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="44422-1996">Az.ServiceBus</span></span>
* <span data-ttu-id="44422-1997">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="44422-1997">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="44422-1998">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="44422-1998">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-1999">Az.Sql</span></span>
* <span data-ttu-id="44422-2000">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="44422-2000">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="44422-2001">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="44422-2001">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="44422-2002">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="44422-2002">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2003">Az.Storage</span></span>
* <span data-ttu-id="44422-2004">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="44422-2004">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="44422-2005">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="44422-2005">Az.StorageSync</span></span>
* <span data-ttu-id="44422-2006">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="44422-2006">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="44422-2007">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="44422-2007">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2008">Az.Websites</span></span>
* <span data-ttu-id="44422-2009">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44422-2009">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="44422-2010">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="44422-2010">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="44422-2011">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="44422-2011">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="44422-2012">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2012">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2013">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2013">Az.Accounts</span></span>
* <span data-ttu-id="44422-2014">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="44422-2014">Add support for profile cmdlets</span></span>
* <span data-ttu-id="44422-2015">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="44422-2015">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="44422-2016">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="44422-2016">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="44422-2017">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="44422-2017">Az.Advisor</span></span>
* <span data-ttu-id="44422-2018">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="44422-2018">GA release of Az.Advisor</span></span>
* <span data-ttu-id="44422-2019">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="44422-2019">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="44422-2020">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-2020">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-2021">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="44422-2021">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="44422-2022">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="44422-2022">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="44422-2023">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="44422-2023">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="44422-2024">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="44422-2024">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="44422-2025">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="44422-2025">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="44422-2026">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="44422-2026">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="44422-2027">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="44422-2027">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-2028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2028">Az.Automation</span></span>
* <span data-ttu-id="44422-2029">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="44422-2029">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2030">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2030">Az.Compute</span></span>
* <span data-ttu-id="44422-2031">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="44422-2031">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-2032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-2032">Az.DataFactory</span></span>
* <span data-ttu-id="44422-2033">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="44422-2033">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="44422-2034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="44422-2034">Az.EventGrid</span></span>
* <span data-ttu-id="44422-2035">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="44422-2035">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-2036">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-2036">Az.IotHub</span></span>
* <span data-ttu-id="44422-2037">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="44422-2037">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2038">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2038">Az.Network</span></span>
* <span data-ttu-id="44422-2039">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="44422-2039">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="44422-2040">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="44422-2040">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-2041">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2041">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-2042">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="44422-2042">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="44422-2043">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="44422-2043">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-2045">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="44422-2045">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2046">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-2047">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="44422-2047">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2048">Az.Resources</span></span>
    - <span data-ttu-id="44422-2049">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="44422-2049">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="44422-2050">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="44422-2050">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="44422-2051">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="44422-2051">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="44422-2052">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="44422-2052">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="44422-2053">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="44422-2053">Az.ServiceBus</span></span>
* <span data-ttu-id="44422-2054">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="44422-2054">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2055">Az.Sql</span></span>
* <span data-ttu-id="44422-2056">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="44422-2056">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="44422-2057">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="44422-2057">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="44422-2058">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="44422-2058">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="44422-2059">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="44422-2059">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="44422-2060">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="44422-2060">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="44422-2061">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="44422-2061">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="44422-2062">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="44422-2062">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="44422-2063">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="44422-2063">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="44422-2064">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="44422-2064">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2065">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2065">Az.Storage</span></span>
* <span data-ttu-id="44422-2066">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="44422-2066">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="44422-2067">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="44422-2067">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="44422-2068">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="44422-2068">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="44422-2069">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="44422-2069">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="44422-2070">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2070">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="44422-2071">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2071">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="44422-2072">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2072">Set-AzStorageAccount</span></span>
* <span data-ttu-id="44422-2073">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="44422-2073">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="44422-2074">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="44422-2074">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="44422-2075">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="44422-2075">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="44422-2076">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="44422-2076">Az.StorageSync</span></span>
* <span data-ttu-id="44422-2077">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="44422-2077">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="44422-2078">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2078">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2079">Az.Accounts</span></span>
* <span data-ttu-id="44422-2080">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="44422-2080">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="44422-2081">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="44422-2081">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="44422-2082">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="44422-2082">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="44422-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="44422-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="44422-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="44422-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2085">Az.Compute</span></span>
* <span data-ttu-id="44422-2086">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="44422-2086">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="44422-2087">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="44422-2087">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="44422-2088">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="44422-2088">Az.Dns</span></span>
* <span data-ttu-id="44422-2089">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="44422-2089">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="44422-2090">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="44422-2090">Az.EventGrid</span></span>
* <span data-ttu-id="44422-2091">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="44422-2091">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="44422-2092">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="44422-2092">New cmdlets:</span></span>
    - <span data-ttu-id="44422-2093">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="44422-2093">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="44422-2094">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-2094">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="44422-2095">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="44422-2095">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="44422-2096">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-2096">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="44422-2097">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="44422-2097">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="44422-2098">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-2098">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="44422-2099">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="44422-2099">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="44422-2100">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-2100">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="44422-2101">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="44422-2101">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="44422-2102">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="44422-2102">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="44422-2103">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="44422-2103">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="44422-2104">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-2104">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="44422-2105">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="44422-2105">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="44422-2106">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="44422-2106">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="44422-2107">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="44422-2107">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="44422-2108">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="44422-2108">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="44422-2109">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="44422-2109">Updated cmdlets:</span></span>
    - <span data-ttu-id="44422-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="44422-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="44422-2111">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="44422-2111">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="44422-2112">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="44422-2112">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="44422-2113">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="44422-2113">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="44422-2114">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="44422-2114">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="44422-2115">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="44422-2115">Event subscription expiration date,</span></span>
            - <span data-ttu-id="44422-2116">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="44422-2116">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="44422-2117">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="44422-2117">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="44422-2118">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="44422-2118">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="44422-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="44422-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="44422-2120">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="44422-2120">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="44422-2121">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="44422-2121">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="44422-2122">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="44422-2122">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="44422-2123">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="44422-2123">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-2124">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-2124">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-2125">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="44422-2125">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="44422-2126">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="44422-2126">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="44422-2127">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="44422-2127">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="44422-2128">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="44422-2128">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2129">Az.Network</span></span>
* <span data-ttu-id="44422-2130">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="44422-2130">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="44422-2131">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="44422-2131">New cmdlets</span></span>
        - <span data-ttu-id="44422-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="44422-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="44422-2133">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="44422-2133">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="44422-2134">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="44422-2134">New cmdlets</span></span>
        - <span data-ttu-id="44422-2135">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="44422-2135">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="44422-2136">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="44422-2136">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="44422-2137">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="44422-2137">New cmdlets</span></span>
        - <span data-ttu-id="44422-2138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="44422-2138">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="44422-2139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="44422-2139">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="44422-2140">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="44422-2140">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="44422-2141">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="44422-2141">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="44422-2142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="44422-2142">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="44422-2143">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44422-2143">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="44422-2144">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="44422-2144">New cmdlets</span></span>
        - <span data-ttu-id="44422-2145">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44422-2145">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="44422-2146">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44422-2146">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="44422-2147">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="44422-2147">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="44422-2148">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="44422-2148">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="44422-2149">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="44422-2149">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="44422-2150">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="44422-2150">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="44422-2151">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="44422-2151">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="44422-2152">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44422-2152">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="44422-2153">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="44422-2153">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="44422-2154">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="44422-2154">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="44422-2155">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2155">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="44422-2156">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="44422-2156">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="44422-2157">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2157">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="44422-2158">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="44422-2158">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="44422-2159">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="44422-2159">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="44422-2160">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="44422-2160">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="44422-2161">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="44422-2161">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="44422-2162">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2162">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="44422-2163">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="44422-2163">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="44422-2164">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="44422-2164">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="44422-2165">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="44422-2165">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="44422-2166">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="44422-2166">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="44422-2167">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="44422-2167">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="44422-2168">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="44422-2168">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="44422-2169">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="44422-2169">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="44422-2170">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="44422-2170">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="44422-2171">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="44422-2171">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-2172">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2172">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-2173">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="44422-2173">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2174">Az.Resources</span></span>
* <span data-ttu-id="44422-2175">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="44422-2175">Support for additional Template Export options</span></span>
    - <span data-ttu-id="44422-2176">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44422-2176">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="44422-2177">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44422-2177">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="44422-2178">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="44422-2178">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-2179">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-2179">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-2180">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="44422-2180">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2181">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2181">Az.Sql</span></span>
* <span data-ttu-id="44422-2182">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="44422-2182">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="44422-2183">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="44422-2183">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="44422-2184">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="44422-2184">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="44422-2185">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44422-2185">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="44422-2186">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44422-2186">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="44422-2187">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44422-2187">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="44422-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="44422-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="44422-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="44422-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2190">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2190">Az.Storage</span></span>
* <span data-ttu-id="44422-2191">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-2191">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="44422-2192">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2192">New-AzStorageAccount</span></span>
* <span data-ttu-id="44422-2193">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="44422-2193">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="44422-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2195">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2195">Az.Websites</span></span>
* <span data-ttu-id="44422-2196">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="44422-2196">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="44422-2197">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="44422-2197">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="44422-2198">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2198">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="44422-2199">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-2199">Az.Cdn</span></span>
* <span data-ttu-id="44422-2200">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="44422-2200">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2201">Az.Compute</span></span>
* <span data-ttu-id="44422-2202">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="44422-2202">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="44422-2203">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="44422-2203">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-2204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-2204">Az.EventHub</span></span>
* <span data-ttu-id="44422-2205">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="44422-2205">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="44422-2206">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44422-2206">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2207">Az.Network</span></span>
* <span data-ttu-id="44422-2208">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="44422-2208">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="44422-2209">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="44422-2209">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-2210">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2210">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-2211">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="44422-2211">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2212">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2212">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-2213">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="44422-2213">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="44422-2214">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="44422-2214">Az.ServiceBus</span></span>
* <span data-ttu-id="44422-2215">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44422-2215">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-2216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-2216">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-2217">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="44422-2217">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="44422-2218">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="44422-2218">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2219">Az.Sql</span></span>
* <span data-ttu-id="44422-2220">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="44422-2220">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="44422-2221">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2221">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="44422-2222">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="44422-2222">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="44422-2223">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="44422-2223">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2224">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2224">Az.Websites</span></span>
* <span data-ttu-id="44422-2225">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="44422-2225">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="44422-2226">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2226">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="44422-2227">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-2227">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-2228">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="44422-2228">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="44422-2229">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="44422-2229">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="44422-2230">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="44422-2230">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="44422-2231">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="44422-2231">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="44422-2232">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="44422-2232">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="44422-2233">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="44422-2233">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="44422-2234">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="44422-2234">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="44422-2235">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="44422-2235">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="44422-2236">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-2236">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="44422-2237">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="44422-2237">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="44422-2238">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2238">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="44422-2239">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="44422-2239">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="44422-2240">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="44422-2240">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="44422-2241">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="44422-2241">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="44422-2242">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="44422-2242">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="44422-2243">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="44422-2243">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="44422-2244">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="44422-2244">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="44422-2245">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="44422-2245">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="44422-2246">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="44422-2246">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="44422-2247">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="44422-2247">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="44422-2248">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="44422-2248">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="44422-2249">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="44422-2249">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="44422-2250">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="44422-2250">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="44422-2251">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-2251">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="44422-2252">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="44422-2252">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="44422-2253">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="44422-2253">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="44422-2254">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="44422-2254">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="44422-2255">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="44422-2255">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="44422-2256">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="44422-2256">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="44422-2257">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="44422-2257">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="44422-2258">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="44422-2258">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="44422-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="44422-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="44422-2260">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="44422-2260">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="44422-2261">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="44422-2261">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="44422-2262">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="44422-2262">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="44422-2263">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="44422-2263">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="44422-2264">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="44422-2264">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="44422-2265">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="44422-2265">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="44422-2266">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="44422-2266">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="44422-2267">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="44422-2267">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="44422-2268">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="44422-2268">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="44422-2269">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="44422-2269">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="44422-2270">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="44422-2270">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="44422-2271">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="44422-2271">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="44422-2272">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="44422-2272">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="44422-2273">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="44422-2273">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="44422-2274">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="44422-2274">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="44422-2275">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="44422-2275">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="44422-2276">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="44422-2276">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="44422-2277">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="44422-2277">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="44422-2278">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="44422-2278">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="44422-2279">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="44422-2279">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="44422-2280">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="44422-2280">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="44422-2281">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="44422-2281">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="44422-2282">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="44422-2282">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="44422-2283">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="44422-2283">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="44422-2284">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="44422-2284">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="44422-2285">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="44422-2285">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="44422-2286">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="44422-2286">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="44422-2287">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="44422-2287">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="44422-2288">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="44422-2288">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="44422-2289">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="44422-2289">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="44422-2290">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="44422-2290">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="44422-2291">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="44422-2291">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="44422-2292">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="44422-2292">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="44422-2293">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="44422-2293">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="44422-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="44422-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="44422-2295">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="44422-2295">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="44422-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="44422-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="44422-2297">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="44422-2297">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="44422-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="44422-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="44422-2299">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="44422-2299">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="44422-2300">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="44422-2300">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="44422-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="44422-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="44422-2302">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="44422-2302">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="44422-2303">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="44422-2303">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="44422-2304">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="44422-2304">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-2305">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2305">Az.Automation</span></span>
* <span data-ttu-id="44422-2306">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="44422-2306">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="44422-2307">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="44422-2307">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="44422-2308">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="44422-2308">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="44422-2309">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="44422-2309">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="44422-2310">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="44422-2310">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="44422-2311">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="44422-2311">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="44422-2312">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="44422-2312">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2313">Az.Compute</span></span>
* <span data-ttu-id="44422-2314">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="44422-2314">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="44422-2315">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="44422-2315">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-2316">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2316">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-2317">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2317">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-2318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-2318">Az.Monitor</span></span>
* <span data-ttu-id="44422-2319">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-2319">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2320">Az.Network</span></span>
* <span data-ttu-id="44422-2321">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="44422-2321">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="44422-2322">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="44422-2322">Updated cmdlet:</span></span>
        - <span data-ttu-id="44422-2323">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="44422-2323">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="44422-2324">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="44422-2324">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2325">Az.Resources</span></span>
* <span data-ttu-id="44422-2326">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="44422-2326">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2327">Az.Sql</span></span>
* <span data-ttu-id="44422-2328">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="44422-2328">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="44422-2329">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2329">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2330">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2330">Az.Accounts</span></span>
* <span data-ttu-id="44422-2331">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="44422-2331">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-2332">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-2332">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-2333">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="44422-2333">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="44422-2334">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="44422-2334">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2335">Az.Compute</span></span>
* <span data-ttu-id="44422-2336">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="44422-2336">Proximity placement group feature.</span></span>
    - <span data-ttu-id="44422-2337">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="44422-2337">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="44422-2338">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="44422-2338">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="44422-2339">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="44422-2339">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="44422-2340">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="44422-2340">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="44422-2341">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-2341">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="44422-2342">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="44422-2342">Breaking changes</span></span>
    - <span data-ttu-id="44422-2343">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="44422-2343">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="44422-2344">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="44422-2344">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="44422-2345">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="44422-2345">Az.DeploymentManager</span></span>
* <span data-ttu-id="44422-2346">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2346">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="44422-2347">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="44422-2347">Az.Dns</span></span>
* <span data-ttu-id="44422-2348">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="44422-2348">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="44422-2349">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="44422-2349">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="44422-2350">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="44422-2350">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="44422-2351">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-2351">Az.FrontDoor</span></span>
* <span data-ttu-id="44422-2352">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2352">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="44422-2353">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="44422-2353">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="44422-2354">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-2354">Az.HDInsight</span></span>
* <span data-ttu-id="44422-2355">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="44422-2355">Removed two cmdlets:</span></span>
    - <span data-ttu-id="44422-2356">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="44422-2356">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="44422-2357">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="44422-2357">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="44422-2358">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="44422-2358">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="44422-2359">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="44422-2359">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="44422-2360">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="44422-2360">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="44422-2361">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="44422-2361">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-2362">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-2362">Az.Monitor</span></span>
* <span data-ttu-id="44422-2363">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="44422-2363">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="44422-2364">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="44422-2364">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="44422-2365">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="44422-2365">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="44422-2366">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="44422-2366">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="44422-2367">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="44422-2367">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="44422-2368">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="44422-2368">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="44422-2369">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="44422-2369">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="44422-2370">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="44422-2370">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="44422-2371">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="44422-2371">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="44422-2372">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="44422-2372">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="44422-2373">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="44422-2373">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="44422-2374">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="44422-2374">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="44422-2375">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="44422-2375">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="44422-2376">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="44422-2376">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2377">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2377">Az.Network</span></span>
* <span data-ttu-id="44422-2378">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="44422-2378">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="44422-2379">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="44422-2379">New cmdlets</span></span>
        - <span data-ttu-id="44422-2380">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="44422-2380">New-AzNatGateway</span></span>
        - <span data-ttu-id="44422-2381">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="44422-2381">Get-AzNatGateway</span></span>
        - <span data-ttu-id="44422-2382">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="44422-2382">Set-AzNatGateway</span></span>
        - <span data-ttu-id="44422-2383">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="44422-2383">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="44422-2384">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="44422-2384">Updated cmdlets</span></span>
        - <span data-ttu-id="44422-2385">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="44422-2385">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="44422-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="44422-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="44422-2387">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="44422-2387">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="44422-2388">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="44422-2388">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="44422-2389">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="44422-2389">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-2390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2390">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-2391">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="44422-2391">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="44422-2392">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="44422-2392">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="44422-2393">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="44422-2393">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2394">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2394">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-2395">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="44422-2395">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="44422-2396">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="44422-2396">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="44422-2397">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="44422-2397">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="44422-2398">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-2398">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="44422-2399">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="44422-2399">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="44422-2400">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="44422-2400">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="44422-2401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="44422-2401">Az.Relay</span></span>
* <span data-ttu-id="44422-2402">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="44422-2402">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="44422-2403">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="44422-2403">Az.ServiceBus</span></span>
* <span data-ttu-id="44422-2404">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="44422-2404">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2405">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2405">Az.Storage</span></span>
* <span data-ttu-id="44422-2406">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="44422-2406">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="44422-2407">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="44422-2407">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="44422-2408">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="44422-2408">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="44422-2409">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2409">New-AzStorageAccount</span></span>
* <span data-ttu-id="44422-2410">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="44422-2410">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="44422-2411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2411">New-AzStorageAccount</span></span>
    - <span data-ttu-id="44422-2412">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2412">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="44422-2413">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2413">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2414">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2414">Az.Websites</span></span>
* <span data-ttu-id="44422-2415">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="44422-2415">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="44422-2416">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="44422-2416">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="44422-2417">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2417">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="44422-2418">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="44422-2418">Highlights since the last major release</span></span>
* <span data-ttu-id="44422-2419">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="44422-2419">General availability of `Az` module</span></span>
* <span data-ttu-id="44422-2420">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="44422-2420">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="44422-2421">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="44422-2421">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="44422-2422">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2422">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="44422-2423">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="44422-2423">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="44422-2424">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2424">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="44422-2425">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="44422-2425">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-2426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2426">Az.Accounts</span></span>
* <span data-ttu-id="44422-2427">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="44422-2427">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="44422-2428">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-2428">Az.Batch</span></span>
* <span data-ttu-id="44422-2429">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="44422-2430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-2430">Az.Cdn</span></span>
* <span data-ttu-id="44422-2431">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-2432">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-2432">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-2433">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2433">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2434">Az.Compute</span></span>
* <span data-ttu-id="44422-2435">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="44422-2435">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="44422-2436">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="44422-2437">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="44422-2437">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-2438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-2438">Az.DataFactory</span></span>
* <span data-ttu-id="44422-2439">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="44422-2439">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-2441">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2441">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="44422-2442">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="44422-2442">Az.EventGrid</span></span>
* <span data-ttu-id="44422-2443">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="44422-2443">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-2444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-2444">Az.EventHub</span></span>
* <span data-ttu-id="44422-2445">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="44422-2445">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="44422-2446">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="44422-2446">Az.HDInsight</span></span>
* <span data-ttu-id="44422-2447">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2447">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-2448">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-2448">Az.IotHub</span></span>
* <span data-ttu-id="44422-2449">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2449">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-2450">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-2450">Az.KeyVault</span></span>
* <span data-ttu-id="44422-2451">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2451">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="44422-2452">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="44422-2452">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="44422-2453">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="44422-2453">Az.MachineLearning</span></span>
* <span data-ttu-id="44422-2454">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2454">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="44422-2455">Az.Media</span><span class="sxs-lookup"><span data-stu-id="44422-2455">Az.Media</span></span>
* <span data-ttu-id="44422-2456">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-2457">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-2457">Az.Monitor</span></span>
  * <span data-ttu-id="44422-2458">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="44422-2458">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="44422-2459">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="44422-2459">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="44422-2460">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="44422-2460">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="44422-2461">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="44422-2461">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="44422-2462">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="44422-2462">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="44422-2463">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="44422-2463">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="44422-2464">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="44422-2464">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2465">Az.Network</span></span>
* <span data-ttu-id="44422-2466">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2466">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="44422-2467">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="44422-2467">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="44422-2468">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="44422-2468">Az.NotificationHubs</span></span>
* <span data-ttu-id="44422-2469">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2469">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-2470">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2470">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-2471">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2471">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="44422-2472">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="44422-2472">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="44422-2473">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2474">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2474">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-2475">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="44422-2476">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2476">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="44422-2477">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="44422-2477">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="44422-2478">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="44422-2478">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="44422-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="44422-2479">Az.RedisCache</span></span>
* <span data-ttu-id="44422-2480">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2481">Az.Resources</span></span>
* <span data-ttu-id="44422-2482">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="44422-2482">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2483">Az.Sql</span></span>
* <span data-ttu-id="44422-2484">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="44422-2484">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="44422-2485">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2485">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="44422-2486">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="44422-2486">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="44422-2487">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="44422-2487">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="44422-2488">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="44422-2488">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="44422-2489">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="44422-2489">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="44422-2490">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="44422-2490">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2491">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2491">Az.Websites</span></span>
* <span data-ttu-id="44422-2492">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="44422-2492">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="44422-2493">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="44422-2493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="44422-2494">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="44422-2494">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="44422-2495">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="44422-2495">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="44422-2496">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2496">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="44422-2497">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="44422-2497">Highlights since the last major release</span></span>
* <span data-ttu-id="44422-2498">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="44422-2498">General availability of `Az` module</span></span>
* <span data-ttu-id="44422-2499">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="44422-2499">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="44422-2500">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="44422-2500">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="44422-2501">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2501">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="44422-2502">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="44422-2502">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="44422-2503">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2503">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="44422-2504">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="44422-2504">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="44422-2505">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2505">Az.Accounts</span></span>
* <span data-ttu-id="44422-2506">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="44422-2506">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="44422-2507">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="44422-2507">Az.AnalysisServices</span></span>
* <span data-ttu-id="44422-2508">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="44422-2508">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="44422-2509">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="44422-2509">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-2510">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2510">Az.Automation</span></span>
* <span data-ttu-id="44422-2511">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="44422-2511">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="44422-2512">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="44422-2512">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="44422-2513">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2513">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2514">Az.Compute</span></span>
* <span data-ttu-id="44422-2515">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="44422-2515">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="44422-2516">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="44422-2516">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="44422-2517">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="44422-2517">Az.ContainerInstance</span></span>
* <span data-ttu-id="44422-2518">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="44422-2518">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-2519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-2519">Az.DataFactory</span></span>
* <span data-ttu-id="44422-2520">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="44422-2520">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="44422-2521">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="44422-2521">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2522">Az.Resources</span></span>
* <span data-ttu-id="44422-2523">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="44422-2523">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="44422-2524">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-2524">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="44422-2525">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="44422-2525">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="44422-2526">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="44422-2526">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="44422-2527">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="44422-2527">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="44422-2528">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="44422-2528">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2529">Az.Sql</span></span>
* <span data-ttu-id="44422-2530">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="44422-2530">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2531">Az.Storage</span></span>
* <span data-ttu-id="44422-2532">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2532">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="44422-2533">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="44422-2533">New-AzStorageContext</span></span>
* <span data-ttu-id="44422-2534">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="44422-2534">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="44422-2535">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="44422-2535">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="44422-2536">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="44422-2536">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="44422-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="44422-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="44422-2539">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="44422-2539">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="44422-2540">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="44422-2540">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="44422-2541">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="44422-2541">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="44422-2542">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="44422-2542">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="44422-2543">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="44422-2543">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="44422-2544">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2544">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="44422-2545">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="44422-2545">Highlights since the last major release</span></span>
* <span data-ttu-id="44422-2546">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="44422-2546">General availability of `Az` module</span></span>
* <span data-ttu-id="44422-2547">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="44422-2547">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="44422-2548">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="44422-2548">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="44422-2549">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2549">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="44422-2550">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="44422-2550">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="44422-2551">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2551">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="44422-2552">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="44422-2552">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-2553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2553">Az.Automation</span></span>
* <span data-ttu-id="44422-2554">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="44422-2554">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="44422-2555">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="44422-2555">Dynamic grouping</span></span>
    * <span data-ttu-id="44422-2556">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="44422-2556">Pre-Post script</span></span>
    * <span data-ttu-id="44422-2557">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="44422-2557">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2558">Az.Compute</span></span>
* <span data-ttu-id="44422-2559">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="44422-2559">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="44422-2560">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="44422-2560">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-2561">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-2561">Az.KeyVault</span></span>
* <span data-ttu-id="44422-2562">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-2562">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2563">Az.Network</span></span>
* <span data-ttu-id="44422-2564">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2564">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="44422-2565">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="44422-2565">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2566">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2566">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-2567">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="44422-2567">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="44422-2568">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="44422-2568">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2569">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2569">Az.Resources</span></span>
* <span data-ttu-id="44422-2570">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44422-2570">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="44422-2571">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="44422-2571">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2572">Az.Sql</span></span>
* <span data-ttu-id="44422-2573">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="44422-2573">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2574">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2574">Az.Storage</span></span>
* <span data-ttu-id="44422-2575">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-2575">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="44422-2576">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2576">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="44422-2577">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2577">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="44422-2578">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2578">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="44422-2579">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="44422-2579">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="44422-2580">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="44422-2580">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="44422-2581">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="44422-2581">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2582">Az.Websites</span></span>
* <span data-ttu-id="44422-2583">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="44422-2583">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="44422-2584">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2584">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2585">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2585">Az.Accounts</span></span>
* <span data-ttu-id="44422-2586">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="44422-2586">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="44422-2587">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2587">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2588">Az.Automation</span></span>
* <span data-ttu-id="44422-2589">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2589">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="44422-2590">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="44422-2590">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="44422-2591">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="44422-2591">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="44422-2592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-2592">Az.Cdn</span></span>
* <span data-ttu-id="44422-2593">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="44422-2593">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2594">Az.Compute</span></span>
* <span data-ttu-id="44422-2595">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="44422-2595">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-2596">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-2596">Az.DataFactory</span></span>
* <span data-ttu-id="44422-2597">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="44422-2597">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="44422-2598">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="44422-2598">Az.LogicApp</span></span>
* <span data-ttu-id="44422-2599">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="44422-2599">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2600">Az.Network</span></span>
* <span data-ttu-id="44422-2601">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="44422-2601">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2602">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2602">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-2603">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-2603">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="44422-2604">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="44422-2604">SDK Update</span></span>
* <span data-ttu-id="44422-2605">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="44422-2605">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="44422-2606">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="44422-2606">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2607">Az.Resources</span></span>
* <span data-ttu-id="44422-2608">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="44422-2608">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="44422-2609">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="44422-2609">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="44422-2610">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="44422-2610">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="44422-2611">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="44422-2611">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="44422-2612">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="44422-2612">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="44422-2613">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="44422-2613">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2614">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2614">Az.Sql</span></span>
* <span data-ttu-id="44422-2615">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="44422-2615">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="44422-2616">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="44422-2616">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2617">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2617">Az.Storage</span></span>
* <span data-ttu-id="44422-2618">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2618">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="44422-2619">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2619">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="44422-2620">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="44422-2620">Az.AnalysisServices</span></span>
* <span data-ttu-id="44422-2621">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2621">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-2622">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2622">Az.Automation</span></span>
* <span data-ttu-id="44422-2623">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2623">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="44422-2624">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2624">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="44422-2625">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2625">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-2626">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-2626">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-2627">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="44422-2627">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2628">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2628">Az.Compute</span></span>
* <span data-ttu-id="44422-2629">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="44422-2629">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="44422-2630">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="44422-2630">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="44422-2631">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="44422-2631">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="44422-2632">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="44422-2632">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-2633">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2633">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-2634">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="44422-2634">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="44422-2635">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-2635">Az.EventHub</span></span>
* <span data-ttu-id="44422-2636">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="44422-2636">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-2637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-2637">Az.KeyVault</span></span>
* <span data-ttu-id="44422-2638">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="44422-2638">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="44422-2639">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="44422-2639">Az.LogicApp</span></span>
* <span data-ttu-id="44422-2640">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="44422-2640">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="44422-2641">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="44422-2641">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="44422-2642">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="44422-2642">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="44422-2643">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="44422-2643">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="44422-2644">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="44422-2644">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="44422-2645">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="44422-2645">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="44422-2646">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="44422-2646">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="44422-2647">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="44422-2647">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="44422-2648">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2648">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="44422-2649">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2649">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="44422-2650">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2650">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="44422-2651">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2651">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="44422-2652">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="44422-2652">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="44422-2653">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-2653">Az.Monitor</span></span>
* <span data-ttu-id="44422-2654">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="44422-2654">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2655">Az.Network</span></span>
* <span data-ttu-id="44422-2656">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="44422-2656">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="44422-2657">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2657">Az.OperationalInsights</span></span>
* <span data-ttu-id="44422-2658">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="44422-2658">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="44422-2659">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="44422-2659">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="44422-2660">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="44422-2660">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2661">Az.Resources</span></span>
* <span data-ttu-id="44422-2662">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="44422-2662">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="44422-2663">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="44422-2663">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="44422-2664">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="44422-2664">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="44422-2665">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="44422-2665">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2666">Az.Sql</span></span>
* <span data-ttu-id="44422-2667">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="44422-2667">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="44422-2668">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="44422-2668">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2669">Az.Websites</span></span>
* <span data-ttu-id="44422-2670">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="44422-2670">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="44422-2671">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2671">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2672">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2672">Az.Accounts</span></span>
* <span data-ttu-id="44422-2673">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="44422-2673">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="44422-2674">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="44422-2674">Az.AnalysisServices</span></span>
<span data-ttu-id="44422-2675">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="44422-2675">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2676">Az.Compute</span></span>
* <span data-ttu-id="44422-2677">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="44422-2677">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="44422-2678">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="44422-2678">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="44422-2679">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="44422-2679">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2680">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2680">Az.RecoveryServices</span></span>
<span data-ttu-id="44422-2681">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="44422-2681">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2682">Az.Resources</span></span>
* <span data-ttu-id="44422-2683">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="44422-2683">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="44422-2684">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="44422-2684">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="44422-2685">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="44422-2685">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="44422-2686">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="44422-2686">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2687">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2687">Az.Sql</span></span>
* <span data-ttu-id="44422-2688">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="44422-2688">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="44422-2689">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="44422-2689">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="44422-2690">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="44422-2690">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="44422-2691">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2691">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2692">Az.Accounts</span></span>
* <span data-ttu-id="44422-2693">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="44422-2693">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="44422-2694">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="44422-2694">Az.AnalysisServices</span></span>
* <span data-ttu-id="44422-2695">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-2695">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2696">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2696">Az.RecoveryServices</span></span>
* <span data-ttu-id="44422-2697">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-2697">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="44422-2698">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2698">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2699">Az.Accounts</span></span>
* <span data-ttu-id="44422-2700">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="44422-2700">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="44422-2701">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2701">Update incorrect online help URLs</span></span>
* <span data-ttu-id="44422-2702">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="44422-2702">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="44422-2703">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="44422-2703">Az.Aks</span></span>
* <span data-ttu-id="44422-2704">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2704">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="44422-2705">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2705">Az.Automation</span></span>
* <span data-ttu-id="44422-2706">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="44422-2706">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="44422-2707">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2707">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="44422-2708">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="44422-2708">Az.Cdn</span></span>
* <span data-ttu-id="44422-2709">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2709">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2710">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2710">Az.Compute</span></span>
* <span data-ttu-id="44422-2711">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="44422-2711">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="44422-2712">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="44422-2712">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="44422-2713">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="44422-2713">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="44422-2714">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="44422-2714">Az.ContainerRegistry</span></span>
* <span data-ttu-id="44422-2715">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2715">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="44422-2716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="44422-2716">Az.DataFactory</span></span>
* <span data-ttu-id="44422-2717">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="44422-2717">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-2718">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2718">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-2719">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="44422-2719">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="44422-2720">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="44422-2720">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="44422-2721">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2721">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-2722">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-2722">Az.IotHub</span></span>
* <span data-ttu-id="44422-2723">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="44422-2723">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="44422-2724">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-2724">Az.KeyVault</span></span>
* <span data-ttu-id="44422-2725">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2725">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2726">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2726">Az.Network</span></span>
* <span data-ttu-id="44422-2727">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2727">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2728">Az.Resources</span></span>
* <span data-ttu-id="44422-2729">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="44422-2729">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="44422-2730">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="44422-2730">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="44422-2731">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="44422-2731">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="44422-2732">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="44422-2732">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="44422-2733">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="44422-2733">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="44422-2734">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="44422-2734">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="44422-2735">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="44422-2735">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-2737">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="44422-2737">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="44422-2738">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="44422-2738">Fix some error messages.</span></span>
* <span data-ttu-id="44422-2739">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="44422-2739">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="44422-2740">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="44422-2740">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="44422-2741">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="44422-2741">Az.SignalR</span></span>
* <span data-ttu-id="44422-2742">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2742">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2743">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2743">Az.Sql</span></span>
* <span data-ttu-id="44422-2744">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2744">Update incorrect online help URLs</span></span>
* <span data-ttu-id="44422-2745">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="44422-2745">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="44422-2746">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="44422-2746">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="44422-2747">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="44422-2747">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2748">Az.Storage</span></span>
* <span data-ttu-id="44422-2749">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2749">Update incorrect online help URLs</span></span>
* <span data-ttu-id="44422-2750">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="44422-2750">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="44422-2751">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="44422-2751">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="44422-2752">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="44422-2752">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="44422-2753">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="44422-2753">Az.TrafficManager</span></span>
* <span data-ttu-id="44422-2754">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2754">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2755">Az.Websites</span></span>
* <span data-ttu-id="44422-2756">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="44422-2756">Update incorrect online help URLs</span></span>
* <span data-ttu-id="44422-2757">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="44422-2757">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="44422-2758">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="44422-2758">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="44422-2759">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="44422-2759">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="44422-2760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2760">Az.Accounts</span></span>
* <span data-ttu-id="44422-2761">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="44422-2761">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2762">Az.Compute</span></span>
* <span data-ttu-id="44422-2763">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="44422-2763">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="44422-2764">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="44422-2764">Updated the description of ID in help files</span></span>
* <span data-ttu-id="44422-2765">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2765">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2766">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-2767">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="44422-2767">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="44422-2768">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="44422-2768">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="44422-2769">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="44422-2769">Az.EventGrid</span></span>
* <span data-ttu-id="44422-2770">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="44422-2770">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="44422-2771">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="44422-2771">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="44422-2772">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="44422-2772">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="44422-2773">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="44422-2773">Event Time-To-Live,</span></span>
        - <span data-ttu-id="44422-2774">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="44422-2774">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="44422-2775">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="44422-2775">Dead letter endpoint.</span></span>
    - <span data-ttu-id="44422-2776">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="44422-2776">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="44422-2777">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="44422-2777">Event Time-To-Live,</span></span>
        - <span data-ttu-id="44422-2778">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="44422-2778">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="44422-2779">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="44422-2779">Dead letter endpoint.</span></span>
* <span data-ttu-id="44422-2780">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="44422-2780">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="44422-2781">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="44422-2781">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="44422-2782">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-2782">Az.IotHub</span></span>
* <span data-ttu-id="44422-2783">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="44422-2783">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="44422-2784">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="44422-2784">Az.LogicApp</span></span>
* <span data-ttu-id="44422-2785">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="44422-2785">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-2786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2786">Az.Resources</span></span>
* <span data-ttu-id="44422-2787">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="44422-2787">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="44422-2788">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="44422-2788">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="44422-2789">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="44422-2789">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="44422-2790">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="44422-2790">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="44422-2791">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="44422-2791">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="44422-2792">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="44422-2792">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="44422-2793">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="44422-2793">Az.SignalR</span></span>
* <span data-ttu-id="44422-2794">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2794">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-2795">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2795">Az.Sql</span></span>
* <span data-ttu-id="44422-2796">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="44422-2796">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="44422-2797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2797">Az.Storage</span></span>
* <span data-ttu-id="44422-2798">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="44422-2798">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="44422-2799">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="44422-2799">New-AzStorageContext</span></span>
* <span data-ttu-id="44422-2800">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="44422-2800">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="44422-2801">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="44422-2801">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2802">Az.Websites</span></span>
* <span data-ttu-id="44422-2803">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="44422-2803">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="44422-2804">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2804">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="44422-2805">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="44422-2805">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="44422-2806">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-2806">General</span></span>

- <span data-ttu-id="44422-2807">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="44422-2807">General Availability of Az Module</span></span>
- <span data-ttu-id="44422-2808">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="44422-2808">Online help for each module</span></span>
- <span data-ttu-id="44422-2809">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="44422-2809">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="44422-2810">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="44422-2810">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="44422-2811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2811">Az.Accounts</span></span>
- <span data-ttu-id="44422-2812">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="44422-2812">Changed from Az.Profile</span></span>
- <span data-ttu-id="44422-2813">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="44422-2813">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="44422-2814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-2814">Az.ApiManagement</span></span>
- <span data-ttu-id="44422-2815">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="44422-2815">Fixes for #7002</span></span>
- <span data-ttu-id="44422-2816">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="44422-2817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="44422-2817">Az.Batch</span></span>
- <span data-ttu-id="44422-2818">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="44422-2818">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="44422-2819">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="44422-2819">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="44422-2820">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="44422-2821">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="44422-2821">Az.Billing</span></span>
- <span data-ttu-id="44422-2822">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2822">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="44422-2823">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="44422-2823">Az.CognitivServices</span></span>
- <span data-ttu-id="44422-2824">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2824">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="44422-2825">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="44422-2825">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="44422-2826">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="44422-2826">Az.ContainerInstance</span></span>
- <span data-ttu-id="44422-2827">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="44422-2827">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="44422-2828">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="44422-2828">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="44422-2829">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2829">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="44422-2830">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2830">Az.DataLakeStore</span></span>
- <span data-ttu-id="44422-2831">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="44422-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="44422-2832">Az.Monitor</span></span>
- <span data-ttu-id="44422-2833">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2833">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="44422-2834">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="44422-2834">Az.KeyVault</span></span>
- <span data-ttu-id="44422-2835">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="44422-2835">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="44422-2836">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="44422-2836">Az.MachineLearning</span></span>
- <span data-ttu-id="44422-2837">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="44422-2837">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="44422-2838">Az.Media</span><span class="sxs-lookup"><span data-stu-id="44422-2838">Az.Media</span></span>
- <span data-ttu-id="44422-2839">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="44422-2839">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="44422-2840">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2840">Az.Network</span></span>
<span data-ttu-id="44422-2841">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="44422-2841">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="44422-2842">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="44422-2842">New cmdlets added:</span></span>
        - <span data-ttu-id="44422-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="44422-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="44422-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="44422-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="44422-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="44422-2848">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="44422-2848">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="44422-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="44422-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="44422-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="44422-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="44422-2851">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="44422-2851">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="44422-2852">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44422-2852">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="44422-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44422-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="44422-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="44422-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="44422-2855">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="44422-2855">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="44422-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="44422-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="44422-2857">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="44422-2857">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="44422-2858">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="44422-2858">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="44422-2859">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44422-2859">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="44422-2860">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44422-2860">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="44422-2861">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="44422-2861">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="44422-2862">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="44422-2862">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="44422-2863">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2863">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="44422-2864">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="44422-2864">Az.OperationalInsights</span></span>
- <span data-ttu-id="44422-2865">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2865">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="44422-2866">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="44422-2866">Az.Profile</span></span>
- <span data-ttu-id="44422-2867">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="44422-2867">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2868">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2868">Az.RecoveryServices</span></span>
- <span data-ttu-id="44422-2869">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2869">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="44422-2870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2870">Az.Resources</span></span>
- <span data-ttu-id="44422-2871">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2871">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="44422-2872">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-2872">Az.ServiceFabric</span></span>
- <span data-ttu-id="44422-2873">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="44422-2873">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="44422-2874">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2874">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="44422-2875">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="44422-2875">Az.SIgnalR</span></span>
- <span data-ttu-id="44422-2876">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="44422-2876">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="44422-2877">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2877">Az.Sql</span></span>
- <span data-ttu-id="44422-2878">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="44422-2878">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="44422-2879">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="44422-2879">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="44422-2880">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2880">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="44422-2881">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2881">Az.Storage</span></span>
- <span data-ttu-id="44422-2882">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2882">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="44422-2883">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2883">Az.Websites</span></span>
- <span data-ttu-id="44422-2884">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="44422-2884">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="44422-2885">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="44422-2885">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="44422-2886">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-2886">General</span></span>

* <span data-ttu-id="44422-2887">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="44422-2887">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="44422-2888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2888">Az.Compute</span></span>

* <span data-ttu-id="44422-2889">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="44422-2889">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="44422-2890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2890">Az.DataLakeStore</span></span>

* <span data-ttu-id="44422-2891">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="44422-2891">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="44422-2892">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="44422-2892">Az.FrontDoor</span></span>

* <span data-ttu-id="44422-2893">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="44422-2893">Fixed some broken links</span></span>
    - <span data-ttu-id="44422-2894">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="44422-2894">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="44422-2895">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="44422-2895">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="44422-2896">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="44422-2896">Az.RecoveryServices</span></span>

* <span data-ttu-id="44422-2897">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="44422-2897">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="44422-2898">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="44422-2898">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="44422-2899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2899">Az.Resources</span></span>

* <span data-ttu-id="44422-2900">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="44422-2900">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="44422-2901">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="44422-2901">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="44422-2902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2902">Az.Sql</span></span>

* <span data-ttu-id="44422-2903">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="44422-2903">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="44422-2904">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="44422-2904">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="44422-2905">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="44422-2905">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="44422-2906">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-2906">Az.Storage</span></span>

* <span data-ttu-id="44422-2907">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2907">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="44422-2908">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="44422-2908">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="44422-2909">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="44422-2909">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="44422-2910">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="44422-2910">Support Static Website configuration</span></span>
    - <span data-ttu-id="44422-2911">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="44422-2911">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="44422-2912">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="44422-2912">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="44422-2913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-2913">Az.Websites</span></span>

* <span data-ttu-id="44422-2914">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44422-2914">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="44422-2915">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="44422-2915">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="44422-2916">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44422-2916">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="44422-2917">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="44422-2917">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="44422-2918">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="44422-2918">Az.ApiManagement</span></span>
* <span data-ttu-id="44422-2919">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="44422-2919">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="44422-2920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="44422-2920">Az.Automation</span></span>
* <span data-ttu-id="44422-2921">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="44422-2921">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="44422-2922">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-2922">Added Update Management cmdlets</span></span>
* <span data-ttu-id="44422-2923">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-2923">Added Source Control cmdlets</span></span>
* <span data-ttu-id="44422-2924">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="44422-2924">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="44422-2925">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="44422-2925">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="44422-2926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2926">Az.Compute</span></span>
* <span data-ttu-id="44422-2927">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="44422-2927">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="44422-2928">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="44422-2928">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="44422-2929">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="44422-2929">Az.ContainerInstance</span></span>
* <span data-ttu-id="44422-2930">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="44422-2930">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="44422-2931">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="44422-2931">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="44422-2932">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="44422-2932">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="44422-2933">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2933">Az.Network</span></span>
* <span data-ttu-id="44422-2934">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-2934">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="44422-2935">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="44422-2935">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="44422-2936">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="44422-2936">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="44422-2937">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="44422-2937">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="44422-2938">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="44422-2938">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="44422-2939">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="44422-2939">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="44422-2940">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="44422-2940">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="44422-2941">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="44422-2941">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="44422-2942">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="44422-2942">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="44422-2943">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="44422-2943">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="44422-2944">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="44422-2944">Az.Relay</span></span>
* <span data-ttu-id="44422-2945">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="44422-2945">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="44422-2946">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-2946">Az.Resources</span></span>
* <span data-ttu-id="44422-2947">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="44422-2947">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="44422-2948">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="44422-2948">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="44422-2949">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="44422-2949">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="44422-2950">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-2950">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-2951">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="44422-2951">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="44422-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-2952">Az.Sql</span></span>
* <span data-ttu-id="44422-2953">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="44422-2953">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="44422-2954">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="44422-2954">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="44422-2955">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="44422-2955">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="44422-2956">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="44422-2956">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="44422-2957">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="44422-2957">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="44422-2958">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="44422-2958">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="44422-2959">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="44422-2959">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="44422-2960">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="44422-2960">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="44422-2961">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="44422-2961">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="44422-2962">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="44422-2962">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="44422-2963">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="44422-2963">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="44422-2964">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="44422-2964">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="44422-2965">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="44422-2965">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="44422-2966">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="44422-2966">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="44422-2967">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="44422-2967">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="44422-2968">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="44422-2968">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="44422-2969">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44422-2969">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="44422-2970">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="44422-2970">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="44422-2971">Geral</span><span class="sxs-lookup"><span data-stu-id="44422-2971">General</span></span>
* <span data-ttu-id="44422-2972">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="44422-2972">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="44422-2973">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="44422-2973">Az.Profile</span></span>
* <span data-ttu-id="44422-2974">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="44422-2974">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="44422-2975">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="44422-2975">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="44422-2976">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="44422-2976">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="44422-2977">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="44422-2977">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="44422-2978">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="44422-2978">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="44422-2979">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="44422-2979">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="44422-2980">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="44422-2980">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-2981">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-2981">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-2982">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="44422-2982">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-2983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-2983">Az.Compute</span></span>
* <span data-ttu-id="44422-2984">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="44422-2984">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="44422-2985">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="44422-2985">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="44422-2986">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="44422-2986">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-2987">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-2988">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="44422-2988">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="44422-2989">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="44422-2989">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="44422-2990">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="44422-2990">Az.Insights</span></span>
* <span data-ttu-id="44422-2991">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="44422-2991">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="44422-2992">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="44422-2992">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="44422-2993">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="44422-2993">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="44422-2994">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="44422-2994">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-2995">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-2995">Az.Network</span></span>
* <span data-ttu-id="44422-2996">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="44422-2996">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="44422-2997">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="44422-2997">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="44422-2998">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="44422-2998">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="44422-2999">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="44422-2999">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="44422-3000">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="44422-3000">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="44422-3001">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="44422-3001">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="44422-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="44422-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="44422-3003">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="44422-3003">Az.PolicyInsights</span></span>
* <span data-ttu-id="44422-3004">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="44422-3004">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-3005">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-3005">Az.Resources</span></span>
* <span data-ttu-id="44422-3006">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="44422-3006">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="44422-3007">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="44422-3007">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="44422-3008">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="44422-3008">Az.ServiceBus</span></span>
* <span data-ttu-id="44422-3009">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="44422-3009">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="44422-3010">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="44422-3010">Az.ServiceFabric</span></span>
* <span data-ttu-id="44422-3011">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="44422-3011">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="44422-3012">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="44422-3012">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="44422-3013">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="44422-3013">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="44422-3014">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="44422-3014">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="44422-3015">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="44422-3015">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="44422-3016">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="44422-3016">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="44422-3017">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="44422-3017">Az.Profile</span></span>
* <span data-ttu-id="44422-3018">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="44422-3018">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="44422-3019">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="44422-3019">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-3020">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-3020">Az.Compute</span></span>
* <span data-ttu-id="44422-3021">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="44422-3021">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="44422-3022">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="44422-3022">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="44422-3023">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="44422-3023">Az.DataLakeStore</span></span>
* <span data-ttu-id="44422-3024">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="44422-3024">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="44422-3025">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44422-3025">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="44422-3026">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="44422-3026">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="44422-3027">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="44422-3027">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="44422-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44422-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-3029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-3029">Az.Network</span></span>
* <span data-ttu-id="44422-3030">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="44422-3030">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="44422-3031">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="44422-3031">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-3032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-3032">Az.Resources</span></span>
* <span data-ttu-id="44422-3033">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="44422-3033">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="44422-3034">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="44422-3034">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="44422-3035">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="44422-3035">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="44422-3036">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="44422-3036">Azure.Storage</span></span>
* <span data-ttu-id="44422-3037">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="44422-3037">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="44422-3038">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="44422-3038">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="44422-3039">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="44422-3039">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="44422-3040">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="44422-3040">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="44422-3041">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="44422-3041">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="44422-3042">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="44422-3042">Az.CognitiveServices</span></span>
* <span data-ttu-id="44422-3043">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="44422-3043">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="44422-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="44422-3044">Az.Compute</span></span>
* <span data-ttu-id="44422-3045">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="44422-3045">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="44422-3046">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="44422-3046">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="44422-3047">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="44422-3047">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="44422-3048">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="44422-3048">Az.DataFactoryV2</span></span>
* <span data-ttu-id="44422-3049">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="44422-3049">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="44422-3050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="44422-3050">Az.Network</span></span>
* <span data-ttu-id="44422-3051">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="44422-3051">Added NetworkProfile functionality.</span></span> <span data-ttu-id="44422-3052">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="44422-3052">new cmdlets added</span></span>
    - <span data-ttu-id="44422-3053">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="44422-3053">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="44422-3054">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="44422-3054">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="44422-3055">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="44422-3055">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="44422-3056">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="44422-3056">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="44422-3057">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="44422-3057">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="44422-3058">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="44422-3058">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="44422-3059">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="44422-3059">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="44422-3060">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="44422-3060">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="44422-3061">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="44422-3061">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="44422-3062">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="44422-3062">Az.RedisCache</span></span>
* <span data-ttu-id="44422-3063">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="44422-3063">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="44422-3064">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="44422-3064">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="44422-3065">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="44422-3065">Az.Resources</span></span>
* <span data-ttu-id="44422-3066">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="44422-3066">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="44422-3067">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="44422-3067">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="44422-3068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="44422-3068">Az.Sql</span></span>
* <span data-ttu-id="44422-3069">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="44422-3069">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="44422-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="44422-3070">Az.Websites</span></span>
* <span data-ttu-id="44422-3071">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="44422-3071">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="44422-3072">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="44422-3072">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="44422-3073">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="44422-3073">0.2.0 - September 2018</span></span>
 <span data-ttu-id="44422-3074">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="44422-3074">Initial Release</span></span>
