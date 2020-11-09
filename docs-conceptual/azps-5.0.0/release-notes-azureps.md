---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4ab5639cfb997c5f9ee1286e6eacb97ef775239a
ms.sourcegitcommit: 63181e0af0e4468b0530fdb0495ed4d44bdfd1c8
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2020
ms.locfileid: "93134855"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="dcd6e-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="dcd6e-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="dcd6e-104">5.0.0 – outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-105">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-106">[Alteração da Falha] Remoção de 'Get-AzProfile' e 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="dcd6e-107">Substituição da Biblioteca de Autenticação do Azure Directory pela MSAL (Biblioteca de Autenticação da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-108">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-109">[Alteração da Falha] Remoção do alias do parâmetro 'ClientIdAndSecret' em 'New-AzAksCluster' e 'Set-AzAksCluster'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="dcd6e-110">[Alteração da Falha] Alteração do valor padrão de 'NodeVmSetType' em 'New-AzAksCluster' de 'AvailabilitySet' para 'VirtualMachineScaleSets'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="dcd6e-111">[Alteração da Falha] Alteração do valor padrão de 'NetworkPlugin' em 'New-AzAksCluster' de 'None' para 'azure'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="dcd6e-112">[Alteração da Falha] Remoção do parâmetro 'NodeOsType' em 'New-AzAksCluster', pois ele é compatível somente com um valor Linux.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="dcd6e-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="dcd6e-113">Az.Billing</span></span>
* <span data-ttu-id="dcd6e-114">Adição do cmdlet 'Get-AzBillingAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="dcd6e-115">Adição do cmdlet 'Get-AzBillingProfile'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="dcd6e-116">Adição do cmdlet 'Get-AzInvoiceSection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="dcd6e-117">Adição de novos parâmetros ao cmdlet 'Get-AzBillingInvoice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="dcd6e-118">Remoção das propriedades DownloadUrlExpiry, Type e BillingPeriodNames da resposta do cmdlet Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="dcd6e-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-119">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-120">Adição de cmdlets para dar suporte a uma funcionalidade de link privado e várias origens</span><span class="sxs-lookup"><span data-stu-id="dcd6e-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-122">Atualização do SDK para 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-123">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-124">Adição do parâmetro '-VmssId ' ao 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="dcd6e-125">Adição do parâmetro 'PlatformFaultDomainCount' ao cmdlet 'New-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-126">Novo cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="dcd6e-127">Adição dos parâmetros opcionais 'Tier' e 'LogicalSectorSize' ao cmdlet New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="dcd6e-128">Adição dos parâmetros opcionais 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' e 'DiskMBpsReadOnly' ao cmdlet 'New-AzDiskUpdateConfig'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="dcd6e-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dcd6e-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dcd6e-130">[Alteração da Falha] Atualiza a versão da API para a 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="dcd6e-130">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="dcd6e-131">[Alteração da Falha] Remoção do SKU 'Classic' e do parâmetro 'StorageAccountName' de 'New-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="dcd6e-132">Adição de novos cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule' e 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="dcd6e-133">Adição do novo parâmetro 'NetworkRuleSet' ao 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="dcd6e-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-134">Az.Databricks</span></span>
* <span data-ttu-id="dcd6e-135">Correção de um bug que pode causar a atualização do workspace do Databricks sem que ocorra falha do `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-136">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-137">Atualização do SDK do .NET do ADF para a versão 4.12.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="dcd6e-138">Atualização do SDK cliente da criptografia do ADF para a versão 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="dcd6e-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="dcd6e-139">Adição dos comandos 'Stop-AzDataFactoryV2TriggerRun' e 'Invoke-AzDataFactoryV2TriggerRun'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="dcd6e-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="dcd6e-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="dcd6e-141">Exigir a propriedade Location para criar objetos ARM de nível superior.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="dcd6e-142">\* `ApplicationGroupType` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="dcd6e-143">\* `HostPoolArmPath` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="dcd6e-144">\* Adição do `PreferredAppGroupType` ao `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="dcd6e-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="dcd6e-145">Az.Functions</span></span>
* <span data-ttu-id="dcd6e-146">[Alteração da Falha] Remoção do parâmetro de opção 'IncludeSlot' de todos os parâmetros, exceto de um conjunto de parâmetros de 'Get-AzFunctionApp'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="dcd6e-147">O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados em que '-IncludeSlot' for especificado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="dcd6e-148">Atualização do 'New-AzFunctionApp':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="dcd6e-149">Correção do -DisableApplicationInsights para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="dcd6e-150">[Nº 12728]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-150">[#12728]</span></span>
  - <span data-ttu-id="dcd6e-151">[Alteração da Falha] Remoção do suporte para criar aplicativos de funções do PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="dcd6e-152">[Alteração da Falha] Alteração da versão de runtime padrão da 6.2 para a 7.0 do Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="dcd6e-153">[Alteração da Falha] Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="dcd6e-154">[Alteração da Falha] Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-155">Az.HDInsight</span></span>
 * <span data-ttu-id="dcd6e-156">Para o cmdlet New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="dcd6e-157">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="dcd6e-158">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="dcd6e-159">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="dcd6e-160">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="dcd6e-161">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="dcd6e-162">Adição de novos parâmetros: 'StorageFileSystem' e 'StorageAccountManagedIdentity' para dar suporte ao ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="dcd6e-163">Adição do novo parâmetro 'EnableIDBroker' para dar suporte ao Agente de IDs do HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="dcd6e-164">Adição de novos parâmetros: Parâmetros 'KafkaClientGroupId', 'KafkaClientGroupName' e 'KafkaManagementNodeSize' para dar suporte ao Proxy REST do Kafka</span><span class="sxs-lookup"><span data-stu-id="dcd6e-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="dcd6e-165">Para o cmdlet New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="dcd6e-166">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="dcd6e-167">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="dcd6e-168">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="dcd6e-169">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="dcd6e-170">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="dcd6e-171">Para o cmdlet Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="dcd6e-172">Substituição do parâmetro 'StorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="dcd6e-173">Para o cmdlet Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="dcd6e-174">Substituição do parâmetro 'Domain' por 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="dcd6e-175">Remoção do requisito obrigatório para o parâmetro 'OrganizationalUnitDN'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-176">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-177">[Alteração da Falha] O parâmetro DisableSoftDelete foi preterido em 'New-AzKeyVault', bem como EnableSoftDelete em 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="dcd6e-178">[Alteração da Falha] Remoção do atributo SecretValueText para evitar a exibição de SecretValue de modo direto [Nº 12266]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="dcd6e-179">Um novo tipo de recurso é compatível: HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="dcd6e-180">Comandos CRUD de cmdlets e do HSM gerenciado para operar chaves no HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="dcd6e-181">Backup/restauração completos do HSM, criação de chave AES, backup/restauração do domínio de segurança e RBAC</span><span class="sxs-lookup"><span data-stu-id="dcd6e-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="dcd6e-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-182">Az.ManagedServices</span></span>
* <span data-ttu-id="dcd6e-183">[Alteração da Falha] Atualização de parâmetros de convenções de nomenclatura e exemplos associados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-184">Az.Network</span></span>
* <span data-ttu-id="dcd6e-185">[Alteração da Falha] Remoção do parâmetro 'HostedSubnet' e adição de 'Subnet' como alternativa</span><span class="sxs-lookup"><span data-stu-id="dcd6e-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="dcd6e-186">Adição de novos cmdlets às Rotas do Par no Nível do Roteador Virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="dcd6e-187">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="dcd6e-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="dcd6e-189">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="dcd6e-190">Adição do parâmetro '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="dcd6e-191">Adição do parâmetro '-SkuName' e, para isso, o SKU foi executado com um Alias</span><span class="sxs-lookup"><span data-stu-id="dcd6e-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="dcd6e-192">Remoção do parâmetro '-Sku'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="dcd6e-193">[Alteração da Falha] O argumento 'Connectionlink' agora é obrigatório em 'Start-AzVpnConnectionPacketCapture' e 'Stop-AzVpnConnectionPacketCapture'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="dcd6e-194">[Alteração da Falha] Atualização do 'New-AzNetworkWatcherConnectionMonitorEndPointObject' para remover o parâmetro '-Filter'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="dcd6e-195">[Alteração da Falha] Substituição do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' por 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="dcd6e-196">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndPointObject':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="dcd6e-197">Adição do parâmetro '-Type'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="dcd6e-198">Adição do parâmetro '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="dcd6e-199">Adição do parâmetro '-Scope'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="dcd6e-200">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' com o novo parâmetro '-DestinationPortBehavior'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-202">Correção da Restauração da Carga de Trabalho para permissões de colaborador.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="dcd6e-203">Adição de novos conjuntos e novas validações de parâmetros ao cmdlet Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-204">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-205">Correção de um bug de análise</span><span class="sxs-lookup"><span data-stu-id="dcd6e-205">Fixed parsing bug</span></span>
* <span data-ttu-id="dcd6e-206">Atualização de cmdlets What-If do modelo do ARM para remover uma mensagem de visualização dos resultados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="dcd6e-207">Correção de um problema em que ocorria falha nos cmdlets de implantação de modelo caso '-WhatIf' fosse definido em um escopo maior [Nº13038]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="dcd6e-208">Correção de um problema em que cmdlets de implantação de modelo não preservavam maiúsculas e minúsculas para parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="dcd6e-209">Adição de uma versão de API padrão para ser usada no cmdlet 'Export-AzResourceGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="dcd6e-210">Adição de cmdlets às Especificações de Modelo ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec' e 'Export-AzTemplateSpec')</span><span class="sxs-lookup"><span data-stu-id="dcd6e-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="dcd6e-211">Adição de um suporte para implantar Especificações de Modelo usando cmdlets de implantação existentes (por meio do novo parâmetro -TemplateSpecId)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="dcd6e-212">Atualização do parâmetro 'Get-AzResourceGroupDeploymentOperation' para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="dcd6e-213">Remoção do parâmetro '-ApiVersion' de cmdlets '\*-AzDeployment'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-214">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-215">Adição de DiffBackupIntervalInHours a 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-215">Added DiffBackupIntervalInHours to 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span> 
* <span data-ttu-id="dcd6e-216">Correção de um problema em que ocorria uma falha de New-AzSqlDatabaseExport caso networkIsolation não fosse especificado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-216">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="dcd6e-217">Correção de um problema em que New-AzSqlDatabaseExport e New-AzSqlDatabaseImport não retornavam OperationStatusLink no objeto de resultado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-217">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="dcd6e-218">Atualizar a URL de regiões emparelhadas do Azure em avisos de redundância de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-218">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-219">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-219">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-220">Remoção da propriedade obsoleta RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="dcd6e-220">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="dcd6e-221">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-221">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="dcd6e-222">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-222">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="dcd6e-223">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-223">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="dcd6e-224">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-224">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="dcd6e-225">Alterar o Tipo de DaysAfterModificationGreaterThan de int para int?</span><span class="sxs-lookup"><span data-stu-id="dcd6e-225">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="dcd6e-226">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-226">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="dcd6e-227">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-227">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="dcd6e-228">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-228">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="dcd6e-229">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-229">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="dcd6e-230">Criação/atualização de compartilhamento de arquivo compatível com uma camada de acesso</span><span class="sxs-lookup"><span data-stu-id="dcd6e-230">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="dcd6e-231">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-231">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="dcd6e-232">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-232">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="dcd6e-233">Definição/atualização/removção recursiva de ACL compatível com um item do Datalake Gen2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-233">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="dcd6e-234">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-234">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="dcd6e-235">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-235">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="dcd6e-236">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-236">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="dcd6e-237">Política de acesso de Contêiner compatível com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="dcd6e-237">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="dcd6e-238">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-238">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="dcd6e-239">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-239">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="dcd6e-240">Alteração da saída do cmdlet da política de acesso ao Contêiner get/set mudando o tipo de Permissão de propriedade filho de enum para String</span><span class="sxs-lookup"><span data-stu-id="dcd6e-240">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="dcd6e-241">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-241">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="dcd6e-242">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-242">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="dcd6e-243">Correção de um problema do script de exemplo da política de gerenciamento de conjuntos com JSON</span><span class="sxs-lookup"><span data-stu-id="dcd6e-243">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="dcd6e-244">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-244">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-245">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-245">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-246">Adição de suporte para o tipo de preço Premium V3</span><span class="sxs-lookup"><span data-stu-id="dcd6e-246">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="dcd6e-247">Atualização do SDK de Sites para a versão 3.1.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-247">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="dcd6e-248">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="dcd6e-248">Thanks to our community contributors</span></span>
* <span data-ttu-id="dcd6e-249">@atul-ram, por atualizar Get-AzDelegation.md (nº 13176)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-249">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="dcd6e-250">@dineshreddy007, por obter as Funções de Aplicativos atribuídas de modo correto em caso de registro do Stack HCI usando um token WAC.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-250">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="dcd6e-251">(nº 13249)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-251">(#13249)</span></span>
* <span data-ttu-id="dcd6e-252">@kongou-ae, por atualizar New-AzOffice365PolicyProperty.md (nº 13217)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-252">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="dcd6e-253">Lohith Chowdary Chilukuri (@Lochiluk), por atualizar Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-253">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="dcd6e-254">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-254">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="dcd6e-255">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13203)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-255">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="dcd6e-256">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13190)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-256">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="dcd6e-257">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13189)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-257">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="dcd6e-258">Adicionar links aos cmdlets referenciados (nº 13137)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-258">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="dcd6e-259">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13204)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-259">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="dcd6e-260">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13205)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-260">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="dcd6e-261">4.8.0 – Outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-261">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-262">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-263">Foi corrigido um problema de análise de datetime em bibliotecas comuns [#13045]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-263">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-264">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-264">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-265">Foi adicionado o cmdlet 'New-AzCognitiveServicesAccountApiProperty'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-265">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-266">Parâmetro 'ApiProperty' compatível com 'New-AzCognitiveServicesAccount' e 'Set-AzCognitiveServicesAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-266">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-267">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-268">Foi corrigido o problema em 'Update-ASRRecoveryPlan' populando o FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-268">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="dcd6e-269">Foram adicionados os parâmetros opcionais '-Top' e '-OrderBy' ao cmdlet 'Get-AzVmImage'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-269">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="dcd6e-270">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-270">Az.Databricks</span></span>
* <span data-ttu-id="dcd6e-271">Disponibilidade geral do módulo 'Az.Databricks'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-271">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="dcd6e-272">Foi adicionado suporte para emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-272">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-273">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-274">Foi corrigido erro de digitação nas mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="dcd6e-274">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-275">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-275">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-276">Foi adicionado o parâmetro de opção opcional 'TrustedServiceAccessEnabled' ao cmdlet 'Set-AzEventHubNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-276">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-277">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-277">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-278">Foi adicionada uma mensagem de aviso para planejamento do preterimento dos parâmetros 'PublicNetworkAccessType' e 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-278">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="dcd6e-279">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="dcd6e-280">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="dcd6e-281">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-281">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="dcd6e-282">Adicionada mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageContainer' por 'StorageContainer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-282">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="dcd6e-283">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageRootPath' por 'StorageRootPath'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-283">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-284">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-284">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-285">O SDK de dispositivos foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-285">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-286">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-287">A data detalhada da remoção da propriedade SecretValueText foi fornecida</span><span class="sxs-lookup"><span data-stu-id="dcd6e-287">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="dcd6e-288">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-288">Az.ManagedServices</span></span>
* <span data-ttu-id="dcd6e-289">Os avisos de alteração da falha nos cmdlets de definição e atribuição de serviços gerenciados foram atualizados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-289">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-290">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-290">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-291">Foi corrigido o bug que fazia com que a mensagem de aviso não pudesse ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-291">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="dcd6e-292">[#12889]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-292">[#12889]</span></span>
* <span data-ttu-id="dcd6e-293">Parâmetro 'SkipMetricValidation' com suporte nos critérios da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-293">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="dcd6e-294">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação da métrica seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-294">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-295">Az.Network</span></span>
* <span data-ttu-id="dcd6e-296">Política do Office365 adicionada ao recurso VPNSite</span><span class="sxs-lookup"><span data-stu-id="dcd6e-296">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="dcd6e-297">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-297">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-298">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-299">Foi adicionada a validação do nome do contêiner para backup da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-299">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dcd6e-300">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-300">Az.RedisCache</span></span>
* <span data-ttu-id="dcd6e-301">Correção dos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache' para não falharem devido a um problema de permissão relacionado ao registro do RP do Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-301">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-302">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-303">Foi adicionado BackupStorageRedundancy ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-303">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="dcd6e-304">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-304">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="dcd6e-305">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-305">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="dcd6e-306">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-306">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="dcd6e-307">Foi removida a diferenciação de maiúsculas e minúsculas para o parâmetro BackupStorageRedundancy em todas as referências de Banco de Dados SQL</span><span class="sxs-lookup"><span data-stu-id="dcd6e-307">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="dcd6e-308">Foram atualizados os nomes das mensagens de aviso do BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-308">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-309">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-310">Suporte para habilitar/desabilitar/obter propriedades de exclusão reversível de compartilhamento no serviço de arquivo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-310">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="dcd6e-311">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-311">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="dcd6e-312">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-312">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="dcd6e-313">Os compartilhamentos de arquivos de lista com suporte incluem os excluídos de uma conta de armazenamento e obtêm uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="dcd6e-313">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="dcd6e-314">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-314">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="dcd6e-315">Suporte para restauração de um compartilhamento de arquivo excluído</span><span class="sxs-lookup"><span data-stu-id="dcd6e-315">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="dcd6e-316">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-316">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="dcd6e-317">Foram alterados os cmdlets para modificar as propriedades do serviço blobs, não obtendo as propriedades originais do servidor, mas apenas definindo as propriedades modificadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-317">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="dcd6e-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="dcd6e-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="dcd6e-320">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-320">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="dcd6e-321">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-321">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="dcd6e-322">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-322">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="dcd6e-323">Foi corrigido o problema de ajuda para o valor padrão do tipo do parâmetro New-AzStorageAccount [#12189]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-323">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="dcd6e-324">Foi corrigido o problema adicionando exemplo para mostrar como definir o ContentType correto no upload do blob [#12989]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-324">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="dcd6e-325">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-325">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-326">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-327">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-327">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="dcd6e-328">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-328">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-329">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-329">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-330">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-330">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="dcd6e-331">[#12372]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-331">[#12372]</span></span>
* <span data-ttu-id="dcd6e-332">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-332">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="dcd6e-333">[#11239]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-333">[#11239]</span></span>
* <span data-ttu-id="dcd6e-334">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-334">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="dcd6e-335">[#11239]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-335">[#11239]</span></span>
* <span data-ttu-id="dcd6e-336">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-336">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="dcd6e-337">[#12371]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-337">[#12371]</span></span>
* <span data-ttu-id="dcd6e-338">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-338">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-339">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-339">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-340">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-340">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-341">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-341">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-342">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-342">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="dcd6e-343">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-343">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="dcd6e-344">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="dcd6e-345">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-345">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="dcd6e-346">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dcd6e-346">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="dcd6e-347">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-347">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="dcd6e-348">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-348">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="dcd6e-349">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-349">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="dcd6e-350">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-350">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="dcd6e-351">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-351">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-352">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-353">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-353">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-354">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-354">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-355">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-355">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="dcd6e-356">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-356">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="dcd6e-357">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="dcd6e-357">Az.Functions</span></span>
* <span data-ttu-id="dcd6e-358">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-358">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="dcd6e-359">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-359">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="dcd6e-360">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-360">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-361">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-361">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-362">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="dcd6e-362">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="dcd6e-363">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-363">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="dcd6e-364">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="dcd6e-364">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="dcd6e-365">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-365">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-366">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-366">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-367">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-367">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-368">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-368">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-369">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-369">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-370">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-370">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-371">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-371">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="dcd6e-372">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-372">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="dcd6e-373">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="dcd6e-373">Az.Kusto</span></span>
* <span data-ttu-id="dcd6e-374">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-374">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-375">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-375">Az.Network</span></span>
* <span data-ttu-id="dcd6e-376">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-376">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="dcd6e-377">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-377">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="dcd6e-378">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="dcd6e-378">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="dcd6e-379">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-379">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="dcd6e-380">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-380">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="dcd6e-381">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-381">Added subscription level parameter set</span></span>
    - <span data-ttu-id="dcd6e-382">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-382">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="dcd6e-383">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-383">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="dcd6e-384">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-384">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="dcd6e-385">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-385">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="dcd6e-386">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-386">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="dcd6e-387">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-387">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="dcd6e-388">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dcd6e-388">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="dcd6e-389">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-389">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="dcd6e-390">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-390">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="dcd6e-391">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-391">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="dcd6e-392">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-392">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="dcd6e-393">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-393">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="dcd6e-394">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-394">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="dcd6e-395">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-395">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="dcd6e-396">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-396">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="dcd6e-397">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-397">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="dcd6e-398">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-398">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="dcd6e-399">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-399">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-400">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-401">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-401">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-402">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-403">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-403">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="dcd6e-404">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-404">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="dcd6e-405">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="dcd6e-405">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="dcd6e-406">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-406">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-407">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-408">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-408">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="dcd6e-409">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-409">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="dcd6e-410">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-410">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="dcd6e-411">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-411">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="dcd6e-412">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-412">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="dcd6e-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="dcd6e-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="dcd6e-415">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-415">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="dcd6e-416">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-416">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="dcd6e-417">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-417">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="dcd6e-418">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-418">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="dcd6e-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="dcd6e-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="dcd6e-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="dcd6e-422">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-422">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="dcd6e-423">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-423">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-424">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-424">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-425">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-425">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="dcd6e-426">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-426">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="dcd6e-427">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-427">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="dcd6e-428">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-428">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="dcd6e-429">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-429">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="dcd6e-430">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-430">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="dcd6e-431">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-431">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="dcd6e-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="dcd6e-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="dcd6e-434">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-434">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="dcd6e-435">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-435">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="dcd6e-436">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-436">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="dcd6e-437">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="dcd6e-437">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="dcd6e-438">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-438">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="dcd6e-439">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-439">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="dcd6e-440">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-440">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="dcd6e-441">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-441">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="dcd6e-442">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-442">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-443">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-443">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-444">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-444">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="dcd6e-445">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="dcd6e-445">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="dcd6e-446">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-446">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="dcd6e-447">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-447">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="dcd6e-448">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-448">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="dcd6e-449">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-449">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="dcd6e-450">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-450">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="dcd6e-451">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-451">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="dcd6e-452">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="dcd6e-452">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="dcd6e-453">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-453">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="dcd6e-454">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-454">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="dcd6e-455">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-455">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="dcd6e-456">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-456">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="dcd6e-457">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-457">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="dcd6e-458">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-458">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="dcd6e-459">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="dcd6e-459">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="dcd6e-460">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="dcd6e-460">Thanks to our community contributors</span></span>
* <span data-ttu-id="dcd6e-461">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-461">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="dcd6e-462">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-462">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="dcd6e-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="dcd6e-464">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-464">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="dcd6e-465">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-465">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="dcd6e-466">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-466">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="dcd6e-467">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-467">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="dcd6e-468">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-468">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="dcd6e-469">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-469">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="dcd6e-470">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-470">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="dcd6e-471">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-471">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="dcd6e-472">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-472">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="dcd6e-473">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-473">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-474">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-474">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="dcd6e-475">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-475">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-476">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-476">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-477">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-477">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="dcd6e-478">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-478">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-479">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-480">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="dcd6e-480">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-481">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-482">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-482">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="dcd6e-483">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-483">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="dcd6e-484">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-484">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="dcd6e-485">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-485">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-486">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-487">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-487">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-488">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-488">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-489">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-489">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-490">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-491">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="dcd6e-491">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="dcd6e-492">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="dcd6e-492">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="dcd6e-493">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-493">Az.Maintenance</span></span>
* <span data-ttu-id="dcd6e-494">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-494">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="dcd6e-495">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-495">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="dcd6e-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-496">Az.ManagedServices</span></span>
* <span data-ttu-id="dcd6e-497">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-497">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-498">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-498">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-499">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-499">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="dcd6e-500">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="dcd6e-500">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-501">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-502">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-502">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="dcd6e-503">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-503">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="dcd6e-504">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-504">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="dcd6e-505">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="dcd6e-505">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="dcd6e-506">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-506">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="dcd6e-507">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="dcd6e-507">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="dcd6e-508">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-508">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="dcd6e-509">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="dcd6e-509">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dcd6e-510">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-510">Az.SignalR</span></span>
* <span data-ttu-id="dcd6e-511">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-511">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="dcd6e-512">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-512">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-513">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-514">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="dcd6e-514">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="dcd6e-515">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-515">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="dcd6e-516">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-516">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="dcd6e-517">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-517">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="dcd6e-518">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-518">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="dcd6e-519">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-519">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="dcd6e-520">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-520">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="dcd6e-521">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-521">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="dcd6e-522">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-522">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="dcd6e-523">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-523">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="dcd6e-524">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-524">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="dcd6e-525">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-525">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="dcd6e-526">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-526">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="dcd6e-527">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-527">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="dcd6e-528">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-528">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="dcd6e-529">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-529">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-530">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-531">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-531">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="dcd6e-532">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-532">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="dcd6e-533">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-533">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="dcd6e-534">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-534">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="dcd6e-535">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="dcd6e-535">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-536">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-536">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-537">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="dcd6e-537">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="dcd6e-538">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="dcd6e-538">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-539">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-539">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-540">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-540">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-541">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-541">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-542">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-542">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-543">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-543">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-544">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-544">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-545">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-545">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-546">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-546">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-547">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-547">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-548">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-548">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-549">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-549">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-550">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-550">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-551">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-551">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-552">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-552">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-553">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-553">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-554">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-554">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-555">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-555">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-556">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-556">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-557">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-557">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="dcd6e-558">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dcd6e-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="dcd6e-559">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-559">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="dcd6e-560">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-560">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="dcd6e-561">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dcd6e-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="dcd6e-562">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-562">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="dcd6e-563">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dcd6e-563">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-564">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-564">Az.Network</span></span>
* <span data-ttu-id="dcd6e-565">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-565">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="dcd6e-566">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-566">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="dcd6e-567">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-567">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="dcd6e-568">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-568">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-569">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-569">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-570">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-570">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="dcd6e-571">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-571">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="dcd6e-572">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-572">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-574">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-574">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-575">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-576">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-576">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="dcd6e-577">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-577">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-578">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-578">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-579">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-579">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="dcd6e-580">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="dcd6e-580">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-581">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-582">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="dcd6e-582">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="dcd6e-583">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-583">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="dcd6e-584">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="dcd6e-584">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="dcd6e-585">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="dcd6e-585">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="dcd6e-586">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="dcd6e-586">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="dcd6e-587">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="dcd6e-587">Supported get single file share usage</span></span>
    - <span data-ttu-id="dcd6e-588">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-588">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="dcd6e-589">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-589">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-590">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-591">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-591">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="dcd6e-592">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-592">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-593">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-593">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-594">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-594">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dcd6e-595">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-595">Az.AnalysisServices</span></span>
* <span data-ttu-id="dcd6e-596">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-596">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-597">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-597">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-598">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-598">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-599">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-599">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-600">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-600">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-601">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-602">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-602">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dcd6e-603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dcd6e-603">Az.EventGrid</span></span>
* <span data-ttu-id="dcd6e-604">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-604">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="dcd6e-605">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-605">Added new features:</span></span>
    - <span data-ttu-id="dcd6e-606">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-606">Input mapping</span></span>
    - <span data-ttu-id="dcd6e-607">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-607">Event Delivery Schema</span></span>
    - <span data-ttu-id="dcd6e-608">Link Privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-608">Private Link</span></span>
    - <span data-ttu-id="dcd6e-609">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="dcd6e-609">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="dcd6e-610">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="dcd6e-610">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="dcd6e-611">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="dcd6e-611">Azure Function As Destination</span></span>
    - <span data-ttu-id="dcd6e-612">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-612">WebHook Batching</span></span>
    - <span data-ttu-id="dcd6e-613">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-613">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="dcd6e-614">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="dcd6e-614">IpFiltering</span></span>
* <span data-ttu-id="dcd6e-615">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-615">Updated cmdlets:</span></span>
    - <span data-ttu-id="dcd6e-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="dcd6e-617">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-617">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="dcd6e-618">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-618">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="dcd6e-619">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-619">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="dcd6e-620">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-620">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="dcd6e-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="dcd6e-622">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-622">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="dcd6e-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="dcd6e-624">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-624">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-625">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-625">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-626">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="dcd6e-626">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="dcd6e-627">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-627">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-628">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-628">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-629">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-629">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-630">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-630">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-631">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-631">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-632">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-632">Az.Network</span></span>
* <span data-ttu-id="dcd6e-633">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-633">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="dcd6e-634">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-634">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="dcd6e-635">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-635">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="dcd6e-636">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-636">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="dcd6e-637">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-637">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="dcd6e-638">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-638">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="dcd6e-639">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-639">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="dcd6e-640">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-640">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="dcd6e-641">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-641">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="dcd6e-642">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-642">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="dcd6e-643">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-643">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="dcd6e-644">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-644">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="dcd6e-645">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-645">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="dcd6e-646">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-646">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="dcd6e-647">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-647">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="dcd6e-648">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-648">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="dcd6e-649">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-649">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-651">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-651">Removed project reference to Authentication</span></span>
* <span data-ttu-id="dcd6e-652">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-652">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="dcd6e-653">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-653">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-654">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-654">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-655">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-655">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="dcd6e-656">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-656">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-657">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-657">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-658">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-658">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="dcd6e-659">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-659">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="dcd6e-660">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-660">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-661">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-661">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-662">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-662">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="dcd6e-663">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="dcd6e-663">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="dcd6e-664">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-664">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="dcd6e-665">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-665">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="dcd6e-666">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-666">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="dcd6e-667">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-667">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="dcd6e-668">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="dcd6e-668">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="dcd6e-669">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-669">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="dcd6e-670">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="dcd6e-670">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="dcd6e-671">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-671">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="dcd6e-672">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-672">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="dcd6e-673">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="dcd6e-673">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="dcd6e-674">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-674">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="dcd6e-675">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-675">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="dcd6e-676">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-676">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="dcd6e-677">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-677">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="dcd6e-678">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-678">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dcd6e-679">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dcd6e-679">Az.StorageSync</span></span>
* <span data-ttu-id="dcd6e-680">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="dcd6e-680">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="dcd6e-681">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-681">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="dcd6e-682">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-682">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="dcd6e-683">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-683">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-684">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-685">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-685">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="dcd6e-686">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-686">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-687">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-687">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-688">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-688">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="dcd6e-689">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-689">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="dcd6e-690">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-690">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="dcd6e-691">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-691">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-692">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-692">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-693">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-693">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dcd6e-694">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-694">Az.Batch</span></span>
* <span data-ttu-id="dcd6e-695">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-695">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="dcd6e-696">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-696">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-698">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-698">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="dcd6e-699">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-699">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-700">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-701">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-701">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="dcd6e-702">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-702">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="dcd6e-703">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-703">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="dcd6e-704">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-704">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="dcd6e-705">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="dcd6e-705">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-706">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-706">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-707">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-707">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-708">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-708">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-709">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-709">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="dcd6e-710">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="dcd6e-710">Az.Functions</span></span>
* <span data-ttu-id="dcd6e-711">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="dcd6e-711">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-712">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-712">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-713">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-713">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dcd6e-714">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dcd6e-714">Az.HealthcareApis</span></span>
* <span data-ttu-id="dcd6e-715">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-715">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="dcd6e-716">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-716">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-717">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-717">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-718">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-718">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="dcd6e-719">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-719">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-720">Az.Network</span></span>
* <span data-ttu-id="dcd6e-721">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-721">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="dcd6e-722">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-722">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="dcd6e-723">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-723">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="dcd6e-724">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="dcd6e-724">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="dcd6e-725">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="dcd6e-725">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="dcd6e-726">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-726">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="dcd6e-727">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-727">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="dcd6e-728">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-728">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="dcd6e-729">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-729">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="dcd6e-730">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-730">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="dcd6e-731">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-731">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="dcd6e-732">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-732">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="dcd6e-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="dcd6e-734">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-734">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="dcd6e-735">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-735">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="dcd6e-736">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-736">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="dcd6e-737">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-737">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="dcd6e-738">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-738">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="dcd6e-739">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-739">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="dcd6e-740">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-740">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="dcd6e-741">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="dcd6e-741">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="dcd6e-742">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="dcd6e-742">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="dcd6e-743">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="dcd6e-743">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="dcd6e-744">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-744">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="dcd6e-745">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="dcd6e-746">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-746">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="dcd6e-747">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-747">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="dcd6e-748">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-748">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="dcd6e-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="dcd6e-755">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-755">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="dcd6e-756">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-756">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="dcd6e-757">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-757">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="dcd6e-758">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-758">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="dcd6e-759">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-759">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="dcd6e-760">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-760">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="dcd6e-761">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-761">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="dcd6e-762">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-762">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="dcd6e-763">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-763">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="dcd6e-764">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-764">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="dcd6e-765">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-765">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="dcd6e-766">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-766">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="dcd6e-767">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-767">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="dcd6e-768">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-768">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="dcd6e-769">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-769">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-770">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-770">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-771">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-771">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="dcd6e-772">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-772">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="dcd6e-773">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="dcd6e-773">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="dcd6e-774">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-774">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="dcd6e-775">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-775">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-776">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-777">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-777">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="dcd6e-778">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-778">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-779">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-780">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-780">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="dcd6e-781">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-781">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="dcd6e-782">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-782">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="dcd6e-783">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-783">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="dcd6e-784">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="dcd6e-784">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="dcd6e-785">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="dcd6e-785">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-786">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-787">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="dcd6e-787">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="dcd6e-788">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-788">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="dcd6e-789">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-789">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-790">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-790">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-791">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="dcd6e-791">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="dcd6e-792">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-792">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="dcd6e-793">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-793">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-794">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-795">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-795">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="dcd6e-796">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-796">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="dcd6e-797">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-797">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="dcd6e-798">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-798">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="dcd6e-799">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="dcd6e-799">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="dcd6e-800">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-800">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="dcd6e-801">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-801">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-802">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-803">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-803">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dcd6e-804">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-804">Az.AnalysisServices</span></span>
* <span data-ttu-id="dcd6e-805">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-805">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-806">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-807">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-807">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="dcd6e-808">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="dcd6e-808">Az.Billing</span></span>
* <span data-ttu-id="dcd6e-809">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-809">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-810">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-810">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-811">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-811">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-812">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-813">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-813">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="dcd6e-814">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-814">Az.DataShare</span></span>
* <span data-ttu-id="dcd6e-815">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="dcd6e-815">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="dcd6e-816">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="dcd6e-816">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="dcd6e-817">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="dcd6e-817">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-818">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-818">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-819">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-819">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="dcd6e-820">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="dcd6e-820">Added optional parameters to</span></span> 
    - <span data-ttu-id="dcd6e-821">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-821">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="dcd6e-822">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-822">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-823">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-823">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-824">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-824">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="dcd6e-825">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="dcd6e-825">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="dcd6e-826">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-826">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="dcd6e-827">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="dcd6e-827">Az.PrivateDns</span></span>
* <span data-ttu-id="dcd6e-828">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-828">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-829">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-830">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-830">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="dcd6e-831">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="dcd6e-831">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-832">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-833">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="dcd6e-833">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="dcd6e-834">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="dcd6e-834">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="dcd6e-835">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-835">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="dcd6e-836">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-836">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="dcd6e-837">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-837">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-838">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-839">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-839">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="dcd6e-840">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-840">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="dcd6e-841">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="dcd6e-841">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-842">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-843">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-843">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="dcd6e-844">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-844">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="dcd6e-845">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="dcd6e-845">Highlights since the last release</span></span>
* <span data-ttu-id="dcd6e-846">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="dcd6e-846">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="dcd6e-847">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="dcd6e-847">General availability of Az.Functions</span></span> 
* <span data-ttu-id="dcd6e-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="dcd6e-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-849">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-850">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-850">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="dcd6e-851">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="dcd6e-851">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-852">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-852">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-853">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="dcd6e-853">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="dcd6e-854">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="dcd6e-854">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="dcd6e-855">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-855">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-856">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-856">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-857">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-857">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="dcd6e-858">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-858">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="dcd6e-859">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-859">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="dcd6e-860">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-860">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="dcd6e-861">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-861">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="dcd6e-862">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-862">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="dcd6e-863">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-863">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="dcd6e-864">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-864">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="dcd6e-865">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-865">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="dcd6e-866">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-866">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="dcd6e-867">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-867">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="dcd6e-868">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-868">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="dcd6e-869">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-869">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="dcd6e-870">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-870">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="dcd6e-871">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-871">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="dcd6e-872">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-872">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="dcd6e-873">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-873">Az.ApplicationInsights</span></span>
* <span data-ttu-id="dcd6e-874">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-874">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="dcd6e-875">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-875">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="dcd6e-876">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-876">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dcd6e-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-877">Az.Batch</span></span>
* <span data-ttu-id="dcd6e-878">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-878">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="dcd6e-879">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-879">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="dcd6e-880">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-880">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="dcd6e-881">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-881">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="dcd6e-882">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-882">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="dcd6e-883">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-883">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="dcd6e-884">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-884">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="dcd6e-885">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-885">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="dcd6e-886">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-886">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-887">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-887">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-888">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-888">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="dcd6e-889">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-889">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="dcd6e-890">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="dcd6e-890">Breaking changes</span></span>
    - <span data-ttu-id="dcd6e-891">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-891">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="dcd6e-892">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-892">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="dcd6e-893">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-893">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="dcd6e-894">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-894">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="dcd6e-895">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-895">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="dcd6e-896">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-896">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="dcd6e-897">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-897">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-898">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-899">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-899">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-900">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-901">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="dcd6e-901">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="dcd6e-902">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="dcd6e-902">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="dcd6e-903">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-903">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="dcd6e-904">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="dcd6e-904">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="dcd6e-905">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="dcd6e-905">Az.Functions</span></span>
* <span data-ttu-id="dcd6e-906">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="dcd6e-906">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-907">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-907">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-908">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-908">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dcd6e-909">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dcd6e-909">Az.HealthcareApis</span></span>
* <span data-ttu-id="dcd6e-910">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-910">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-911">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-911">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-912">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-912">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="dcd6e-913">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-913">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="dcd6e-914">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-914">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="dcd6e-915">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-915">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="dcd6e-916">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-916">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="dcd6e-917">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-917">New cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-918">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-918">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="dcd6e-919">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-919">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="dcd6e-920">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-920">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="dcd6e-921">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-921">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="dcd6e-922">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-922">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="dcd6e-923">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-923">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-924">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-924">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-925">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-925">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="dcd6e-926">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="dcd6e-926">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="dcd6e-927">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="dcd6e-927">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="dcd6e-928">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-928">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="dcd6e-929">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="dcd6e-929">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="dcd6e-930">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-930">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="dcd6e-931">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-931">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-932">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-932">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-933">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-933">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="dcd6e-934">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-934">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="dcd6e-935">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-935">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="dcd6e-936">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="dcd6e-936">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="dcd6e-937">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-937">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="dcd6e-938">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-938">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="dcd6e-939">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-939">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-940">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-940">Az.Network</span></span>
* <span data-ttu-id="dcd6e-941">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-941">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="dcd6e-942">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-942">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="dcd6e-943">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-943">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="dcd6e-944">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-944">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="dcd6e-945">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dcd6e-945">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="dcd6e-946">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-946">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-947">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dcd6e-947">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="dcd6e-948">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dcd6e-948">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="dcd6e-949">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dcd6e-949">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="dcd6e-950">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dcd6e-950">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="dcd6e-951">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-951">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="dcd6e-952">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-952">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="dcd6e-953">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-953">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="dcd6e-954">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-954">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="dcd6e-955">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-955">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="dcd6e-956">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-956">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="dcd6e-957">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-957">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="dcd6e-958">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-958">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="dcd6e-959">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-959">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="dcd6e-960">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-960">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="dcd6e-961">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-961">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="dcd6e-962">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-962">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="dcd6e-963">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-963">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="dcd6e-964">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-964">Updated cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-965">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dcd6e-965">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-966">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-966">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-967">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-967">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="dcd6e-968">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-968">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="dcd6e-969">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="dcd6e-969">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="dcd6e-970">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="dcd6e-970">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="dcd6e-971">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="dcd6e-971">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="dcd6e-972">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-972">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="dcd6e-973">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-973">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="dcd6e-974">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-974">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-975">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-975">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-976">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-976">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="dcd6e-977">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-977">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="dcd6e-978">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-978">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="dcd6e-979">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-979">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="dcd6e-980">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-980">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-981">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-982">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="dcd6e-982">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="dcd6e-983">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-983">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="dcd6e-984">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-984">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="dcd6e-985">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-985">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="dcd6e-986">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-986">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="dcd6e-987">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-987">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="dcd6e-988">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-988">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="dcd6e-989">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-989">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="dcd6e-990">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-990">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="dcd6e-991">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-991">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="dcd6e-992">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-992">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="dcd6e-993">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-993">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="dcd6e-994">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-994">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="dcd6e-995">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="dcd6e-995">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="dcd6e-996">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="dcd6e-996">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="dcd6e-997">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="dcd6e-997">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="dcd6e-998">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-998">'New-AzDeployment'</span></span>
    - <span data-ttu-id="dcd6e-999">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-999">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="dcd6e-1000">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1000">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="dcd6e-1001">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1001">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-1002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1002">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-1003">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1003">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1004">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1005">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1005">Enhance performance of:</span></span>
    - <span data-ttu-id="dcd6e-1006">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1006">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="dcd6e-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="dcd6e-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="dcd6e-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="dcd6e-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="dcd6e-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="dcd6e-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="dcd6e-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="dcd6e-1014">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1014">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="dcd6e-1015">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1015">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1016">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1017">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1017">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="dcd6e-1018">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1018">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="dcd6e-1019">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1019">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="dcd6e-1020">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1020">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="dcd6e-1021">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1021">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="dcd6e-1022">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1022">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="dcd6e-1023">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1023">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="dcd6e-1024">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1024">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="dcd6e-1025">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1025">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="dcd6e-1026">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1026">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="dcd6e-1027">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1027">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="dcd6e-1028">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1028">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="dcd6e-1029">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1029">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="dcd6e-1030">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1030">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="dcd6e-1031">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1031">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="dcd6e-1032">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1032">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="dcd6e-1033">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1033">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="dcd6e-1034">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1034">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="dcd6e-1035">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1035">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="dcd6e-1036">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1036">Supported failover Storage account</span></span>
    - <span data-ttu-id="dcd6e-1037">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1037">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="dcd6e-1038">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1038">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="dcd6e-1039">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1039">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="dcd6e-1040">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1040">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="dcd6e-1041">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1041">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="dcd6e-1042">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1042">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="dcd6e-1043">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1043">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="dcd6e-1044">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1044">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="dcd6e-1045">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1045">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="dcd6e-1046">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1046">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="dcd6e-1047">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1047">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="dcd6e-1048">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1048">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="dcd6e-1049">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1049">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="dcd6e-1050">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1050">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="dcd6e-1051">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1051">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="dcd6e-1052">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1052">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="dcd6e-1053">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1053">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="dcd6e-1054">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1054">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="dcd6e-1055">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1055">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="dcd6e-1056">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1056">Az.TrafficManager</span></span>
* <span data-ttu-id="dcd6e-1057">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1057">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1058">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-1059">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1059">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="dcd6e-1060">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1060">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="dcd6e-1061">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1061">Highlights since the last release</span></span>
* <span data-ttu-id="dcd6e-1062">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1062">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1063">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1063">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1064">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1064">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-1065">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1065">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-1066">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1066">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="dcd6e-1067">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1067">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1068">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-1069">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1069">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-1071">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1071">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1072">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1073">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1073">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-1074">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1074">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-1075">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1075">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-1076">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1076">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1077">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1077">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="dcd6e-1078">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1078">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="dcd6e-1079">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1079">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="dcd6e-1080">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1080">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1081">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1081">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="dcd6e-1082">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1082">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="dcd6e-1083">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1083">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="dcd6e-1084">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1084">New cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1085">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1085">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-1086">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1086">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-1087">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1087">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="dcd6e-1088">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1088">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="dcd6e-1089">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1089">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-1090">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1090">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-1091">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1091">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="dcd6e-1092">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1092">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="dcd6e-1093">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1093">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="dcd6e-1094">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1094">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="dcd6e-1095">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1095">Az.Maintenance</span></span>
* <span data-ttu-id="dcd6e-1096">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1096">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1097">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-1098">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1098">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="dcd6e-1099">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1099">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dcd6e-1100">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1100">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dcd6e-1101">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1101">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dcd6e-1102">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1102">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="dcd6e-1103">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1103">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="dcd6e-1104">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1104">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="dcd6e-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1106">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1107">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1107">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="dcd6e-1108">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1108">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="dcd6e-1109">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1109">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="dcd6e-1110">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1110">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="dcd6e-1111">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1111">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="dcd6e-1112">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1112">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="dcd6e-1113">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1113">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="dcd6e-1114">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1114">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="dcd6e-1115">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1115">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="dcd6e-1116">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1116">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="dcd6e-1117">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1117">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="dcd6e-1118">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1118">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="dcd6e-1119">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1119">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="dcd6e-1120">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1120">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="dcd6e-1121">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1121">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="dcd6e-1122">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1122">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-1123">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1123">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-1124">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1124">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="dcd6e-1125">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1125">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-1126">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1126">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-1127">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1127">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1128">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1128">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1129">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1129">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="dcd6e-1130">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1130">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1131">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1132">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1132">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="dcd6e-1133">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1133">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="dcd6e-1134">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1134">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="dcd6e-1135">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1135">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="dcd6e-1136">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1136">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="dcd6e-1137">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1137">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dcd6e-1138">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1138">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dcd6e-1139">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1139">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="dcd6e-1140">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1140">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dcd6e-1141">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1141">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="dcd6e-1142">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1142">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="dcd6e-1143">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1143">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="dcd6e-1144">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1144">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="dcd6e-1145">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1145">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="dcd6e-1146">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1146">General</span></span>
* <span data-ttu-id="dcd6e-1147">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1147">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="dcd6e-1148">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1148">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="dcd6e-1149">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1149">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="dcd6e-1150">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1150">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="dcd6e-1151">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1151">Az.Billing</span></span>
  - <span data-ttu-id="dcd6e-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1152">Az.Compute</span></span>
  - <span data-ttu-id="dcd6e-1153">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1153">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="dcd6e-1154">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1154">Az.EventHub</span></span>
  - <span data-ttu-id="dcd6e-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1155">Az.IotHub</span></span>
  - <span data-ttu-id="dcd6e-1156">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1156">Az.KeyVault</span></span>
  - <span data-ttu-id="dcd6e-1157">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1157">Az.Monitor</span></span>
  - <span data-ttu-id="dcd6e-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1158">Az.Network</span></span>
  - <span data-ttu-id="dcd6e-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1159">Az.Resources</span></span>
  - <span data-ttu-id="dcd6e-1160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1160">Az.Storage</span></span>
  - <span data-ttu-id="dcd6e-1161">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1161">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-1162">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1162">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-1163">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1163">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="dcd6e-1164">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1164">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="dcd6e-1165">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1165">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1166">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1166">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1167">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1167">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1168">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1169">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1169">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="dcd6e-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="dcd6e-1171">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1171">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-1172">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1172">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="dcd6e-1173">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1173">[#11354]</span></span>
* <span data-ttu-id="dcd6e-1174">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1174">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="dcd6e-1175">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1175">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="dcd6e-1176">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1176">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="dcd6e-1177">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1177">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="dcd6e-1178">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1178">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="dcd6e-1179">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1179">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="dcd6e-1180">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1180">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="dcd6e-1181">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1181">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="dcd6e-1182">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1182">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1183">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1184">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1184">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="dcd6e-1185">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1185">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-1186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1186">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-1187">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1187">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="dcd6e-1188">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1188">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-1189">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1189">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-1190">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1190">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-1191">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1191">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-1192">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1192">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="dcd6e-1193">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1193">New Cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1194">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1194">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="dcd6e-1195">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1195">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-1196">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1196">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-1197">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1197">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-1198">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1198">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-1199">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1199">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1200">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1201">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1201">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="dcd6e-1202">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1202">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="dcd6e-1203">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1203">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="dcd6e-1204">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1204">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="dcd6e-1205">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1205">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="dcd6e-1206">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1206">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-1207">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1207">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-1208">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1208">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-1209">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1209">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-1210">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1210">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="dcd6e-1211">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1211">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="dcd6e-1212">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1212">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="dcd6e-1213">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1213">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="dcd6e-1214">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1214">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="dcd6e-1215">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1215">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1216">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1216">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1217">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1217">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="dcd6e-1218">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1218">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="dcd6e-1219">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1219">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="dcd6e-1220">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1220">Added example.</span></span>
* <span data-ttu-id="dcd6e-1221">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1221">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="dcd6e-1222">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1222">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1223">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1224">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1224">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="dcd6e-1225">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1225">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="dcd6e-1226">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1226">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="dcd6e-1227">Az.Support</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1227">Az.Support</span></span>
* <span data-ttu-id="dcd6e-1228">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1228">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-1229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1229">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-1230">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1230">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="dcd6e-1231">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1231">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="dcd6e-1232">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1232">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="dcd6e-1233">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1233">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="dcd6e-1234">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1234">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="dcd6e-1235">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1235">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1236">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1237">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1237">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="dcd6e-1238">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1238">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="dcd6e-1239">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1239">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-1240">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1240">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-1241">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1241">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="dcd6e-1242">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1242">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="dcd6e-1243">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1243">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="dcd6e-1244">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1244">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-1246">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1246">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-1247">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1247">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-1248">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1248">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="dcd6e-1249">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1249">New Cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1250">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1250">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dcd6e-1251">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1251">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dcd6e-1252">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1252">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dcd6e-1253">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1253">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="dcd6e-1254">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1254">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="dcd6e-1255">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1255">New Cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1256">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1256">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="dcd6e-1257">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1257">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="dcd6e-1258">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1258">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="dcd6e-1259">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1259">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="dcd6e-1260">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1260">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="dcd6e-1261">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1261">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="dcd6e-1262">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1262">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="dcd6e-1263">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1263">New Cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1264">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1264">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="dcd6e-1265">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1265">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="dcd6e-1266">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1266">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-1267">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1267">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-1268">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1268">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1269">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1269">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1270">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1270">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="dcd6e-1271">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1271">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="dcd6e-1272">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1272">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="dcd6e-1273">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1273">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1274">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1274">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1275">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1275">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="dcd6e-1276">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1276">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="dcd6e-1277">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1277">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="dcd6e-1278">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1278">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="dcd6e-1279">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1279">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="dcd6e-1280">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1280">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="dcd6e-1281">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1281">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="dcd6e-1282">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1282">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="dcd6e-1283">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1283">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="dcd6e-1284">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1284">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="dcd6e-1285">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1285">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="dcd6e-1286">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1286">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="dcd6e-1287">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1287">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="dcd6e-1288">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1288">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1289">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1290">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1290">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="dcd6e-1291">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1291">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="dcd6e-1292">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1292">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="dcd6e-1293">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1293">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="dcd6e-1294">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1294">Remove an LTR backup</span></span>
    - <span data-ttu-id="dcd6e-1295">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1295">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="dcd6e-1296">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1296">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="dcd6e-1297">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1297">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="dcd6e-1298">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1298">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1299">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1299">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1300">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1300">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="dcd6e-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="dcd6e-1302">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1302">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="dcd6e-1303">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1303">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="dcd6e-1304">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1304">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1305">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-1306">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1306">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="dcd6e-1307">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1307">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="dcd6e-1308">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1308">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="dcd6e-1309">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1309">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="dcd6e-1310">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1310">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="dcd6e-1311">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1311">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dcd6e-1312">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="dcd6e-1313">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1313">Updated client side telemetry.</span></span>
* <span data-ttu-id="dcd6e-1314">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1314">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="dcd6e-1315">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1315">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1316">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1317">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1317">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-1318">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1318">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-1319">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1319">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-1320">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1320">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-1321">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1321">Updated SDK to 7.0</span></span>
* <span data-ttu-id="dcd6e-1322">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1322">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1323">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1323">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1324">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1324">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-1326">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1326">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1327">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-1328">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1328">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="dcd6e-1329">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1329">New Cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1330">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1330">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dcd6e-1331">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1331">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dcd6e-1332">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1332">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="dcd6e-1333">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1333">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-1334">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1334">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-1335">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1335">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-1336">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1336">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-1337">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1337">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="dcd6e-1338">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1338">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="dcd6e-1339">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1339">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1340">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1341">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1341">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-1342">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1342">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="dcd6e-1343">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1343">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="dcd6e-1344">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1344">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="dcd6e-1345">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1345">No new cmdlets are added.</span></span> <span data-ttu-id="dcd6e-1346">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1346">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-1347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1347">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-1348">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1348">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1349">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1350">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1350">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="dcd6e-1351">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1351">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="dcd6e-1352">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1352">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="dcd6e-1353">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1353">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="dcd6e-1354">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1354">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="dcd6e-1355">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1355">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="dcd6e-1356">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1356">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="dcd6e-1357">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1357">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1358">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1359">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1359">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="dcd6e-1360">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1360">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="dcd6e-1361">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1361">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="dcd6e-1362">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1362">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="dcd6e-1363">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1363">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dcd6e-1364">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1364">Az.StorageSync</span></span>
* <span data-ttu-id="dcd6e-1365">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1365">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="dcd6e-1366">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1366">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dcd6e-1367">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1367">Highlights since the last major release</span></span>
* <span data-ttu-id="dcd6e-1368">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1368">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="dcd6e-1369">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1369">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1370">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1370">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1371">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1371">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="dcd6e-1372">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1372">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-1373">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1373">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-1374">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1374">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="dcd6e-1375">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1375">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="dcd6e-1376">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1376">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="dcd6e-1377">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1377">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1378">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1379">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1379">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="dcd6e-1380">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1380">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="dcd6e-1381">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1381">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="dcd6e-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="dcd6e-1383">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1383">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1384">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1384">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1385">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1385">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="dcd6e-1386">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1386">Az.DeploymentManager</span></span>
* <span data-ttu-id="dcd6e-1387">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1387">Adds LIST operations for resources</span></span>
* <span data-ttu-id="dcd6e-1388">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1388">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-1389">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1389">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-1390">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1390">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-1391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1391">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-1392">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1392">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1393">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1394">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1394">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="dcd6e-1395">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1395">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="dcd6e-1396">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1396">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-1397">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1397">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="dcd6e-1398">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1398">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="dcd6e-1399">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1399">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="dcd6e-1400">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1400">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="dcd6e-1401">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1401">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="dcd6e-1402">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1402">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="dcd6e-1404">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1404">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="dcd6e-1405">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1405">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="dcd6e-1406">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1406">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-1407">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1407">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-1408">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1408">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="dcd6e-1409">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1409">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="dcd6e-1410">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1410">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="dcd6e-1411">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1411">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-1412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1412">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-1413">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1413">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="dcd6e-1414">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1414">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1415">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1416">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1416">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="dcd6e-1417">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1417">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1418">Az.Sql</span></span>
<span data-ttu-id="dcd6e-1419">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1419">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1420">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1421">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1421">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="dcd6e-1422">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1422">New-AzStorageAccount</span></span>
* <span data-ttu-id="dcd6e-1423">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1423">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="dcd6e-1424">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1424">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1425">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-1426">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1426">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="dcd6e-1427">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1427">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="dcd6e-1428">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1428">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1429">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1429">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1430">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1430">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1431">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-1432">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1432">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1433">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1434">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1434">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="dcd6e-1435">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1435">Az.ContainerInstance</span></span>
* <span data-ttu-id="dcd6e-1436">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1436">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="dcd6e-1437">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1437">Az.DataBoxEdge</span></span>
* <span data-ttu-id="dcd6e-1438">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1438">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dcd6e-1439">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1439">Get the Edge Storage Container</span></span>
* <span data-ttu-id="dcd6e-1440">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1440">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dcd6e-1441">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1441">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="dcd6e-1442">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1442">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dcd6e-1443">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1443">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="dcd6e-1444">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1444">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="dcd6e-1445">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1445">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="dcd6e-1446">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1446">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dcd6e-1447">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1447">Get the Edge Storage Account</span></span>
* <span data-ttu-id="dcd6e-1448">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1448">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dcd6e-1449">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1449">Create new Edge Storage Account</span></span>
* <span data-ttu-id="dcd6e-1450">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1450">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="dcd6e-1451">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1451">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="dcd6e-1452">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1452">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="dcd6e-1453">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1453">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="dcd6e-1454">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1454">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="dcd6e-1455">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1455">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1456">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1457">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1457">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="dcd6e-1458">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1458">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="dcd6e-1459">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1459">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="dcd6e-1460">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1460">Az.DevTestLabs</span></span>
* <span data-ttu-id="dcd6e-1461">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1461">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-1462">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1462">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-1463">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1463">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-1464">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1464">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-1465">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1465">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="dcd6e-1466">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1466">Az.MachineLearning</span></span>
* <span data-ttu-id="dcd6e-1467">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1467">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="dcd6e-1468">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1468">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="dcd6e-1469">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1469">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="dcd6e-1470">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1470">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="dcd6e-1471">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1471">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="dcd6e-1472">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1472">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="dcd6e-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="dcd6e-1474">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1474">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1475">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1476">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1476">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-1477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1477">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-1478">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1478">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="dcd6e-1479">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="dcd6e-1480">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1480">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="dcd6e-1481">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1481">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1482">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1483">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1483">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1484">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1485">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1485">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="dcd6e-1486">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1486">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="dcd6e-1487">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1487">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="dcd6e-1488">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1488">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1489">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1489">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1490">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1490">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="dcd6e-1491">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1491">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="dcd6e-1492">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1492">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="dcd6e-1493">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1493">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="dcd6e-1494">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1494">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="dcd6e-1495">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1495">General</span></span>
* <span data-ttu-id="dcd6e-1496">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1496">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1497">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1498">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1498">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="dcd6e-1499">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1499">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dcd6e-1500">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1500">Az.Batch</span></span>
* <span data-ttu-id="dcd6e-1501">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1501">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1502">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1503">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1503">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-1504">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1504">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-1505">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1505">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="dcd6e-1506">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1506">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dcd6e-1507">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1507">Az.HealthcareApis</span></span>
* <span data-ttu-id="dcd6e-1508">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1508">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1509">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-1510">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1510">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="dcd6e-1511">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1511">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="dcd6e-1512">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1512">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-1513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1513">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-1514">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1514">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="dcd6e-1515">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1515">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="dcd6e-1516">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1516">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1517">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1517">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1518">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1518">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1519">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1520">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1520">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="dcd6e-1521">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1521">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1522">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1523">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1523">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1524">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1524">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1525">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1525">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="dcd6e-1526">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1526">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="dcd6e-1527">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1527">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="dcd6e-1528">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1528">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="dcd6e-1529">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1529">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="dcd6e-1530">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1530">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="dcd6e-1531">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1531">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="dcd6e-1532">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1532">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="dcd6e-1533">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1533">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="dcd6e-1534">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1534">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="dcd6e-1535">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1535">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="dcd6e-1536">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1536">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="dcd6e-1537">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1537">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="dcd6e-1538">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1538">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dcd6e-1539">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1539">Highlights since the last major release</span></span>
* <span data-ttu-id="dcd6e-1540">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1540">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="dcd6e-1541">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1541">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1542">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1543">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1543">VM Reapply feature</span></span>
    - <span data-ttu-id="dcd6e-1544">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1544">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="dcd6e-1545">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1545">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="dcd6e-1546">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1546">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="dcd6e-1547">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1547">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="dcd6e-1548">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1548">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="dcd6e-1549">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1549">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="dcd6e-1550">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1550">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="dcd6e-1551">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1551">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="dcd6e-1552">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1552">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="dcd6e-1553">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1553">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="dcd6e-1554">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1554">Az.DataBoxEdge</span></span>
* <span data-ttu-id="dcd6e-1555">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1555">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dcd6e-1556">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1556">Get the Order</span></span>
* <span data-ttu-id="dcd6e-1557">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1557">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dcd6e-1558">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1558">Create new Order</span></span>
* <span data-ttu-id="dcd6e-1559">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1559">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="dcd6e-1560">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1560">Remove the Order</span></span>
* <span data-ttu-id="dcd6e-1561">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1561">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="dcd6e-1562">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1562">Now creates Local Share</span></span>
* <span data-ttu-id="dcd6e-1563">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1563">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="dcd6e-1564">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1564">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="dcd6e-1565">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1565">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="dcd6e-1566">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1566">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="dcd6e-1567">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1567">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dcd6e-1568">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1568">Gets the information about Triggers</span></span>
* <span data-ttu-id="dcd6e-1569">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1569">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dcd6e-1570">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1570">Create new Triggers</span></span>
* <span data-ttu-id="dcd6e-1571">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1571">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="dcd6e-1572">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1572">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1573">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1573">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1574">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1574">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="dcd6e-1575">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1575">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-1576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1576">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-1577">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1577">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-1578">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1578">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-1579">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1579">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-1580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1580">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-1581">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1581">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="dcd6e-1582">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1582">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="dcd6e-1583">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1583">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="dcd6e-1584">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1584">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1585">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1586">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1586">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="dcd6e-1587">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1587">Az.PrivateDns</span></span>
* <span data-ttu-id="dcd6e-1588">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1588">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-1589">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1589">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-1590">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1590">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="dcd6e-1591">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1591">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="dcd6e-1592">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1592">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dcd6e-1593">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1593">Az.RedisCache</span></span>
* <span data-ttu-id="dcd6e-1594">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1594">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="dcd6e-1595">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1595">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="dcd6e-1596">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1596">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1597">Az.Resources</span></span>
- <span data-ttu-id="dcd6e-1598">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1598">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="dcd6e-1599">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1599">Updated create policy definition help example</span></span>
- <span data-ttu-id="dcd6e-1600">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1600">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="dcd6e-1601">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1601">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="dcd6e-1602">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1602">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1603">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1604">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1604">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="dcd6e-1605">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1605">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="dcd6e-1606">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1606">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="dcd6e-1607">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1607">General</span></span>
* <span data-ttu-id="dcd6e-1608">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1608">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1609">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1609">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1610">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1610">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="dcd6e-1611">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1611">Az.Advisor</span></span>
* <span data-ttu-id="dcd6e-1612">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1612">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dcd6e-1613">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1613">Az.Batch</span></span>
* <span data-ttu-id="dcd6e-1614">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1614">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="dcd6e-1615">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1615">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="dcd6e-1616">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1616">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="dcd6e-1617">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1617">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="dcd6e-1618">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1618">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="dcd6e-1619">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1619">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="dcd6e-1620">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1620">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="dcd6e-1621">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1621">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="dcd6e-1622">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1622">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="dcd6e-1623">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1623">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="dcd6e-1624">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1624">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="dcd6e-1625">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1625">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="dcd6e-1626">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1626">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="dcd6e-1627">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1627">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="dcd6e-1628">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1628">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="dcd6e-1629">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1629">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="dcd6e-1630">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1630">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="dcd6e-1631">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1631">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="dcd6e-1632">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1632">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="dcd6e-1633">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1633">This operation is no longer supported.</span></span>
* <span data-ttu-id="dcd6e-1634">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1634">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="dcd6e-1635">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1635">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="dcd6e-1636">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1636">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="dcd6e-1637">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1637">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="dcd6e-1638">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku** , mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1638">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="dcd6e-1639">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1639">New non-verified images are also now returned.</span></span> <span data-ttu-id="dcd6e-1640">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1640">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="dcd6e-1641">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1641">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="dcd6e-1642">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1642">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="dcd6e-1643">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1643">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="dcd6e-1644">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1644">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="dcd6e-1645">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1645">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="dcd6e-1646">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1646">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="dcd6e-1647">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1647">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="dcd6e-1648">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1648">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="dcd6e-1649">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1649">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-1650">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1650">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-1651">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1651">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="dcd6e-1652">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1652">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1653">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1654">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1654">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="dcd6e-1655">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1655">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="dcd6e-1656">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1656">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="dcd6e-1657">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1657">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dcd6e-1658">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1658">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="dcd6e-1659">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1659">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="dcd6e-1660">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1660">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="dcd6e-1661">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1661">Breaking changes</span></span>
    - <span data-ttu-id="dcd6e-1662">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1662">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="dcd6e-1663">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1663">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1664">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1664">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1665">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1665">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-1667">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1667">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="dcd6e-1668">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1668">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="dcd6e-1669">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1669">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="dcd6e-1670">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1670">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="dcd6e-1671">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1671">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="dcd6e-1672">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1672">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-1673">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1673">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-1674">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1674">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-1675">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1675">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-1676">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1676">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="dcd6e-1677">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1677">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="dcd6e-1678">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1678">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="dcd6e-1679">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1679">Removed five cmdlets:</span></span>
    - <span data-ttu-id="dcd6e-1680">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1680">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dcd6e-1681">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1681">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dcd6e-1682">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1682">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="dcd6e-1683">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1683">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="dcd6e-1684">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1684">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="dcd6e-1685">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1685">Added three cmdlets:</span></span>
    - <span data-ttu-id="dcd6e-1686">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1686">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="dcd6e-1687">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1687">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="dcd6e-1688">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1688">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="dcd6e-1689">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1689">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="dcd6e-1690">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1690">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="dcd6e-1691">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1691">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="dcd6e-1692">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1692">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="dcd6e-1693">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1693">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="dcd6e-1694">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1694">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="dcd6e-1695">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1695">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="dcd6e-1696">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1696">Added some scenario test cases.</span></span>
* <span data-ttu-id="dcd6e-1697">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1697">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-1698">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1698">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-1699">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1699">Breaking changes:</span></span>
    - <span data-ttu-id="dcd6e-1700">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1700">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dcd6e-1701">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1701">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dcd6e-1702">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1702">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dcd6e-1703">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1703">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dcd6e-1704">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="dcd6e-1705">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1705">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="dcd6e-1706">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1706">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="dcd6e-1707">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1707">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="dcd6e-1708">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1708">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dcd6e-1709">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1709">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="dcd6e-1710">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1710">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="dcd6e-1711">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1711">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-1712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1712">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-1713">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1713">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="dcd6e-1714">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1714">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="dcd6e-1715">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1715">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="dcd6e-1716">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1716">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="dcd6e-1717">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1717">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="dcd6e-1718">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1718">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="dcd6e-1719">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1719">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="dcd6e-1720">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1720">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="dcd6e-1721">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1721">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1722">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1723">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1723">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1724">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1724">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1725">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1725">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="dcd6e-1726">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1726">Updated cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-1727">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1727">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-1728">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1728">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-1729">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1729">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-1730">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1730">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-1731">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1731">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="dcd6e-1732">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1732">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="dcd6e-1733">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1733">New cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-1734">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1734">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="dcd6e-1735">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1735">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="dcd6e-1736">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1736">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="dcd6e-1737">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1737">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="dcd6e-1738">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1738">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="dcd6e-1739">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1739">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="dcd6e-1740">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1740">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="dcd6e-1741">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1741">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="dcd6e-1742">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1742">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-1743">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1743">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="dcd6e-1744">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1744">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dcd6e-1745">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1745">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dcd6e-1746">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1746">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="dcd6e-1747">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1747">Set-AzVirtualHub</span></span>
* <span data-ttu-id="dcd6e-1748">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1748">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="dcd6e-1749">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1749">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dcd6e-1750">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1750">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="dcd6e-1751">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1751">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="dcd6e-1752">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1752">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="dcd6e-1753">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1753">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="dcd6e-1754">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1754">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="dcd6e-1755">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1755">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-1756">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1756">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="dcd6e-1757">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1757">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dcd6e-1758">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1758">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dcd6e-1759">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1759">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dcd6e-1760">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1760">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dcd6e-1761">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1761">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="dcd6e-1762">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1762">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="dcd6e-1763">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1763">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="dcd6e-1764">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1764">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-1765">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1765">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="dcd6e-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="dcd6e-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="dcd6e-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="dcd6e-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="dcd6e-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="dcd6e-1771">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dcd6e-1772">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1772">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="dcd6e-1773">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1773">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="dcd6e-1774">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1774">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="dcd6e-1775">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1775">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="dcd6e-1776">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1776">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="dcd6e-1777">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1777">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="dcd6e-1778">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1778">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="dcd6e-1779">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1779">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="dcd6e-1780">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1780">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="dcd6e-1781">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1781">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="dcd6e-1782">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1782">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-1783">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1783">New-AzIpGroup</span></span>
        - <span data-ttu-id="dcd6e-1784">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1784">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="dcd6e-1785">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1785">Get-AzIpGroup</span></span>
        - <span data-ttu-id="dcd6e-1786">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1786">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-1787">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1787">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-1788">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1788">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1789">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1789">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1790">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1790">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="dcd6e-1791">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1791">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="dcd6e-1792">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1792">Removed deprecated aliases:</span></span>
* <span data-ttu-id="dcd6e-1793">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1793">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="dcd6e-1794">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1794">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="dcd6e-1795">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1795">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="dcd6e-1796">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1796">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="dcd6e-1797">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1797">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="dcd6e-1798">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1798">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1799">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1799">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1800">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1800">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="dcd6e-1801">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1801">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="dcd6e-1802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1802">Set-AzStorageAccount</span></span>
* <span data-ttu-id="dcd6e-1803">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1803">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="dcd6e-1804">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1804">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="dcd6e-1805">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1805">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="dcd6e-1806">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1806">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="dcd6e-1807">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1807">General</span></span>
* <span data-ttu-id="dcd6e-1808">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1808">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1809">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1809">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1810">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1810">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-1811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1811">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-1812">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1812">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="dcd6e-1813">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1813">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1814">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-1815">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1815">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dcd6e-1816">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1816">Az.Batch</span></span>
* <span data-ttu-id="dcd6e-1817">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1817">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1818">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1818">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1819">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1819">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="dcd6e-1820">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1820">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="dcd6e-1821">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1821">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="dcd6e-1822">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1822">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1823">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1823">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1824">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1824">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="dcd6e-1825">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1825">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="dcd6e-1826">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1826">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-1828">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1828">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="dcd6e-1829">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1829">Az.HealthcareApis</span></span>
* <span data-ttu-id="dcd6e-1830">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1830">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="dcd6e-1831">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1831">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="dcd6e-1832">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1832">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="dcd6e-1833">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1833">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-1834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1834">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-1835">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1835">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="dcd6e-1836">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1836">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-1837">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1837">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-1838">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1838">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="dcd6e-1839">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1839">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="dcd6e-1840">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1840">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="dcd6e-1841">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1841">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1842">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1842">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1843">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1843">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="dcd6e-1844">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1844">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="dcd6e-1845">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-1846">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1846">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="dcd6e-1847">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1847">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dcd6e-1848">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1848">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="dcd6e-1849">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1849">Updated cmdlets:</span></span>
        - <span data-ttu-id="dcd6e-1850">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1850">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dcd6e-1851">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1851">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dcd6e-1852">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1852">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="dcd6e-1853">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1853">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="dcd6e-1854">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1854">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="dcd6e-1855">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1855">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="dcd6e-1856">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1856">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dcd6e-1857">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1857">Az.RedisCache</span></span>
* <span data-ttu-id="dcd6e-1858">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1858">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1859">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1859">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1860">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1860">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1861">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1862">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1862">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="dcd6e-1863">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1863">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="dcd6e-1864">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1864">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="dcd6e-1865">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1865">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="dcd6e-1866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1866">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dcd6e-1867">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1867">Az.StorageSync</span></span>
* <span data-ttu-id="dcd6e-1868">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1868">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-1869">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1869">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-1870">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1870">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="dcd6e-1871">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1871">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-1872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1872">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-1873">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1873">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="dcd6e-1874">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1874">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="dcd6e-1875">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1875">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-1876">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1876">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-1877">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1877">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="dcd6e-1878">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1878">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="dcd6e-1879">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1879">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1880">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-1881">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1881">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="dcd6e-1882">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1882">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dcd6e-1883">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1883">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="dcd6e-1884">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1884">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="dcd6e-1885">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1885">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="dcd6e-1886">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1886">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="dcd6e-1887">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1887">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="dcd6e-1888">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1888">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="dcd6e-1889">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1889">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-1890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1890">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-1891">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1891">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="dcd6e-1892">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1892">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-1893">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1893">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-1894">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1894">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-1895">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1895">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-1896">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1896">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="dcd6e-1897">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1897">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="dcd6e-1898">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1898">New cmdlets are:</span></span>
    - <span data-ttu-id="dcd6e-1899">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1899">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dcd6e-1900">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1900">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dcd6e-1901">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1901">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="dcd6e-1902">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1902">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-1903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1903">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-1904">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1904">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="dcd6e-1905">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1905">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="dcd6e-1906">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1906">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="dcd6e-1907">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019** , antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1907">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="dcd6e-1908">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1908">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="dcd6e-1909">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1909">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="dcd6e-1910">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1910">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="dcd6e-1911">**OBSERVAÇÃO** : é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1911">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="dcd6e-1912">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource** ) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1912">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dcd6e-1913">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1913">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="dcd6e-1914">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource** ) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1914">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="dcd6e-1915">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1915">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="dcd6e-1916">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1916">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="dcd6e-1917">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1917">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="dcd6e-1918">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1918">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="dcd6e-1919">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1919">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="dcd6e-1920">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1920">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="dcd6e-1921">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1921">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="dcd6e-1922">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1922">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="dcd6e-1923">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1923">Overall improved help files</span></span>
* <span data-ttu-id="dcd6e-1924">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1924">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1925">Az.Network</span></span>
* <span data-ttu-id="dcd6e-1926">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1926">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="dcd6e-1927">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1927">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="dcd6e-1928">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1928">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="dcd6e-1929">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1929">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="dcd6e-1930">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1930">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="dcd6e-1931">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1931">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="dcd6e-1932">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1932">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="dcd6e-1933">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1933">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="dcd6e-1934">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1934">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="dcd6e-1935">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1935">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="dcd6e-1936">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1936">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="dcd6e-1937">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1937">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="dcd6e-1938">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1938">New cmdlets</span></span>
        - <span data-ttu-id="dcd6e-1939">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1939">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="dcd6e-1940">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1940">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="dcd6e-1941">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1941">Updated cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-1942">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1942">New-VpnSite</span></span>
        - <span data-ttu-id="dcd6e-1943">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1943">Update-VpnSite</span></span>
        - <span data-ttu-id="dcd6e-1944">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1944">New-VpnConnection</span></span>
        - <span data-ttu-id="dcd6e-1945">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1945">Update-VpnConnection</span></span>
* <span data-ttu-id="dcd6e-1946">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1946">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-1947">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1947">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-1948">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1948">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="dcd6e-1949">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1949">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-1950">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1950">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-1951">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1951">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-1952">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1952">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-1953">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1953">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="dcd6e-1954">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1954">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="dcd6e-1955">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1955">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dcd6e-1956">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1956">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dcd6e-1957">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1957">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dcd6e-1958">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1958">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="dcd6e-1959">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1959">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dcd6e-1960">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1960">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dcd6e-1961">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1961">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dcd6e-1962">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1962">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dcd6e-1963">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1963">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="dcd6e-1964">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1964">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="dcd6e-1965">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1965">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="dcd6e-1966">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1966">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="dcd6e-1967">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1967">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="dcd6e-1968">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1968">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dcd6e-1969">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1969">Az.SignalR</span></span>
* <span data-ttu-id="dcd6e-1970">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1970">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-1971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1971">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-1972">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1972">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="dcd6e-1973">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1973">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="dcd6e-1974">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1974">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="dcd6e-1975">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1975">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="dcd6e-1976">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1976">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1977">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-1978">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1978">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="dcd6e-1979">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1979">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="dcd6e-1980">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1980">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="dcd6e-1981">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1981">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="dcd6e-1982">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1982">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="dcd6e-1983">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1983">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="dcd6e-1984">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1984">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="dcd6e-1985">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1985">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dcd6e-1986">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1986">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dcd6e-1987">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1987">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="dcd6e-1988">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1988">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1989">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-1990">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1990">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="dcd6e-1991">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1991">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="dcd6e-1992">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1992">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="dcd6e-1993">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1993">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="dcd6e-1994">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1994">General</span></span>
* <span data-ttu-id="dcd6e-1995">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1995">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-1996">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1996">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-1997">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1997">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-1998">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1998">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-1999">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-1999">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="dcd6e-2000">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2000">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-2001">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2001">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-2002">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2002">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="dcd6e-2003">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2003">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="dcd6e-2004">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2004">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="dcd6e-2005">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2005">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="dcd6e-2006">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2006">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dcd6e-2007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2007">Az.Batch</span></span>
* <span data-ttu-id="dcd6e-2008">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2008">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2009">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-2010">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2010">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2011">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2012">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2012">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="dcd6e-2013">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2013">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="dcd6e-2014">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2014">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="dcd6e-2015">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2015">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="dcd6e-2016">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2016">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="dcd6e-2017">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2017">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="dcd6e-2018">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2018">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="dcd6e-2019">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2019">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-2020">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2020">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-2021">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2021">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="dcd6e-2022">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2022">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="dcd6e-2023">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2023">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="dcd6e-2024">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2024">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-2025">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2025">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-2026">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2026">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-2027">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2027">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-2028">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2028">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="dcd6e-2029">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2029">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="dcd6e-2030">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2030">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="dcd6e-2031">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2031">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="dcd6e-2032">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2032">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dcd6e-2033">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2033">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2034">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-2035">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2035">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2036">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2036">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2037">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2037">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="dcd6e-2038">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2038">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="dcd6e-2039">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2039">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="dcd6e-2040">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2040">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="dcd6e-2041">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2041">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="dcd6e-2042">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2042">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="dcd6e-2043">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2043">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-2045">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2045">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="dcd6e-2046">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2046">Added example</span></span>
    - <span data-ttu-id="dcd6e-2047">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2047">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="dcd6e-2048">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2048">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="dcd6e-2049">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2049">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2050">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2050">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2051">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2051">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2052">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2052">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2053">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2053">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="dcd6e-2054">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2054">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="dcd6e-2055">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2055">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="dcd6e-2056">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2056">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dcd6e-2057">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2057">Az.ServiceBus</span></span>
* <span data-ttu-id="dcd6e-2058">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2058">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="dcd6e-2059">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2059">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="dcd6e-2060">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2060">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-2061">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2061">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-2062">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2062">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="dcd6e-2063">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2063">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="dcd6e-2064">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2064">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="dcd6e-2065">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2065">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="dcd6e-2066">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2066">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="dcd6e-2067">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2067">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2068">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2069">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2069">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2070">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2070">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2071">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2071">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="dcd6e-2072">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2072">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="dcd6e-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2073">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="dcd6e-2074">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2074">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="dcd6e-2075">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2075">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="dcd6e-2076">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2076">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2077">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2077">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2078">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2078">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="dcd6e-2079">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2079">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2080">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2081">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2081">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="dcd6e-2082">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2082">Az.ApplicationInsights</span></span>
* <span data-ttu-id="dcd6e-2083">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2083">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2084">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2084">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2085">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2085">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-2087">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2087">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2088">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2089">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2089">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dcd6e-2090">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2090">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dcd6e-2091">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2091">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="dcd6e-2092">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2092">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-2093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2093">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-2094">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2094">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="dcd6e-2095">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2095">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-2096">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2096">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-2097">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2097">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dcd6e-2098">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2098">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-2099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2099">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-2100">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2100">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dcd6e-2101">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2101">Az.LogicApp</span></span>
* <span data-ttu-id="dcd6e-2102">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2102">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="dcd6e-2103">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2103">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="dcd6e-2104">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2104">Az.ManagedServices</span></span>
* <span data-ttu-id="dcd6e-2105">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2105">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2106">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2107">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2107">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="dcd6e-2108">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2108">New cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2109">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2109">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dcd6e-2110">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2110">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dcd6e-2111">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2111">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-2112">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2112">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-2113">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2113">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-2114">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2114">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="dcd6e-2115">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2115">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="dcd6e-2116">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2116">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="dcd6e-2117">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2117">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="dcd6e-2118">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2118">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="dcd6e-2119">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2119">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="dcd6e-2120">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2120">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="dcd6e-2121">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2121">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="dcd6e-2122">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2122">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="dcd6e-2123">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2123">Updated cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2124">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2124">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dcd6e-2125">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2125">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="dcd6e-2126">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2126">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="dcd6e-2127">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2127">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="dcd6e-2128">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2128">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="dcd6e-2129">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-2130">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2130">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dcd6e-2131">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2131">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="dcd6e-2132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2132">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="dcd6e-2133">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2133">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="dcd6e-2134">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2134">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="dcd6e-2135">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2135">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-2136">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2136">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-2137">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2137">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="dcd6e-2138">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2138">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2139">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2139">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2140">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2140">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dcd6e-2141">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2141">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="dcd6e-2142">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2142">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="dcd6e-2143">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2143">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="dcd6e-2144">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2144">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="dcd6e-2145">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2145">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dcd6e-2146">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2146">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="dcd6e-2147">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2147">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="dcd6e-2148">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2148">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="dcd6e-2149">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2149">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2150">Az.Resources</span></span>
- <span data-ttu-id="dcd6e-2151">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2151">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="dcd6e-2152">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2152">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dcd6e-2153">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2153">Az.ServiceBus</span></span>
* <span data-ttu-id="dcd6e-2154">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2154">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="dcd6e-2155">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2155">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2156">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2157">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2157">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="dcd6e-2158">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2158">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="dcd6e-2159">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2159">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2160">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2161">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2161">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dcd6e-2162">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2162">Az.StorageSync</span></span>
* <span data-ttu-id="dcd6e-2163">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2163">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="dcd6e-2164">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2164">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2165">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2165">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2166">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2166">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="dcd6e-2167">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2167">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="dcd6e-2168">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2168">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="dcd6e-2169">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2169">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2170">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2171">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2171">Add support for profile cmdlets</span></span>
* <span data-ttu-id="dcd6e-2172">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2172">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="dcd6e-2173">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2173">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="dcd6e-2174">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2174">Az.Advisor</span></span>
* <span data-ttu-id="dcd6e-2175">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2175">GA release of Az.Advisor</span></span>
* <span data-ttu-id="dcd6e-2176">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2176">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-2177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2177">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-2178">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2178">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="dcd6e-2179">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2179">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="dcd6e-2180">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2180">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="dcd6e-2181">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2181">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="dcd6e-2182">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2182">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="dcd6e-2183">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2183">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="dcd6e-2184">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2184">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2185">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2186">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2186">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2187">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2187">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2188">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2188">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-2189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2189">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-2190">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2190">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dcd6e-2191">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2191">Az.EventGrid</span></span>
* <span data-ttu-id="dcd6e-2192">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2192">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-2193">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2193">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-2194">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2194">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2195">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2195">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2196">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2196">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="dcd6e-2197">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2197">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-2198">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2198">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-2199">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2199">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="dcd6e-2200">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2200">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-2201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2201">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-2202">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2202">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2203">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2204">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2204">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2205">Az.Resources</span></span>
    - <span data-ttu-id="dcd6e-2206">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2206">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="dcd6e-2207">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2207">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="dcd6e-2208">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2208">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="dcd6e-2209">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2209">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dcd6e-2210">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2210">Az.ServiceBus</span></span>
* <span data-ttu-id="dcd6e-2211">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2211">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2212">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2213">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2213">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="dcd6e-2214">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2214">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="dcd6e-2215">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2215">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dcd6e-2216">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2216">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dcd6e-2217">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2217">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="dcd6e-2218">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2218">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dcd6e-2219">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2219">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="dcd6e-2220">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2220">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="dcd6e-2221">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2221">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2222">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2223">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2223">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="dcd6e-2224">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2224">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="dcd6e-2225">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2225">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="dcd6e-2226">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2226">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="dcd6e-2227">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2227">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="dcd6e-2228">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2228">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="dcd6e-2229">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2229">Set-AzStorageAccount</span></span>
* <span data-ttu-id="dcd6e-2230">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2230">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="dcd6e-2231">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2231">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="dcd6e-2232">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2232">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="dcd6e-2233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2233">Az.StorageSync</span></span>
* <span data-ttu-id="dcd6e-2234">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2234">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="dcd6e-2235">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2235">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2236">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2237">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2237">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="dcd6e-2238">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2238">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="dcd6e-2239">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2239">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="dcd6e-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="dcd6e-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2242">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2243">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2243">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="dcd6e-2244">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2244">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="dcd6e-2245">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2245">Az.Dns</span></span>
* <span data-ttu-id="dcd6e-2246">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2246">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dcd6e-2247">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2247">Az.EventGrid</span></span>
* <span data-ttu-id="dcd6e-2248">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2248">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="dcd6e-2249">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2249">New cmdlets:</span></span>
    - <span data-ttu-id="dcd6e-2250">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2250">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dcd6e-2251">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2251">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dcd6e-2252">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2252">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dcd6e-2253">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2253">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="dcd6e-2254">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2254">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="dcd6e-2255">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2255">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dcd6e-2256">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2256">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dcd6e-2257">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2257">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="dcd6e-2258">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2258">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="dcd6e-2259">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2259">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="dcd6e-2260">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2260">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dcd6e-2261">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2261">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="dcd6e-2262">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2262">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="dcd6e-2263">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2263">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="dcd6e-2264">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2264">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="dcd6e-2265">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2265">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="dcd6e-2266">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2266">Updated cmdlets:</span></span>
    - <span data-ttu-id="dcd6e-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="dcd6e-2268">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2268">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dcd6e-2269">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2269">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="dcd6e-2270">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2270">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="dcd6e-2271">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2271">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="dcd6e-2272">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2272">Event subscription expiration date,</span></span>
            - <span data-ttu-id="dcd6e-2273">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2273">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="dcd6e-2274">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2274">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="dcd6e-2275">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2275">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="dcd6e-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="dcd6e-2277">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2277">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="dcd6e-2278">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2278">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="dcd6e-2279">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2279">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="dcd6e-2280">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2280">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-2281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2281">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-2282">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2282">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="dcd6e-2283">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2283">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="dcd6e-2284">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2284">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="dcd6e-2285">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2285">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2286">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2287">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2287">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="dcd6e-2288">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2288">New cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="dcd6e-2290">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2290">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="dcd6e-2291">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2291">New cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2292">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2292">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="dcd6e-2293">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2293">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="dcd6e-2294">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2294">New cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2295">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2295">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dcd6e-2296">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2296">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dcd6e-2297">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2297">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="dcd6e-2298">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2298">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="dcd6e-2299">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2299">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="dcd6e-2300">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2300">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="dcd6e-2301">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2301">New cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2302">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2302">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dcd6e-2303">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2303">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dcd6e-2304">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2304">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="dcd6e-2305">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2305">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="dcd6e-2306">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2306">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="dcd6e-2307">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2307">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="dcd6e-2308">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2308">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="dcd6e-2309">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2309">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="dcd6e-2310">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2310">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="dcd6e-2311">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2311">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="dcd6e-2312">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2312">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="dcd6e-2313">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2313">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="dcd6e-2314">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2314">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="dcd6e-2315">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2315">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="dcd6e-2316">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2316">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="dcd6e-2317">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2317">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="dcd6e-2318">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2318">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="dcd6e-2319">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2319">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="dcd6e-2320">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2320">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-2321">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2321">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="dcd6e-2322">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2322">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="dcd6e-2323">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2323">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="dcd6e-2324">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2324">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="dcd6e-2325">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2325">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="dcd6e-2326">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2326">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dcd6e-2327">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2327">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="dcd6e-2328">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2328">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-2330">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2330">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2331">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2331">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2332">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2332">Support for additional Template Export options</span></span>
    - <span data-ttu-id="dcd6e-2333">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2333">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dcd6e-2334">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2334">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="dcd6e-2335">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2335">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-2336">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2336">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-2337">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2337">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2338">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2339">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2339">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="dcd6e-2340">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2340">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="dcd6e-2341">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2341">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="dcd6e-2342">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2342">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dcd6e-2343">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2343">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dcd6e-2344">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2344">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="dcd6e-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="dcd6e-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2347">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2347">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2348">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2348">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="dcd6e-2349">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2349">New-AzStorageAccount</span></span>
* <span data-ttu-id="dcd6e-2350">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2350">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="dcd6e-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2352">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2352">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2353">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2353">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="dcd6e-2354">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2354">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="dcd6e-2355">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2355">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="dcd6e-2356">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2356">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-2357">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2357">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2358">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2359">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2359">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="dcd6e-2360">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2360">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-2361">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2361">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-2362">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2362">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="dcd6e-2363">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2363">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2364">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2365">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2365">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="dcd6e-2366">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2366">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-2367">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2367">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-2368">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2368">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2370">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2370">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dcd6e-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="dcd6e-2372">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2372">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-2373">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2373">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-2374">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2374">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="dcd6e-2375">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2375">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2376">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2377">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2377">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="dcd6e-2378">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2378">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="dcd6e-2379">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2379">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="dcd6e-2380">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2380">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2381">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2381">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2382">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2382">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="dcd6e-2383">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2383">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-2384">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2384">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-2385">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2385">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="dcd6e-2386">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2386">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="dcd6e-2387">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2387">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="dcd6e-2388">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2388">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="dcd6e-2389">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2389">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="dcd6e-2390">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2390">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="dcd6e-2391">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2391">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="dcd6e-2392">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2392">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="dcd6e-2393">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2393">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="dcd6e-2394">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2394">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="dcd6e-2395">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2395">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="dcd6e-2396">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2396">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="dcd6e-2397">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2397">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="dcd6e-2398">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2398">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="dcd6e-2399">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2399">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="dcd6e-2400">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2400">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="dcd6e-2401">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2401">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="dcd6e-2402">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2402">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="dcd6e-2403">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2403">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="dcd6e-2404">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2404">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="dcd6e-2405">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2405">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="dcd6e-2406">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2406">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="dcd6e-2407">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2407">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="dcd6e-2408">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2408">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="dcd6e-2409">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2409">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="dcd6e-2410">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2410">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="dcd6e-2411">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2411">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="dcd6e-2412">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2412">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="dcd6e-2413">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2413">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="dcd6e-2414">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2414">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="dcd6e-2415">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2415">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="dcd6e-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="dcd6e-2417">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2417">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="dcd6e-2418">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2418">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dcd6e-2419">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2419">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="dcd6e-2420">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2420">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="dcd6e-2421">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2421">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="dcd6e-2422">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2422">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="dcd6e-2423">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2423">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="dcd6e-2424">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2424">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dcd6e-2425">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2425">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dcd6e-2426">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2426">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="dcd6e-2427">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2427">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="dcd6e-2428">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2428">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="dcd6e-2429">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2429">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="dcd6e-2430">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2430">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="dcd6e-2431">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2431">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="dcd6e-2432">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2432">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="dcd6e-2433">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2433">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="dcd6e-2434">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2434">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="dcd6e-2435">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2435">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="dcd6e-2436">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2436">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="dcd6e-2437">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2437">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="dcd6e-2438">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2438">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="dcd6e-2439">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2439">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="dcd6e-2440">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2440">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="dcd6e-2441">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2441">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dcd6e-2442">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2442">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dcd6e-2443">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2443">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dcd6e-2444">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2444">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dcd6e-2445">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2445">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="dcd6e-2446">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2446">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="dcd6e-2447">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2447">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="dcd6e-2448">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2448">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="dcd6e-2449">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2449">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="dcd6e-2450">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2450">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="dcd6e-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="dcd6e-2452">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2452">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="dcd6e-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="dcd6e-2454">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2454">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="dcd6e-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="dcd6e-2456">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2456">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="dcd6e-2457">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2457">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="dcd6e-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="dcd6e-2459">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2459">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="dcd6e-2460">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2460">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="dcd6e-2461">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2461">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2462">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2462">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2463">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2463">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="dcd6e-2464">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="dcd6e-2465">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2465">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="dcd6e-2466">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2466">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="dcd6e-2467">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2467">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="dcd6e-2468">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2468">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="dcd6e-2469">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2469">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2470">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2470">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2471">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2471">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="dcd6e-2472">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2472">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-2473">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2473">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-2474">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2474">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-2475">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2475">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-2476">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2476">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2477">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2478">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2478">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="dcd6e-2479">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2479">Updated cmdlet:</span></span>
        - <span data-ttu-id="dcd6e-2480">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2480">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="dcd6e-2481">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2481">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2482">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2483">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2483">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2484">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2485">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2485">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="dcd6e-2486">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2486">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2487">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2488">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2488">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-2490">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2490">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="dcd6e-2491">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2491">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2492">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2493">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2493">Proximity placement group feature.</span></span>
    - <span data-ttu-id="dcd6e-2494">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2494">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="dcd6e-2495">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2495">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="dcd6e-2496">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2496">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="dcd6e-2497">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2497">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="dcd6e-2498">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2498">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="dcd6e-2499">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2499">Breaking changes</span></span>
    - <span data-ttu-id="dcd6e-2500">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2500">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="dcd6e-2501">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2501">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="dcd6e-2502">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2502">Az.DeploymentManager</span></span>
* <span data-ttu-id="dcd6e-2503">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2503">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="dcd6e-2504">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2504">Az.Dns</span></span>
* <span data-ttu-id="dcd6e-2505">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2505">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="dcd6e-2506">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2506">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="dcd6e-2507">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2507">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-2508">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2508">Az.FrontDoor</span></span>
* <span data-ttu-id="dcd6e-2509">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2509">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="dcd6e-2510">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2510">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-2511">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2511">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-2512">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2512">Removed two cmdlets:</span></span>
    - <span data-ttu-id="dcd6e-2513">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2513">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="dcd6e-2514">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2514">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dcd6e-2515">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2515">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="dcd6e-2516">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2516">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="dcd6e-2517">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2517">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="dcd6e-2518">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2518">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-2519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2519">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-2520">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2520">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="dcd6e-2521">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2521">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="dcd6e-2522">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2522">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="dcd6e-2523">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2523">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="dcd6e-2524">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2524">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="dcd6e-2525">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2525">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="dcd6e-2526">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2526">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="dcd6e-2527">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2527">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dcd6e-2528">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2528">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dcd6e-2529">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2529">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dcd6e-2530">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2530">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dcd6e-2531">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2531">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="dcd6e-2532">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2532">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="dcd6e-2533">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2533">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2534">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2535">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2535">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="dcd6e-2536">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2536">New cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2537">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2537">New-AzNatGateway</span></span>
        - <span data-ttu-id="dcd6e-2538">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2538">Get-AzNatGateway</span></span>
        - <span data-ttu-id="dcd6e-2539">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2539">Set-AzNatGateway</span></span>
        - <span data-ttu-id="dcd6e-2540">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2540">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="dcd6e-2541">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2541">Updated cmdlets</span></span>
        - <span data-ttu-id="dcd6e-2542">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2542">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="dcd6e-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="dcd6e-2544">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2544">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="dcd6e-2545">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2545">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="dcd6e-2546">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2546">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-2547">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2547">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-2548">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2548">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="dcd6e-2549">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2549">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="dcd6e-2550">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2550">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2551">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2552">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2552">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="dcd6e-2553">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2553">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="dcd6e-2554">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2554">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="dcd6e-2555">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2555">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="dcd6e-2556">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2556">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="dcd6e-2557">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2557">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="dcd6e-2558">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2558">Az.Relay</span></span>
* <span data-ttu-id="dcd6e-2559">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2559">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dcd6e-2560">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2560">Az.ServiceBus</span></span>
* <span data-ttu-id="dcd6e-2561">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2561">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2562">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2562">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2563">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2563">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="dcd6e-2564">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2564">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="dcd6e-2565">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2565">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="dcd6e-2566">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2566">New-AzStorageAccount</span></span>
* <span data-ttu-id="dcd6e-2567">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2567">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="dcd6e-2568">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2568">New-AzStorageAccount</span></span>
    - <span data-ttu-id="dcd6e-2569">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2569">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="dcd6e-2570">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2570">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2571">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2571">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2572">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2572">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="dcd6e-2573">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2573">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="dcd6e-2574">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2574">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dcd6e-2575">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2575">Highlights since the last major release</span></span>
* <span data-ttu-id="dcd6e-2576">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2576">General availability of `Az` module</span></span>
* <span data-ttu-id="dcd6e-2577">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2577">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dcd6e-2578">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2578">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dcd6e-2579">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2579">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dcd6e-2580">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2580">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dcd6e-2581">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2581">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2582">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2582">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2583">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2584">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2584">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="dcd6e-2585">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2585">Az.Batch</span></span>
* <span data-ttu-id="dcd6e-2586">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2586">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-2587">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2587">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-2588">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2588">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-2589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2589">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-2590">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2590">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2591">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2591">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2592">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2592">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="dcd6e-2593">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dcd6e-2594">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2594">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-2595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2595">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-2596">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2596">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-2597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2597">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-2598">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dcd6e-2599">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2599">Az.EventGrid</span></span>
* <span data-ttu-id="dcd6e-2600">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2600">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-2601">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2601">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-2602">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2602">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="dcd6e-2603">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2603">Az.HDInsight</span></span>
* <span data-ttu-id="dcd6e-2604">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2604">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-2605">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2605">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-2606">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2606">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-2607">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2607">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-2608">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dcd6e-2609">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2609">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="dcd6e-2610">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2610">Az.MachineLearning</span></span>
* <span data-ttu-id="dcd6e-2611">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="dcd6e-2612">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2612">Az.Media</span></span>
* <span data-ttu-id="dcd6e-2613">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2613">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-2614">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2614">Az.Monitor</span></span>
  * <span data-ttu-id="dcd6e-2615">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2615">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="dcd6e-2616">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2616">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="dcd6e-2617">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2617">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="dcd6e-2618">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2618">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dcd6e-2619">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2619">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="dcd6e-2620">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2620">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="dcd6e-2621">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2621">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2622">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2623">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2623">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dcd6e-2624">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2624">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="dcd6e-2625">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2625">Az.NotificationHubs</span></span>
* <span data-ttu-id="dcd6e-2626">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-2627">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2627">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-2628">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="dcd6e-2629">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2629">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="dcd6e-2630">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2631">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2632">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dcd6e-2633">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2633">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="dcd6e-2634">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2634">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="dcd6e-2635">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2635">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dcd6e-2636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2636">Az.RedisCache</span></span>
* <span data-ttu-id="dcd6e-2637">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2638">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2638">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2639">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2639">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2640">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2641">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2641">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="dcd6e-2642">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dcd6e-2643">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2643">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="dcd6e-2644">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2644">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="dcd6e-2645">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2645">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="dcd6e-2646">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2646">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="dcd6e-2647">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2647">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2648">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2649">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2649">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="dcd6e-2650">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="dcd6e-2651">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2651">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="dcd6e-2652">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2652">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="dcd6e-2653">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2653">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dcd6e-2654">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2654">Highlights since the last major release</span></span>
* <span data-ttu-id="dcd6e-2655">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2655">General availability of `Az` module</span></span>
* <span data-ttu-id="dcd6e-2656">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2656">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dcd6e-2657">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2657">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dcd6e-2658">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2658">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dcd6e-2659">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2659">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dcd6e-2660">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2660">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2661">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2661">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2662">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2662">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2663">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2663">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dcd6e-2664">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2664">Az.AnalysisServices</span></span>
* <span data-ttu-id="dcd6e-2665">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2665">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="dcd6e-2666">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2666">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2667">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2667">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2668">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2668">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="dcd6e-2669">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2669">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="dcd6e-2670">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2670">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2671">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2672">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2672">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="dcd6e-2673">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2673">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="dcd6e-2674">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2674">Az.ContainerInstance</span></span>
* <span data-ttu-id="dcd6e-2675">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2675">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-2676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2676">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-2677">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2677">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="dcd6e-2678">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2678">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2679">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2680">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2680">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="dcd6e-2681">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2681">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="dcd6e-2682">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2682">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="dcd6e-2683">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2683">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="dcd6e-2684">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2684">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="dcd6e-2685">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2685">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2686">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2686">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2687">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2687">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2688">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2688">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2689">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2689">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="dcd6e-2690">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2690">New-AzStorageContext</span></span>
* <span data-ttu-id="dcd6e-2691">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2691">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="dcd6e-2692">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2692">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dcd6e-2693">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2693">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="dcd6e-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="dcd6e-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="dcd6e-2696">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2696">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="dcd6e-2697">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2697">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dcd6e-2698">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2698">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="dcd6e-2699">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2699">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="dcd6e-2700">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2700">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="dcd6e-2701">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2701">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="dcd6e-2702">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2702">Highlights since the last major release</span></span>
* <span data-ttu-id="dcd6e-2703">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2703">General availability of `Az` module</span></span>
* <span data-ttu-id="dcd6e-2704">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2704">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="dcd6e-2705">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2705">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="dcd6e-2706">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2706">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="dcd6e-2707">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2707">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dcd6e-2708">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2708">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2709">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2709">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2710">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2710">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2711">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2711">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="dcd6e-2712">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2712">Dynamic grouping</span></span>
    * <span data-ttu-id="dcd6e-2713">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2713">Pre-Post script</span></span>
    * <span data-ttu-id="dcd6e-2714">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2714">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2715">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2716">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2716">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="dcd6e-2717">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2717">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-2718">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2718">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-2719">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2719">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2720">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2721">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2721">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="dcd6e-2722">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2722">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2723">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2724">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2724">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="dcd6e-2725">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2725">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2726">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2726">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2727">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2727">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="dcd6e-2728">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2728">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2729">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2730">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2730">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2731">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2732">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2732">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="dcd6e-2733">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2733">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dcd6e-2734">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2734">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dcd6e-2735">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2735">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="dcd6e-2736">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2736">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="dcd6e-2737">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2737">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="dcd6e-2738">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2738">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2739">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2740">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2740">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="dcd6e-2741">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2741">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2742">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2743">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2743">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="dcd6e-2744">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2744">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2745">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2746">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2746">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="dcd6e-2747">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2747">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="dcd6e-2748">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2748">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-2749">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2749">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-2750">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2750">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2751">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2751">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2752">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2752">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-2753">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2753">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-2754">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2754">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dcd6e-2755">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2755">Az.LogicApp</span></span>
* <span data-ttu-id="dcd6e-2756">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2756">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2757">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2757">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2758">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2758">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2759">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2759">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2760">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2760">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="dcd6e-2761">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2761">SDK Update</span></span>
* <span data-ttu-id="dcd6e-2762">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2762">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="dcd6e-2763">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2763">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2764">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2765">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2765">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="dcd6e-2766">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2766">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="dcd6e-2767">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2767">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="dcd6e-2768">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2768">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="dcd6e-2769">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2769">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="dcd6e-2770">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2770">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2771">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2771">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2772">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2772">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="dcd6e-2773">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2773">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2774">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2775">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2775">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="dcd6e-2776">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2776">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="dcd6e-2777">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2777">Az.AnalysisServices</span></span>
* <span data-ttu-id="dcd6e-2778">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2778">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2779">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2779">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2780">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2780">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="dcd6e-2781">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2781">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="dcd6e-2782">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2782">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-2783">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2783">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-2784">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2784">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2785">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2785">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2786">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2786">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="dcd6e-2787">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2787">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="dcd6e-2788">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2788">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="dcd6e-2789">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2789">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-2790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2790">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-2791">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2791">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="dcd6e-2792">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2792">Az.EventHub</span></span>
* <span data-ttu-id="dcd6e-2793">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2793">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-2794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2794">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-2795">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2795">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dcd6e-2796">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2796">Az.LogicApp</span></span>
* <span data-ttu-id="dcd6e-2797">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2797">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="dcd6e-2798">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2798">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="dcd6e-2799">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2799">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="dcd6e-2800">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2800">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dcd6e-2801">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2801">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dcd6e-2802">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2802">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="dcd6e-2803">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2803">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="dcd6e-2804">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2804">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="dcd6e-2805">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2805">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dcd6e-2806">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2806">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dcd6e-2807">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2807">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="dcd6e-2808">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2808">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="dcd6e-2809">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2809">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="dcd6e-2810">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2810">Az.Monitor</span></span>
* <span data-ttu-id="dcd6e-2811">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2811">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2812">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2812">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2813">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2813">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-2814">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2814">Az.OperationalInsights</span></span>
* <span data-ttu-id="dcd6e-2815">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2815">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="dcd6e-2816">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2816">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="dcd6e-2817">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2817">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2818">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2819">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dcd6e-2820">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="dcd6e-2821">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2821">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="dcd6e-2822">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2822">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2823">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2823">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2824">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2824">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="dcd6e-2825">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2825">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2826">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2826">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2827">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2827">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="dcd6e-2828">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2828">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2829">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2829">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2830">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2830">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dcd6e-2831">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2831">Az.AnalysisServices</span></span>
<span data-ttu-id="dcd6e-2832">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2832">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2833">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2834">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2834">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="dcd6e-2835">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2835">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="dcd6e-2836">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2836">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2837">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2837">Az.RecoveryServices</span></span>
<span data-ttu-id="dcd6e-2838">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2838">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2839">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2840">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2840">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="dcd6e-2841">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2841">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="dcd6e-2842">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2842">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="dcd6e-2843">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2843">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2844">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2845">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2845">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="dcd6e-2846">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2846">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="dcd6e-2847">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2847">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="dcd6e-2848">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2848">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2849">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2850">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2850">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="dcd6e-2851">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2851">Az.AnalysisServices</span></span>
* <span data-ttu-id="dcd6e-2852">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2852">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-2853">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2853">Az.RecoveryServices</span></span>
* <span data-ttu-id="dcd6e-2854">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2854">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="dcd6e-2855">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2855">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2856">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2857">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2857">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="dcd6e-2858">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2858">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dcd6e-2859">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2859">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="dcd6e-2860">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2860">Az.Aks</span></span>
* <span data-ttu-id="dcd6e-2861">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2861">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="dcd6e-2862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2862">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-2863">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2863">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="dcd6e-2864">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2864">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="dcd6e-2865">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2865">Az.Cdn</span></span>
* <span data-ttu-id="dcd6e-2866">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2866">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2867">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2868">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2868">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="dcd6e-2869">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2869">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="dcd6e-2870">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2870">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="dcd6e-2871">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2871">Az.ContainerRegistry</span></span>
* <span data-ttu-id="dcd6e-2872">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2872">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="dcd6e-2873">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2873">Az.DataFactory</span></span>
* <span data-ttu-id="dcd6e-2874">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2874">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-2875">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2875">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-2876">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2876">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="dcd6e-2877">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2877">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="dcd6e-2878">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2878">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-2879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2879">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-2880">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2880">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-2881">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2881">Az.KeyVault</span></span>
* <span data-ttu-id="dcd6e-2882">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2882">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2883">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2883">Az.Network</span></span>
* <span data-ttu-id="dcd6e-2884">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2884">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2885">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2886">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2886">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="dcd6e-2887">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2887">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="dcd6e-2888">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2888">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="dcd6e-2889">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="dcd6e-2890">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2890">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="dcd6e-2891">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2891">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="dcd6e-2892">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2892">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-2893">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2893">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-2894">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2894">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="dcd6e-2895">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2895">Fix some error messages.</span></span>
* <span data-ttu-id="dcd6e-2896">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2896">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="dcd6e-2897">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2897">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dcd6e-2898">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2898">Az.SignalR</span></span>
* <span data-ttu-id="dcd6e-2899">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2899">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2900">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2901">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2901">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dcd6e-2902">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2902">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="dcd6e-2903">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2903">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="dcd6e-2904">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2904">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2905">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2906">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2906">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dcd6e-2907">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2907">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="dcd6e-2908">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2908">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="dcd6e-2909">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2909">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="dcd6e-2910">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2910">Az.TrafficManager</span></span>
* <span data-ttu-id="dcd6e-2911">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2911">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2912">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2912">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2913">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2913">Update incorrect online help URLs</span></span>
* <span data-ttu-id="dcd6e-2914">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2914">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="dcd6e-2915">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2915">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="dcd6e-2916">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2916">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2917">Az.Accounts</span></span>
* <span data-ttu-id="dcd6e-2918">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2918">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2919">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-2920">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2920">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="dcd6e-2921">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2921">Updated the description of ID in help files</span></span>
* <span data-ttu-id="dcd6e-2922">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2922">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-2924">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2924">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="dcd6e-2925">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2925">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="dcd6e-2926">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2926">Az.EventGrid</span></span>
* <span data-ttu-id="dcd6e-2927">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2927">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="dcd6e-2928">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2928">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="dcd6e-2929">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2929">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dcd6e-2930">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2930">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dcd6e-2931">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2931">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dcd6e-2932">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2932">Dead letter endpoint.</span></span>
    - <span data-ttu-id="dcd6e-2933">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2933">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="dcd6e-2934">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2934">Event Time-To-Live,</span></span>
        - <span data-ttu-id="dcd6e-2935">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2935">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="dcd6e-2936">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2936">Dead letter endpoint.</span></span>
* <span data-ttu-id="dcd6e-2937">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2937">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="dcd6e-2938">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2938">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="dcd6e-2939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2939">Az.IotHub</span></span>
* <span data-ttu-id="dcd6e-2940">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2940">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="dcd6e-2941">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2941">Az.LogicApp</span></span>
* <span data-ttu-id="dcd6e-2942">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2942">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-2943">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2943">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-2944">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2944">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="dcd6e-2945">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2945">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="dcd6e-2946">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2946">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dcd6e-2947">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2947">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="dcd6e-2948">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2948">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="dcd6e-2949">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2949">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="dcd6e-2950">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2950">Az.SignalR</span></span>
* <span data-ttu-id="dcd6e-2951">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2951">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2952">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-2953">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2953">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="dcd6e-2954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2954">Az.Storage</span></span>
* <span data-ttu-id="dcd6e-2955">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2955">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="dcd6e-2956">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2956">New-AzStorageContext</span></span>
* <span data-ttu-id="dcd6e-2957">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2957">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="dcd6e-2958">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2958">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-2959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2959">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-2960">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2960">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="dcd6e-2961">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2961">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="dcd6e-2962">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2962">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="dcd6e-2963">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2963">General</span></span>

- <span data-ttu-id="dcd6e-2964">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2964">General Availability of Az Module</span></span>
- <span data-ttu-id="dcd6e-2965">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2965">Online help for each module</span></span>
- <span data-ttu-id="dcd6e-2966">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2966">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="dcd6e-2967">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2967">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="dcd6e-2968">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2968">Az.Accounts</span></span>
- <span data-ttu-id="dcd6e-2969">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2969">Changed from Az.Profile</span></span>
- <span data-ttu-id="dcd6e-2970">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2970">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-2971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2971">Az.ApiManagement</span></span>
- <span data-ttu-id="dcd6e-2972">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2972">Fixes for #7002</span></span>
- <span data-ttu-id="dcd6e-2973">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="dcd6e-2974">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2974">Az.Batch</span></span>
- <span data-ttu-id="dcd6e-2975">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2975">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="dcd6e-2976">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2976">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="dcd6e-2977">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2977">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="dcd6e-2978">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2978">Az.Billing</span></span>
- <span data-ttu-id="dcd6e-2979">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2979">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="dcd6e-2980">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2980">Az.CognitivServices</span></span>
- <span data-ttu-id="dcd6e-2981">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2981">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="dcd6e-2982">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2982">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dcd6e-2983">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2983">Az.ContainerInstance</span></span>
- <span data-ttu-id="dcd6e-2984">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2984">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="dcd6e-2985">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2985">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="dcd6e-2986">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2986">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2987">Az.DataLakeStore</span></span>
- <span data-ttu-id="dcd6e-2988">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2988">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="dcd6e-2989">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2989">Az.Monitor</span></span>
- <span data-ttu-id="dcd6e-2990">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2990">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="dcd6e-2991">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2991">Az.KeyVault</span></span>
- <span data-ttu-id="dcd6e-2992">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2992">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="dcd6e-2993">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2993">Az.MachineLearning</span></span>
- <span data-ttu-id="dcd6e-2994">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2994">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="dcd6e-2995">Az.Media</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2995">Az.Media</span></span>
- <span data-ttu-id="dcd6e-2996">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2996">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dcd6e-2997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2997">Az.Network</span></span>
<span data-ttu-id="dcd6e-2998">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2998">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="dcd6e-2999">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="dcd6e-2999">New cmdlets added:</span></span>
        - <span data-ttu-id="dcd6e-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dcd6e-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dcd6e-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dcd6e-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dcd6e-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="dcd6e-3005">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3005">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="dcd6e-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="dcd6e-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="dcd6e-3008">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3008">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="dcd6e-3009">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3009">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="dcd6e-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dcd6e-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="dcd6e-3012">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3012">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="dcd6e-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="dcd6e-3014">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3014">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="dcd6e-3015">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3015">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="dcd6e-3016">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3016">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dcd6e-3017">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3017">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="dcd6e-3018">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3018">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="dcd6e-3019">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3019">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="dcd6e-3020">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3020">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="dcd6e-3021">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3021">Az.OperationalInsights</span></span>
- <span data-ttu-id="dcd6e-3022">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3022">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="dcd6e-3023">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3023">Az.Profile</span></span>
- <span data-ttu-id="dcd6e-3024">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3024">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-3025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3025">Az.RecoveryServices</span></span>
- <span data-ttu-id="dcd6e-3026">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3026">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="dcd6e-3027">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3027">Az.Resources</span></span>
- <span data-ttu-id="dcd6e-3028">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3028">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-3029">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3029">Az.ServiceFabric</span></span>
- <span data-ttu-id="dcd6e-3030">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3030">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="dcd6e-3031">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3031">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="dcd6e-3032">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3032">Az.SIgnalR</span></span>
- <span data-ttu-id="dcd6e-3033">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3033">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="dcd6e-3034">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3034">Az.Sql</span></span>
- <span data-ttu-id="dcd6e-3035">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3035">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="dcd6e-3036">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3036">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="dcd6e-3037">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3037">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="dcd6e-3038">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3038">Az.Storage</span></span>
- <span data-ttu-id="dcd6e-3039">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3039">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dcd6e-3040">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3040">Az.Websites</span></span>
- <span data-ttu-id="dcd6e-3041">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3041">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="dcd6e-3042">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3042">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="dcd6e-3043">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3043">General</span></span>

* <span data-ttu-id="dcd6e-3044">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3044">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="dcd6e-3045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3045">Az.Compute</span></span>

* <span data-ttu-id="dcd6e-3046">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3046">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-3047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3047">Az.DataLakeStore</span></span>

* <span data-ttu-id="dcd6e-3048">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3048">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="dcd6e-3049">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3049">Az.FrontDoor</span></span>

* <span data-ttu-id="dcd6e-3050">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3050">Fixed some broken links</span></span>
    - <span data-ttu-id="dcd6e-3051">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3051">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="dcd6e-3052">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3052">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="dcd6e-3053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3053">Az.RecoveryServices</span></span>

* <span data-ttu-id="dcd6e-3054">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3054">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="dcd6e-3055">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3055">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="dcd6e-3056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3056">Az.Resources</span></span>

* <span data-ttu-id="dcd6e-3057">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3057">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="dcd6e-3058">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3058">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="dcd6e-3059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3059">Az.Sql</span></span>

* <span data-ttu-id="dcd6e-3060">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3060">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="dcd6e-3061">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3061">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="dcd6e-3062">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3062">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="dcd6e-3063">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3063">Az.Storage</span></span>

* <span data-ttu-id="dcd6e-3064">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3064">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="dcd6e-3065">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3065">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="dcd6e-3066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dcd6e-3067">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3067">Support Static Website configuration</span></span>
    - <span data-ttu-id="dcd6e-3068">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3068">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="dcd6e-3069">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3069">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="dcd6e-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3070">Az.Websites</span></span>

* <span data-ttu-id="dcd6e-3071">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3071">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="dcd6e-3072">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3072">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="dcd6e-3073">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3073">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="dcd6e-3074">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3074">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="dcd6e-3075">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3075">Az.ApiManagement</span></span>
* <span data-ttu-id="dcd6e-3076">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3076">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="dcd6e-3077">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3077">Az.Automation</span></span>
* <span data-ttu-id="dcd6e-3078">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3078">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="dcd6e-3079">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3079">Added Update Management cmdlets</span></span>
* <span data-ttu-id="dcd6e-3080">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3080">Added Source Control cmdlets</span></span>
* <span data-ttu-id="dcd6e-3081">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3081">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="dcd6e-3082">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3082">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="dcd6e-3083">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3083">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-3084">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3084">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="dcd6e-3085">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3085">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="dcd6e-3086">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3086">Az.ContainerInstance</span></span>
* <span data-ttu-id="dcd6e-3087">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3087">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="dcd6e-3088">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3088">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="dcd6e-3089">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3089">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="dcd6e-3090">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3090">Az.Network</span></span>
* <span data-ttu-id="dcd6e-3091">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3091">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="dcd6e-3092">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3092">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="dcd6e-3093">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3093">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="dcd6e-3094">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3094">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="dcd6e-3095">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3095">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="dcd6e-3096">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3096">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="dcd6e-3097">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3097">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="dcd6e-3098">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3098">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="dcd6e-3099">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3099">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="dcd6e-3100">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3100">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="dcd6e-3101">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3101">Az.Relay</span></span>
* <span data-ttu-id="dcd6e-3102">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3102">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="dcd6e-3103">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3103">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-3104">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3104">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="dcd6e-3105">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3105">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="dcd6e-3106">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3106">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-3107">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3107">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-3108">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3108">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="dcd6e-3109">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3109">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-3110">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3110">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="dcd6e-3111">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3111">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dcd6e-3112">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3112">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dcd6e-3113">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3113">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dcd6e-3114">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3114">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="dcd6e-3115">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3115">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dcd6e-3116">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3116">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dcd6e-3117">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3117">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="dcd6e-3118">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3118">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="dcd6e-3119">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3119">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="dcd6e-3120">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3120">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="dcd6e-3121">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3121">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="dcd6e-3122">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3122">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dcd6e-3123">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3123">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="dcd6e-3124">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3124">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="dcd6e-3125">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3125">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="dcd6e-3126">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3126">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="dcd6e-3127">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3127">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="dcd6e-3128">Geral</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3128">General</span></span>
* <span data-ttu-id="dcd6e-3129">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3129">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="dcd6e-3130">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3130">Az.Profile</span></span>
* <span data-ttu-id="dcd6e-3131">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3131">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="dcd6e-3132">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3132">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="dcd6e-3133">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3133">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="dcd6e-3134">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3134">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="dcd6e-3135">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3135">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="dcd6e-3136">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3136">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="dcd6e-3137">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3137">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-3138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3138">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-3139">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3139">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-3140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3140">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-3141">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3141">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="dcd6e-3142">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3142">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="dcd6e-3143">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3143">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-3144">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3144">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-3145">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3145">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="dcd6e-3146">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3146">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="dcd6e-3147">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3147">Az.Insights</span></span>
* <span data-ttu-id="dcd6e-3148">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3148">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="dcd6e-3149">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3149">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="dcd6e-3150">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3150">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="dcd6e-3151">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3151">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-3152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3152">Az.Network</span></span>
* <span data-ttu-id="dcd6e-3153">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3153">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="dcd6e-3154">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3154">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="dcd6e-3155">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3155">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="dcd6e-3156">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3156">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="dcd6e-3157">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3157">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="dcd6e-3158">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3158">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="dcd6e-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="dcd6e-3160">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3160">Az.PolicyInsights</span></span>
* <span data-ttu-id="dcd6e-3161">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3161">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-3162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3162">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-3163">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3163">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="dcd6e-3164">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3164">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="dcd6e-3165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3165">Az.ServiceBus</span></span>
* <span data-ttu-id="dcd6e-3166">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3166">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="dcd6e-3167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3167">Az.ServiceFabric</span></span>
* <span data-ttu-id="dcd6e-3168">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3168">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="dcd6e-3169">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3169">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="dcd6e-3170">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3170">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="dcd6e-3171">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3171">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="dcd6e-3172">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3172">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="dcd6e-3173">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3173">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="dcd6e-3174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3174">Az.Profile</span></span>
* <span data-ttu-id="dcd6e-3175">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3175">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="dcd6e-3176">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3176">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-3177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3177">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-3178">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3178">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="dcd6e-3179">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3179">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="dcd6e-3180">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3180">Az.DataLakeStore</span></span>
* <span data-ttu-id="dcd6e-3181">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3181">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="dcd6e-3182">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3182">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="dcd6e-3183">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3183">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dcd6e-3184">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3184">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="dcd6e-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-3186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3186">Az.Network</span></span>
* <span data-ttu-id="dcd6e-3187">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3187">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="dcd6e-3188">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3188">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-3189">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3189">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-3190">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3190">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="dcd6e-3191">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3191">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="dcd6e-3192">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3192">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="dcd6e-3193">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3193">Azure.Storage</span></span>
* <span data-ttu-id="dcd6e-3194">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3194">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="dcd6e-3195">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3195">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="dcd6e-3196">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3196">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="dcd6e-3197">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3197">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="dcd6e-3198">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3198">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="dcd6e-3199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3199">Az.CognitiveServices</span></span>
* <span data-ttu-id="dcd6e-3200">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3200">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="dcd6e-3201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3201">Az.Compute</span></span>
* <span data-ttu-id="dcd6e-3202">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3202">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="dcd6e-3203">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3203">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="dcd6e-3204">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3204">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="dcd6e-3205">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3205">Az.DataFactoryV2</span></span>
* <span data-ttu-id="dcd6e-3206">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3206">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="dcd6e-3207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3207">Az.Network</span></span>
* <span data-ttu-id="dcd6e-3208">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3208">Added NetworkProfile functionality.</span></span> <span data-ttu-id="dcd6e-3209">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3209">new cmdlets added</span></span>
    - <span data-ttu-id="dcd6e-3210">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3210">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="dcd6e-3211">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3211">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="dcd6e-3212">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3212">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="dcd6e-3213">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3213">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="dcd6e-3214">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3214">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="dcd6e-3215">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3215">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="dcd6e-3216">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3216">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="dcd6e-3217">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3217">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="dcd6e-3218">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3218">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="dcd6e-3219">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3219">Az.RedisCache</span></span>
* <span data-ttu-id="dcd6e-3220">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3220">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="dcd6e-3221">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3221">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="dcd6e-3222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3222">Az.Resources</span></span>
* <span data-ttu-id="dcd6e-3223">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3223">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="dcd6e-3224">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3224">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="dcd6e-3225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3225">Az.Sql</span></span>
* <span data-ttu-id="dcd6e-3226">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3226">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="dcd6e-3227">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3227">Az.Websites</span></span>
* <span data-ttu-id="dcd6e-3228">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3228">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="dcd6e-3229">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3229">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="dcd6e-3230">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3230">0.2.0 - September 2018</span></span>
 <span data-ttu-id="dcd6e-3231">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="dcd6e-3231">Initial Release</span></span>
