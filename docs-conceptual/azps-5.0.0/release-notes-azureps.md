---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 5eac1bee53bfadf57d053ad60d6267657b145d67
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427132"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="2d8a5-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d8a5-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="2d8a5-104">5.0.0 – outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-105">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-106">[Alteração da Falha] Remoção de 'Get-AzProfile' e 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="2d8a5-107">Substituição da Biblioteca de Autenticação do Azure Directory pela MSAL (Biblioteca de Autenticação da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-108">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-109">[Alteração da Falha] Remoção do alias do parâmetro 'ClientIdAndSecret' em 'New-AzAksCluster' e 'Set-AzAksCluster'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="2d8a5-110">[Alteração da Falha] Alteração do valor padrão de 'NodeVmSetType' em 'New-AzAksCluster' de 'AvailabilitySet' para 'VirtualMachineScaleSets'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="2d8a5-111">[Alteração da Falha] Alteração do valor padrão de 'NetworkPlugin' em 'New-AzAksCluster' de 'None' para 'azure'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="2d8a5-112">[Alteração da Falha] Remoção do parâmetro 'NodeOsType' em 'New-AzAksCluster', pois ele é compatível somente com um valor Linux.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="2d8a5-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d8a5-113">Az.Billing</span></span>
* <span data-ttu-id="2d8a5-114">Adição do cmdlet 'Get-AzBillingAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="2d8a5-115">Adição do cmdlet 'Get-AzBillingProfile'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="2d8a5-116">Adição do cmdlet 'Get-AzInvoiceSection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="2d8a5-117">Adição de novos parâmetros ao cmdlet 'Get-AzBillingInvoice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="2d8a5-118">Remoção das propriedades DownloadUrlExpiry, Type e BillingPeriodNames da resposta do cmdlet Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="2d8a5-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-119">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-120">Adição de cmdlets para dar suporte a uma funcionalidade de link privado e várias origens</span><span class="sxs-lookup"><span data-stu-id="2d8a5-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-122">Atualização do SDK para 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-123">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-124">Adição do parâmetro '-VmssId ' ao 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="2d8a5-125">Adição do parâmetro 'PlatformFaultDomainCount' ao cmdlet 'New-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-126">Novo cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="2d8a5-127">Adição dos parâmetros opcionais 'Tier' e 'LogicalSectorSize' ao cmdlet New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="2d8a5-128">Adição dos parâmetros opcionais 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' e 'DiskMBpsReadOnly' ao cmdlet 'New-AzDiskUpdateConfig'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d8a5-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d8a5-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d8a5-130">[Alteração da Falha] Atualiza a versão da API para a 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="2d8a5-130">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="2d8a5-131">[Alteração da Falha] Remoção do SKU 'Classic' e do parâmetro 'StorageAccountName' de 'New-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="2d8a5-132">Adição de novos cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule' e 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="2d8a5-133">Adição do novo parâmetro 'NetworkRuleSet' ao 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="2d8a5-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-134">Az.Databricks</span></span>
* <span data-ttu-id="2d8a5-135">Correção de um bug que pode causar a atualização do workspace do Databricks sem que ocorra falha do `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-136">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-137">Atualização do SDK do .NET do ADF para a versão 4.12.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="2d8a5-138">Atualização do SDK cliente da criptografia do ADF para a versão 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="2d8a5-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="2d8a5-139">Adição dos comandos 'Stop-AzDataFactoryV2TriggerRun' e 'Invoke-AzDataFactoryV2TriggerRun'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="2d8a5-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="2d8a5-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="2d8a5-141">Exigir a propriedade Location para criar objetos ARM de nível superior.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="2d8a5-142">\* `ApplicationGroupType` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="2d8a5-143">\* `HostPoolArmPath` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="2d8a5-144">\* Adição do `PreferredAppGroupType` ao `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d8a5-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d8a5-145">Az.Functions</span></span>
* <span data-ttu-id="2d8a5-146">[Alteração da Falha] Remoção do parâmetro de opção 'IncludeSlot' de todos os parâmetros, exceto de um conjunto de parâmetros de 'Get-AzFunctionApp'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="2d8a5-147">O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados em que '-IncludeSlot' for especificado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="2d8a5-148">Atualização do 'New-AzFunctionApp':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="2d8a5-149">Correção do -DisableApplicationInsights para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="2d8a5-150">[Nº 12728]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-150">[#12728]</span></span>
  - <span data-ttu-id="2d8a5-151">[Alteração da Falha] Remoção do suporte para criar aplicativos de funções do PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="2d8a5-152">[Alteração da Falha] Alteração da versão de runtime padrão da 6.2 para a 7.0 do Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="2d8a5-153">[Alteração da Falha] Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="2d8a5-154">[Alteração da Falha] Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-155">Az.HDInsight</span></span>
 * <span data-ttu-id="2d8a5-156">Para o cmdlet New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="2d8a5-157">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="2d8a5-158">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="2d8a5-159">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="2d8a5-160">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="2d8a5-161">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="2d8a5-162">Adição de novos parâmetros: 'StorageFileSystem' e 'StorageAccountManagedIdentity' para dar suporte ao ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="2d8a5-163">Adição do novo parâmetro 'EnableIDBroker' para dar suporte ao Agente de IDs do HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="2d8a5-164">Adição de novos parâmetros: Parâmetros 'KafkaClientGroupId', 'KafkaClientGroupName' e 'KafkaManagementNodeSize' para dar suporte ao Proxy REST do Kafka</span><span class="sxs-lookup"><span data-stu-id="2d8a5-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="2d8a5-165">Para o cmdlet New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="2d8a5-166">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="2d8a5-167">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="2d8a5-168">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="2d8a5-169">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="2d8a5-170">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="2d8a5-171">Para o cmdlet Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="2d8a5-172">Substituição do parâmetro 'StorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="2d8a5-173">Para o cmdlet Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="2d8a5-174">Substituição do parâmetro 'Domain' por 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="2d8a5-175">Remoção do requisito obrigatório para o parâmetro 'OrganizationalUnitDN'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-176">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-177">[Alteração da Falha] O parâmetro DisableSoftDelete foi preterido em 'New-AzKeyVault', bem como EnableSoftDelete em 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="2d8a5-178">[Alteração da Falha] Remoção do atributo SecretValueText para evitar a exibição de SecretValue de modo direto [Nº 12266]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="2d8a5-179">Um novo tipo de recurso é compatível: HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="2d8a5-180">Comandos CRUD de cmdlets e do HSM gerenciado para operar chaves no HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="2d8a5-181">Backup/restauração completos do HSM, criação de chave AES, backup/restauração do domínio de segurança e RBAC</span><span class="sxs-lookup"><span data-stu-id="2d8a5-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d8a5-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-182">Az.ManagedServices</span></span>
* <span data-ttu-id="2d8a5-183">[Alteração da Falha] Atualização de parâmetros de convenções de nomenclatura e exemplos associados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-184">Az.Network</span></span>
* <span data-ttu-id="2d8a5-185">[Alteração da Falha] Remoção do parâmetro 'HostedSubnet' e adição de 'Subnet' como alternativa</span><span class="sxs-lookup"><span data-stu-id="2d8a5-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="2d8a5-186">Adição de novos cmdlets às Rotas do Par no Nível do Roteador Virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="2d8a5-187">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="2d8a5-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="2d8a5-189">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="2d8a5-190">Adição do parâmetro '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="2d8a5-191">Adição do parâmetro '-SkuName' e, para isso, o SKU foi executado com um Alias</span><span class="sxs-lookup"><span data-stu-id="2d8a5-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="2d8a5-192">Remoção do parâmetro '-Sku'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="2d8a5-193">[Alteração da Falha] O argumento 'Connectionlink' agora é obrigatório em 'Start-AzVpnConnectionPacketCapture' e 'Stop-AzVpnConnectionPacketCapture'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="2d8a5-194">[Alteração da Falha] Atualização do 'New-AzNetworkWatcherConnectionMonitorEndPointObject' para remover o parâmetro '-Filter'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="2d8a5-195">[Alteração da Falha] Substituição do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' por 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="2d8a5-196">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndPointObject':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="2d8a5-197">Adição do parâmetro '-Type'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="2d8a5-198">Adição do parâmetro '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="2d8a5-199">Adição do parâmetro '-Scope'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="2d8a5-200">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' com o novo parâmetro '-DestinationPortBehavior'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-202">Correção da Restauração da Carga de Trabalho para permissões de colaborador.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="2d8a5-203">Adição de novos conjuntos e novas validações de parâmetros ao cmdlet Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-204">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-205">Correção de um bug de análise</span><span class="sxs-lookup"><span data-stu-id="2d8a5-205">Fixed parsing bug</span></span>
* <span data-ttu-id="2d8a5-206">Atualização de cmdlets What-If do modelo do ARM para remover uma mensagem de visualização dos resultados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="2d8a5-207">Correção de um problema em que ocorria falha nos cmdlets de implantação de modelo caso '-WhatIf' fosse definido em um escopo maior [Nº13038]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="2d8a5-208">Correção de um problema em que cmdlets de implantação de modelo não preservavam maiúsculas e minúsculas para parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="2d8a5-209">Adição de uma versão de API padrão para ser usada no cmdlet 'Export-AzResourceGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="2d8a5-210">Adição de cmdlets às Especificações de Modelo ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec' e 'Export-AzTemplateSpec')</span><span class="sxs-lookup"><span data-stu-id="2d8a5-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="2d8a5-211">Adição de um suporte para implantar Especificações de Modelo usando cmdlets de implantação existentes (por meio do novo parâmetro -TemplateSpecId)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="2d8a5-212">Atualização do parâmetro 'Get-AzResourceGroupDeploymentOperation' para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="2d8a5-213">Remoção do parâmetro '-ApiVersion' de cmdlets '\*-AzDeployment'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-214">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-215">Correção de um problema em que ocorria uma falha de New-AzSqlDatabaseExport caso networkIsolation não fosse especificado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-215">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="2d8a5-216">Correção de um problema em que New-AzSqlDatabaseExport e New-AzSqlDatabaseImport não retornavam OperationStatusLink no objeto de resultado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-216">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="2d8a5-217">Atualizar a URL de regiões emparelhadas do Azure em avisos de redundância de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-217">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-218">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-219">Remoção da propriedade obsoleta RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="2d8a5-219">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="2d8a5-220">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-220">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d8a5-221">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-221">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d8a5-222">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-222">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="2d8a5-223">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-223">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="2d8a5-224">Alterar o Tipo de DaysAfterModificationGreaterThan de int para int?</span><span class="sxs-lookup"><span data-stu-id="2d8a5-224">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="2d8a5-225">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-225">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d8a5-226">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-226">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d8a5-227">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-227">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="2d8a5-228">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-228">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="2d8a5-229">Criação/atualização de compartilhamento de arquivo compatível com uma camada de acesso</span><span class="sxs-lookup"><span data-stu-id="2d8a5-229">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="2d8a5-230">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-230">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="2d8a5-231">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-231">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="2d8a5-232">Definição/atualização/removção recursiva de ACL compatível com um item do Datalake Gen2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-232">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="2d8a5-233">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-233">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="2d8a5-234">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-234">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="2d8a5-235">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-235">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="2d8a5-236">Política de acesso de Contêiner compatível com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="2d8a5-236">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="2d8a5-237">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-237">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="2d8a5-238">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-238">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="2d8a5-239">Alteração da saída do cmdlet da política de acesso ao Contêiner get/set mudando o tipo de Permissão de propriedade filho de enum para String</span><span class="sxs-lookup"><span data-stu-id="2d8a5-239">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="2d8a5-240">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-240">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="2d8a5-241">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-241">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="2d8a5-242">Correção de um problema do script de exemplo da política de gerenciamento de conjuntos com JSON</span><span class="sxs-lookup"><span data-stu-id="2d8a5-242">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="2d8a5-243">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-243">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-244">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-245">Adição de suporte para o tipo de preço Premium V3</span><span class="sxs-lookup"><span data-stu-id="2d8a5-245">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="2d8a5-246">Atualização do SDK de Sites para a versão 3.1.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-246">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d8a5-247">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="2d8a5-247">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d8a5-248">@atul-ram, por atualizar Get-AzDelegation.md (nº 13176)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-248">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="2d8a5-249">@dineshreddy007, por obter as Funções de Aplicativos atribuídas de modo correto em caso de registro do Stack HCI usando um token WAC.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-249">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="2d8a5-250">(nº 13249)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-250">(#13249)</span></span>
* <span data-ttu-id="2d8a5-251">@kongou-ae, por atualizar New-AzOffice365PolicyProperty.md (nº 13217)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-251">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="2d8a5-252">Lohith Chowdary Chilukuri (@Lochiluk), por atualizar Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-252">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="2d8a5-253">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-253">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="2d8a5-254">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13203)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-254">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="2d8a5-255">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13190)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-255">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="2d8a5-256">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13189)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-256">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="2d8a5-257">Adicionar links aos cmdlets referenciados (nº 13137)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-257">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="2d8a5-258">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13204)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-258">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="2d8a5-259">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13205)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-259">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="2d8a5-260">4.8.0 – Outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-260">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-261">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-261">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-262">Foi corrigido um problema de análise de datetime em bibliotecas comuns [#13045]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-262">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-263">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-263">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-264">Foi adicionado o cmdlet 'New-AzCognitiveServicesAccountApiProperty'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-264">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-265">Parâmetro 'ApiProperty' compatível com 'New-AzCognitiveServicesAccount' e 'Set-AzCognitiveServicesAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-265">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-266">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-266">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-267">Foi corrigido o problema em 'Update-ASRRecoveryPlan' populando o FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-267">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="2d8a5-268">Foram adicionados os parâmetros opcionais '-Top' e '-OrderBy' ao cmdlet 'Get-AzVmImage'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-268">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="2d8a5-269">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-269">Az.Databricks</span></span>
* <span data-ttu-id="2d8a5-270">Disponibilidade geral do módulo 'Az.Databricks'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-270">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="2d8a5-271">Foi adicionado suporte para emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-271">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-272">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-273">Foi corrigido erro de digitação nas mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="2d8a5-273">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-274">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-274">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-275">Foi adicionado o parâmetro de opção opcional 'TrustedServiceAccessEnabled' ao cmdlet 'Set-AzEventHubNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-275">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-276">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-276">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-277">Foi adicionada uma mensagem de aviso para planejamento do preterimento dos parâmetros 'PublicNetworkAccessType' e 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-277">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="2d8a5-278">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-278">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="2d8a5-279">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="2d8a5-280">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="2d8a5-281">Adicionada mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageContainer' por 'StorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-281">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="2d8a5-282">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageRootPath' por 'StorageRootPath'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-282">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-283">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-283">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-284">O SDK de dispositivos foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-284">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-285">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-285">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-286">A data detalhada da remoção da propriedade SecretValueText foi fornecida</span><span class="sxs-lookup"><span data-stu-id="2d8a5-286">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d8a5-287">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-287">Az.ManagedServices</span></span>
* <span data-ttu-id="2d8a5-288">Os avisos de alteração da falha nos cmdlets de definição e atribuição de serviços gerenciados foram atualizados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-288">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-289">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-290">Foi corrigido o bug que fazia com que a mensagem de aviso não pudesse ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-290">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="2d8a5-291">[#12889]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-291">[#12889]</span></span>
* <span data-ttu-id="2d8a5-292">Parâmetro 'SkipMetricValidation' com suporte nos critérios da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-292">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="2d8a5-293">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação da métrica seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-293">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-294">Az.Network</span></span>
* <span data-ttu-id="2d8a5-295">Política do Office365 adicionada ao recurso VPNSite</span><span class="sxs-lookup"><span data-stu-id="2d8a5-295">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="2d8a5-296">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-296">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-298">Foi adicionada a validação do nome do contêiner para backup da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-298">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d8a5-299">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-299">Az.RedisCache</span></span>
* <span data-ttu-id="2d8a5-300">Correção dos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache' para não falharem devido a um problema de permissão relacionado ao registro do RP do Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-300">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-301">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-302">Foi adicionado BackupStorageRedundancy ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-302">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="2d8a5-303">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-303">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="2d8a5-304">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-304">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="2d8a5-305">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-305">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="2d8a5-306">Foi removida a diferenciação de maiúsculas e minúsculas para o parâmetro BackupStorageRedundancy em todas as referências de Banco de Dados SQL</span><span class="sxs-lookup"><span data-stu-id="2d8a5-306">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="2d8a5-307">Foram atualizados os nomes das mensagens de aviso do BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-307">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-308">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-309">Suporte para habilitar/desabilitar/obter propriedades de exclusão reversível de compartilhamento no serviço de arquivo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-309">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="2d8a5-310">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-310">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="2d8a5-311">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-311">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="2d8a5-312">Os compartilhamentos de arquivos de lista com suporte incluem os excluídos de uma conta de armazenamento e obtêm uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="2d8a5-312">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="2d8a5-313">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-313">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="2d8a5-314">Suporte para restauração de um compartilhamento de arquivo excluído</span><span class="sxs-lookup"><span data-stu-id="2d8a5-314">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="2d8a5-315">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-315">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="2d8a5-316">Foram alterados os cmdlets para modificar as propriedades do serviço blobs, não obtendo as propriedades originais do servidor, mas apenas definindo as propriedades modificadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-316">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="2d8a5-317">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-317">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="2d8a5-318">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-318">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="2d8a5-319">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-319">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d8a5-320">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-320">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d8a5-321">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-321">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="2d8a5-322">Foi corrigido o problema de ajuda para o valor padrão do tipo do parâmetro New-AzStorageAccount [#12189]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-322">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="2d8a5-323">Foi corrigido o problema adicionando exemplo para mostrar como definir o ContentType correto no upload do blob [#12989]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-323">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="2d8a5-324">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-324">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-325">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-325">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-326">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-326">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="2d8a5-327">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="2d8a5-327">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-328">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-328">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-329">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-329">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="2d8a5-330">[#12372]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-330">[#12372]</span></span>
* <span data-ttu-id="2d8a5-331">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-331">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="2d8a5-332">[#11239]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-332">[#11239]</span></span>
* <span data-ttu-id="2d8a5-333">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-333">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="2d8a5-334">[#11239]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-334">[#11239]</span></span>
* <span data-ttu-id="2d8a5-335">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-335">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="2d8a5-336">[#12371]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-336">[#12371]</span></span>
* <span data-ttu-id="2d8a5-337">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-337">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-338">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-338">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-339">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-339">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-340">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-341">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-341">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="2d8a5-342">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-342">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="2d8a5-343">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-343">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="2d8a5-344">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="2d8a5-345">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2d8a5-345">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="2d8a5-346">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-346">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="2d8a5-347">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-347">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="2d8a5-348">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-348">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="2d8a5-349">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-349">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="2d8a5-350">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-350">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-351">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-351">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-352">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-352">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-353">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-353">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-354">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-354">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="2d8a5-355">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-355">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d8a5-356">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d8a5-356">Az.Functions</span></span>
* <span data-ttu-id="2d8a5-357">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-357">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="2d8a5-358">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-358">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="2d8a5-359">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-359">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-360">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-360">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-361">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="2d8a5-361">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="2d8a5-362">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-362">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="2d8a5-363">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="2d8a5-363">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="2d8a5-364">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-364">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-365">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-365">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-366">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-366">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-367">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-367">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-368">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-368">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-369">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-369">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-370">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-370">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="2d8a5-371">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-371">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="2d8a5-372">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="2d8a5-372">Az.Kusto</span></span>
* <span data-ttu-id="2d8a5-373">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-373">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-374">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-374">Az.Network</span></span>
* <span data-ttu-id="2d8a5-375">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-375">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="2d8a5-376">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-376">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="2d8a5-377">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="2d8a5-377">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="2d8a5-378">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-378">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="2d8a5-379">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-379">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="2d8a5-380">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-380">Added subscription level parameter set</span></span>
    - <span data-ttu-id="2d8a5-381">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-381">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="2d8a5-382">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-382">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="2d8a5-383">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-383">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="2d8a5-384">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-384">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="2d8a5-385">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-385">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="2d8a5-386">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-386">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="2d8a5-387">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2d8a5-387">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="2d8a5-388">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-388">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="2d8a5-389">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-389">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="2d8a5-390">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-390">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="2d8a5-391">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-391">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="2d8a5-392">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-392">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="2d8a5-393">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-393">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="2d8a5-394">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-394">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="2d8a5-395">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-395">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="2d8a5-396">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-396">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="2d8a5-397">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-397">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="2d8a5-398">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-398">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-399">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-399">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-400">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-400">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-401">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-402">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-402">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="2d8a5-403">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-403">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="2d8a5-404">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="2d8a5-404">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="2d8a5-405">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-405">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-406">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-407">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-407">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="2d8a5-408">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-408">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d8a5-409">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-409">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d8a5-410">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-410">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d8a5-411">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-411">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="2d8a5-412">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-412">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="2d8a5-413">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-413">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="2d8a5-414">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-414">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d8a5-415">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-415">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d8a5-416">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-416">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d8a5-417">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-417">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="2d8a5-418">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-418">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="2d8a5-419">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-419">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="2d8a5-420">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-420">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="2d8a5-421">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-421">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="2d8a5-422">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-422">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-423">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-424">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-424">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="2d8a5-425">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-425">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d8a5-426">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-426">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d8a5-427">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-427">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="2d8a5-428">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-428">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="2d8a5-429">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-429">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="2d8a5-430">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-430">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="2d8a5-431">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-431">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="2d8a5-432">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-432">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="2d8a5-433">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-433">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d8a5-434">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-434">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d8a5-435">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-435">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d8a5-436">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="2d8a5-436">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="2d8a5-437">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-437">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="2d8a5-438">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-438">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="2d8a5-439">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-439">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="2d8a5-440">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-440">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="2d8a5-441">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-441">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-442">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-443">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-443">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="2d8a5-444">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="2d8a5-444">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="2d8a5-445">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-445">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d8a5-446">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-446">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="2d8a5-447">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-447">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="2d8a5-448">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-448">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="2d8a5-449">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-449">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="2d8a5-450">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-450">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="2d8a5-451">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="2d8a5-451">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="2d8a5-452">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-452">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="2d8a5-453">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-453">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="2d8a5-454">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-454">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d8a5-455">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-455">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="2d8a5-456">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-456">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="2d8a5-457">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-457">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="2d8a5-458">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="2d8a5-458">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="2d8a5-459">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="2d8a5-459">Thanks to our community contributors</span></span>
* <span data-ttu-id="2d8a5-460">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-460">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="2d8a5-461">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-461">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="2d8a5-462">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-462">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="2d8a5-463">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-463">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="2d8a5-464">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-464">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="2d8a5-465">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-465">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="2d8a5-466">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-466">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="2d8a5-467">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-467">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="2d8a5-468">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-468">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="2d8a5-469">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-469">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="2d8a5-470">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-470">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="2d8a5-471">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-471">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="2d8a5-472">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-472">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-473">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-473">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="2d8a5-474">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-474">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-475">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-475">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-476">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-476">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="2d8a5-477">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-477">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-478">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-478">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-479">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="2d8a5-479">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-480">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-480">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-481">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-481">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="2d8a5-482">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-482">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="2d8a5-483">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-483">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="2d8a5-484">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-484">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-485">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-486">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-486">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-487">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-487">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-488">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-488">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-489">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-490">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="2d8a5-490">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="2d8a5-491">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="2d8a5-491">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="2d8a5-492">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-492">Az.Maintenance</span></span>
* <span data-ttu-id="2d8a5-493">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-493">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="2d8a5-494">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-494">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d8a5-495">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-495">Az.ManagedServices</span></span>
* <span data-ttu-id="2d8a5-496">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-496">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-497">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-498">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-498">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="2d8a5-499">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="2d8a5-499">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-500">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-500">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-501">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-501">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="2d8a5-502">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-502">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="2d8a5-503">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-503">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="2d8a5-504">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="2d8a5-504">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="2d8a5-505">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-505">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="2d8a5-506">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="2d8a5-506">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="2d8a5-507">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-507">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="2d8a5-508">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="2d8a5-508">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d8a5-509">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-509">Az.SignalR</span></span>
* <span data-ttu-id="2d8a5-510">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-510">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="2d8a5-511">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-511">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-512">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-512">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-513">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="2d8a5-513">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="2d8a5-514">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-514">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="2d8a5-515">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-515">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="2d8a5-516">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-516">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="2d8a5-517">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-517">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="2d8a5-518">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-518">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="2d8a5-519">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-519">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="2d8a5-520">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-520">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="2d8a5-521">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-521">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="2d8a5-522">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-522">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="2d8a5-523">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-523">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="2d8a5-524">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-524">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="2d8a5-525">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-525">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="2d8a5-526">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-526">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="2d8a5-527">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-527">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="2d8a5-528">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-528">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-529">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-529">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-530">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-530">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="2d8a5-531">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-531">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="2d8a5-532">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-532">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="2d8a5-533">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-533">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="2d8a5-534">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="2d8a5-534">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-535">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-536">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="2d8a5-536">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="2d8a5-537">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="2d8a5-537">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-538">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-538">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-539">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-539">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-540">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-540">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-541">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-541">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-542">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-542">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-543">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-543">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-544">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-544">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-545">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-545">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-546">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-546">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-547">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-547">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-548">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-548">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-549">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-549">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-550">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-550">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-551">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-551">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-552">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-552">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-553">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-553">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-554">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-554">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-555">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-556">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-556">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="2d8a5-557">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2d8a5-557">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="2d8a5-558">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="2d8a5-559">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-559">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="2d8a5-560">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2d8a5-560">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="2d8a5-561">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="2d8a5-562">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2d8a5-562">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-563">Az.Network</span></span>
* <span data-ttu-id="2d8a5-564">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="2d8a5-565">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-565">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="2d8a5-566">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-566">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="2d8a5-567">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-567">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-568">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-568">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-569">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-569">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="2d8a5-570">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-570">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="2d8a5-571">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-571">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-572">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-572">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-573">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-573">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-574">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-574">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-575">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-575">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="2d8a5-576">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-576">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-577">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-578">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-578">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="2d8a5-579">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2d8a5-579">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-580">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-580">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-581">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="2d8a5-581">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="2d8a5-582">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-582">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="2d8a5-583">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2d8a5-583">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="2d8a5-584">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="2d8a5-584">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="2d8a5-585">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="2d8a5-585">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="2d8a5-586">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="2d8a5-586">Supported get single file share usage</span></span>
    - <span data-ttu-id="2d8a5-587">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-587">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="2d8a5-588">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-588">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-589">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-589">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-590">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-590">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="2d8a5-591">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-591">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-592">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-592">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-593">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-593">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d8a5-594">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-594">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d8a5-595">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-595">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-596">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-596">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-597">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-597">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-598">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-598">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-599">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-599">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-600">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-600">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-601">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-601">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d8a5-602">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d8a5-602">Az.EventGrid</span></span>
* <span data-ttu-id="2d8a5-603">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-603">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="2d8a5-604">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-604">Added new features:</span></span>
    - <span data-ttu-id="2d8a5-605">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-605">Input mapping</span></span>
    - <span data-ttu-id="2d8a5-606">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-606">Event Delivery Schema</span></span>
    - <span data-ttu-id="2d8a5-607">Link Privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-607">Private Link</span></span>
    - <span data-ttu-id="2d8a5-608">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="2d8a5-608">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="2d8a5-609">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="2d8a5-609">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="2d8a5-610">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="2d8a5-610">Azure Function As Destination</span></span>
    - <span data-ttu-id="2d8a5-611">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-611">WebHook Batching</span></span>
    - <span data-ttu-id="2d8a5-612">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-612">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="2d8a5-613">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="2d8a5-613">IpFiltering</span></span>
* <span data-ttu-id="2d8a5-614">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-614">Updated cmdlets:</span></span>
    - <span data-ttu-id="2d8a5-615">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-615">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="2d8a5-616">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-616">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="2d8a5-617">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-617">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="2d8a5-618">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-618">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="2d8a5-619">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-619">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="2d8a5-620">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-620">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="2d8a5-621">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-621">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="2d8a5-622">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-622">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="2d8a5-623">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-623">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-624">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-624">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-625">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="2d8a5-625">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="2d8a5-626">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-626">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-627">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-627">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-628">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-628">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-629">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-629">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-630">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-630">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-631">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-631">Az.Network</span></span>
* <span data-ttu-id="2d8a5-632">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-632">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="2d8a5-633">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-633">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="2d8a5-634">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-634">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d8a5-635">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-635">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d8a5-636">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-636">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d8a5-637">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-637">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="2d8a5-638">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-638">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="2d8a5-639">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-639">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="2d8a5-640">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-640">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d8a5-641">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-641">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d8a5-642">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-642">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d8a5-643">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-643">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="2d8a5-644">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-644">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="2d8a5-645">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-645">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="2d8a5-646">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-646">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="2d8a5-647">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-647">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="2d8a5-648">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-648">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-649">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-649">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-650">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-650">Removed project reference to Authentication</span></span>
* <span data-ttu-id="2d8a5-651">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-651">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="2d8a5-652">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-652">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-653">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-653">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-654">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-654">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="2d8a5-655">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-655">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-656">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-656">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-657">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-657">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="2d8a5-658">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-658">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="2d8a5-659">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-659">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-660">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-661">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-661">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="2d8a5-662">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="2d8a5-662">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="2d8a5-663">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-663">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="2d8a5-664">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-664">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d8a5-665">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-665">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="2d8a5-666">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-666">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="2d8a5-667">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="2d8a5-667">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="2d8a5-668">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-668">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="2d8a5-669">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="2d8a5-669">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="2d8a5-670">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-670">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="2d8a5-671">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-671">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="2d8a5-672">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="2d8a5-672">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="2d8a5-673">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-673">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="2d8a5-674">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-674">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="2d8a5-675">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-675">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="2d8a5-676">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-676">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="2d8a5-677">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-677">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d8a5-678">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d8a5-678">Az.StorageSync</span></span>
* <span data-ttu-id="2d8a5-679">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="2d8a5-679">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="2d8a5-680">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-680">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="2d8a5-681">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-681">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="2d8a5-682">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-682">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-683">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-683">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-684">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-684">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="2d8a5-685">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-685">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-686">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-686">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-687">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-687">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="2d8a5-688">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-688">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="2d8a5-689">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-689">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="2d8a5-690">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-690">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-691">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-691">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-692">O uso da [API AccessProfile](/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-692">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d8a5-693">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-693">Az.Batch</span></span>
* <span data-ttu-id="2d8a5-694">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-694">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="2d8a5-695">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-695">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-697">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-697">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="2d8a5-698">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-698">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-699">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-700">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-700">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="2d8a5-701">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-701">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="2d8a5-702">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-702">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="2d8a5-703">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-703">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="2d8a5-704">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="2d8a5-704">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-705">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-705">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-706">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-706">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-707">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-707">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-708">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-708">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d8a5-709">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d8a5-709">Az.Functions</span></span>
* <span data-ttu-id="2d8a5-710">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="2d8a5-710">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-711">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-711">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-712">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-712">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d8a5-713">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d8a5-713">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d8a5-714">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-714">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="2d8a5-715">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-715">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-716">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-716">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-717">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-717">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="2d8a5-718">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-718">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-719">Az.Network</span></span>
* <span data-ttu-id="2d8a5-720">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-720">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="2d8a5-721">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-721">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="2d8a5-722">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-722">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="2d8a5-723">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="2d8a5-723">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="2d8a5-724">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="2d8a5-724">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="2d8a5-725">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-725">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="2d8a5-726">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-726">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="2d8a5-727">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-727">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="2d8a5-728">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-728">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="2d8a5-729">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-729">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="2d8a5-730">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-730">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="2d8a5-731">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-731">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="2d8a5-732">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-732">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="2d8a5-733">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-733">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="2d8a5-734">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-734">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="2d8a5-735">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-735">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="2d8a5-736">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-736">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="2d8a5-737">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-737">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="2d8a5-738">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-738">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="2d8a5-739">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-739">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="2d8a5-740">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="2d8a5-740">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="2d8a5-741">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="2d8a5-741">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="2d8a5-742">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="2d8a5-742">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="2d8a5-743">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-743">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="2d8a5-744">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-744">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="2d8a5-745">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="2d8a5-746">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-746">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="2d8a5-747">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-747">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="2d8a5-748">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-748">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-749">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-749">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-750">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-750">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-751">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-751">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-752">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-752">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-753">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-753">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="2d8a5-754">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-754">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="2d8a5-755">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-755">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="2d8a5-756">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-756">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="2d8a5-757">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-757">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="2d8a5-758">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-758">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="2d8a5-759">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-759">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="2d8a5-760">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-760">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="2d8a5-761">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-761">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="2d8a5-762">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-762">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="2d8a5-763">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-763">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d8a5-764">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-764">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d8a5-765">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-765">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="2d8a5-766">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-766">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="2d8a5-767">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-767">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="2d8a5-768">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-768">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-769">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-769">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-770">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-770">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="2d8a5-771">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-771">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="2d8a5-772">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="2d8a5-772">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="2d8a5-773">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-773">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="2d8a5-774">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-774">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-775">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-775">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-776">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-776">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="2d8a5-777">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-777">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-778">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-779">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-779">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="2d8a5-780">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-780">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="2d8a5-781">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-781">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="2d8a5-782">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-782">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="2d8a5-783">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="2d8a5-783">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="2d8a5-784">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="2d8a5-784">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-785">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-785">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-786">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="2d8a5-786">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="2d8a5-787">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-787">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="2d8a5-788">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-788">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-789">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-789">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-790">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="2d8a5-790">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="2d8a5-791">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-791">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="2d8a5-792">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-792">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-793">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-794">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-794">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2d8a5-795">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-795">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="2d8a5-796">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-796">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="2d8a5-797">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-797">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="2d8a5-798">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="2d8a5-798">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="2d8a5-799">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-799">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="2d8a5-800">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-800">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-801">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-801">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-802">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-802">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d8a5-803">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-803">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d8a5-804">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-804">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-805">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-805">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-806">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-806">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="2d8a5-807">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d8a5-807">Az.Billing</span></span>
* <span data-ttu-id="2d8a5-808">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-808">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-809">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-810">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-810">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-811">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-811">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-812">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-812">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="2d8a5-813">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-813">Az.DataShare</span></span>
* <span data-ttu-id="2d8a5-814">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="2d8a5-814">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="2d8a5-815">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="2d8a5-815">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="2d8a5-816">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="2d8a5-816">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-817">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-817">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-818">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-818">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="2d8a5-819">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="2d8a5-819">Added optional parameters to</span></span> 
    - <span data-ttu-id="2d8a5-820">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-820">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="2d8a5-821">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-821">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-822">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-822">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-823">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-823">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2d8a5-824">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d8a5-824">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d8a5-825">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-825">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="2d8a5-826">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="2d8a5-826">Az.PrivateDns</span></span>
* <span data-ttu-id="2d8a5-827">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-827">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-828">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-828">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-829">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-829">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="2d8a5-830">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2d8a5-830">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-831">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-832">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="2d8a5-832">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="2d8a5-833">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="2d8a5-833">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="2d8a5-834">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-834">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="2d8a5-835">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-835">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="2d8a5-836">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-836">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-837">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-837">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-838">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-838">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="2d8a5-839">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-839">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="2d8a5-840">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="2d8a5-840">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-841">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-841">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-842">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-842">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="2d8a5-843">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-843">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="2d8a5-844">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="2d8a5-844">Highlights since the last release</span></span>
* <span data-ttu-id="2d8a5-845">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="2d8a5-845">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="2d8a5-846">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d8a5-846">General availability of Az.Functions</span></span> 
* <span data-ttu-id="2d8a5-847">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="2d8a5-847">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-848">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-849">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-849">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="2d8a5-850">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="2d8a5-850">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-851">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-851">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-852">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="2d8a5-852">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="2d8a5-853">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="2d8a5-853">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="2d8a5-854">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-854">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-855">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-855">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-856">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-856">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="2d8a5-857">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-857">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="2d8a5-858">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-858">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d8a5-859">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-859">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="2d8a5-860">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-860">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d8a5-861">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-861">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="2d8a5-862">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-862">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d8a5-863">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-863">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="2d8a5-864">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-864">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="2d8a5-865">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-865">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="2d8a5-866">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-866">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="2d8a5-867">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-867">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="2d8a5-868">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-868">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="2d8a5-869">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-869">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="2d8a5-870">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-870">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="2d8a5-871">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-871">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2d8a5-872">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-872">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2d8a5-873">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-873">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="2d8a5-874">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-874">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="2d8a5-875">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-875">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d8a5-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-876">Az.Batch</span></span>
* <span data-ttu-id="2d8a5-877">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-877">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="2d8a5-878">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-878">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="2d8a5-879">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-879">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="2d8a5-880">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-880">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="2d8a5-881">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-881">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="2d8a5-882">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-882">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="2d8a5-883">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-883">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="2d8a5-884">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-884">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="2d8a5-885">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-885">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-886">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-887">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-887">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="2d8a5-888">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-888">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="2d8a5-889">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="2d8a5-889">Breaking changes</span></span>
    - <span data-ttu-id="2d8a5-890">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-890">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="2d8a5-891">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-891">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="2d8a5-892">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-892">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="2d8a5-893">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-893">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="2d8a5-894">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-894">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="2d8a5-895">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-895">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="2d8a5-896">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-896">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-897">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-897">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-898">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-898">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-899">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-899">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-900">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="2d8a5-900">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="2d8a5-901">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="2d8a5-901">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="2d8a5-902">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-902">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="2d8a5-903">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="2d8a5-903">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="2d8a5-904">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="2d8a5-904">Az.Functions</span></span>
* <span data-ttu-id="2d8a5-905">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="2d8a5-905">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-906">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-906">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-907">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-907">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d8a5-908">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d8a5-908">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d8a5-909">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-909">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-910">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-910">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-911">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-911">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="2d8a5-912">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-912">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="2d8a5-913">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-913">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="2d8a5-914">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-914">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="2d8a5-915">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-915">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="2d8a5-916">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-916">New cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-917">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-917">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="2d8a5-918">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-918">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="2d8a5-919">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-919">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="2d8a5-920">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-920">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="2d8a5-921">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-921">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="2d8a5-922">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-922">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-923">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-923">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-924">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-924">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="2d8a5-925">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="2d8a5-925">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="2d8a5-926">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="2d8a5-926">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="2d8a5-927">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-927">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="2d8a5-928">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="2d8a5-928">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="2d8a5-929">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-929">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="2d8a5-930">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-930">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-931">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-931">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-932">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-932">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="2d8a5-933">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-933">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="2d8a5-934">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-934">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="2d8a5-935">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="2d8a5-935">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="2d8a5-936">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-936">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="2d8a5-937">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-937">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="2d8a5-938">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-938">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-939">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-939">Az.Network</span></span>
* <span data-ttu-id="2d8a5-940">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-940">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="2d8a5-941">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-941">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="2d8a5-942">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-942">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="2d8a5-943">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-943">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="2d8a5-944">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d8a5-944">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="2d8a5-945">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-945">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-946">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d8a5-946">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="2d8a5-947">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d8a5-947">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="2d8a5-948">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d8a5-948">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="2d8a5-949">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="2d8a5-949">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="2d8a5-950">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-950">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="2d8a5-951">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-951">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="2d8a5-952">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-952">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="2d8a5-953">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-953">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="2d8a5-954">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-954">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="2d8a5-955">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-955">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="2d8a5-956">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-956">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="2d8a5-957">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-957">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="2d8a5-958">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-958">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="2d8a5-959">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-959">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="2d8a5-960">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-960">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="2d8a5-961">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-961">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="2d8a5-962">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-962">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="2d8a5-963">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-964">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="2d8a5-964">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-965">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-965">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-966">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-966">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="2d8a5-967">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-967">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="2d8a5-968">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="2d8a5-968">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="2d8a5-969">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="2d8a5-969">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="2d8a5-970">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="2d8a5-970">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="2d8a5-971">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-971">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="2d8a5-972">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-972">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="2d8a5-973">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-973">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-974">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-974">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-975">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-975">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="2d8a5-976">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-976">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="2d8a5-977">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-977">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="2d8a5-978">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-978">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="2d8a5-979">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-979">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-980">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-981">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="2d8a5-981">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="2d8a5-982">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-982">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="2d8a5-983">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-983">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="2d8a5-984">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-984">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="2d8a5-985">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-985">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="2d8a5-986">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-986">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="2d8a5-987">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-987">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="2d8a5-988">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-988">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="2d8a5-989">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-989">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="2d8a5-990">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-990">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="2d8a5-991">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-991">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="2d8a5-992">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-992">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="2d8a5-993">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-993">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="2d8a5-994">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="2d8a5-994">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="2d8a5-995">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="2d8a5-995">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="2d8a5-996">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="2d8a5-996">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="2d8a5-997">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-997">'New-AzDeployment'</span></span>
    - <span data-ttu-id="2d8a5-998">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-998">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="2d8a5-999">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-999">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2d8a5-1000">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1000">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-1001">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1001">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-1002">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1002">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1003">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1003">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1004">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1004">Enhance performance of:</span></span>
    - <span data-ttu-id="2d8a5-1005">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1005">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d8a5-1006">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1006">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d8a5-1007">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1007">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d8a5-1008">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1008">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="2d8a5-1009">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1009">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="2d8a5-1010">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1010">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="2d8a5-1011">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1011">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="2d8a5-1012">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1012">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="2d8a5-1013">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1013">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="2d8a5-1014">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1014">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1015">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1015">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1016">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1016">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="2d8a5-1017">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1017">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="2d8a5-1018">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1018">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d8a5-1019">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1019">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="2d8a5-1020">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1020">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="2d8a5-1021">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1021">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="2d8a5-1022">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1022">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="2d8a5-1023">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1023">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="2d8a5-1024">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1024">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="2d8a5-1025">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1025">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="2d8a5-1026">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1026">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="2d8a5-1027">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1027">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="2d8a5-1028">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1028">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="2d8a5-1029">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1029">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="2d8a5-1030">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1030">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="2d8a5-1031">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1031">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d8a5-1032">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1032">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="2d8a5-1033">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1033">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="2d8a5-1034">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1034">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2d8a5-1035">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1035">Supported failover Storage account</span></span>
    - <span data-ttu-id="2d8a5-1036">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1036">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="2d8a5-1037">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1037">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="2d8a5-1038">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1038">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="2d8a5-1039">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1039">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="2d8a5-1040">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1040">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="2d8a5-1041">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1041">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="2d8a5-1042">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1042">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="2d8a5-1043">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1043">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="2d8a5-1044">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1044">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="2d8a5-1045">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1045">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="2d8a5-1046">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1046">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="2d8a5-1047">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1047">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="2d8a5-1048">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1048">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="2d8a5-1049">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1049">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="2d8a5-1050">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1050">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="2d8a5-1051">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1051">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="2d8a5-1052">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1052">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="2d8a5-1053">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1053">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="2d8a5-1054">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1054">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2d8a5-1055">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1055">Az.TrafficManager</span></span>
* <span data-ttu-id="2d8a5-1056">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1056">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-1057">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1057">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-1058">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1058">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="2d8a5-1059">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1059">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="2d8a5-1060">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1060">Highlights since the last release</span></span>
* <span data-ttu-id="2d8a5-1061">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1061">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1062">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1062">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1063">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1063">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-1064">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1064">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-1065">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1065">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="2d8a5-1066">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1066">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-1067">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1067">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-1068">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1068">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-1069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1069">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-1070">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1070">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1071">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1072">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1072">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-1073">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1073">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-1074">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1074">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-1075">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1075">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1076">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1076">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="2d8a5-1077">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1077">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="2d8a5-1078">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1078">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="2d8a5-1079">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1079">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1080">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1080">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="2d8a5-1081">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1081">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="2d8a5-1082">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1082">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="2d8a5-1083">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1083">New cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1084">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1084">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-1085">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1085">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-1086">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1086">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="2d8a5-1087">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1087">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="2d8a5-1088">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1088">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-1089">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1089">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-1090">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1090">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="2d8a5-1091">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1091">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="2d8a5-1092">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1092">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="2d8a5-1093">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1093">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="2d8a5-1094">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1094">Az.Maintenance</span></span>
* <span data-ttu-id="2d8a5-1095">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1095">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-1096">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1096">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-1097">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1097">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="2d8a5-1098">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1098">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d8a5-1099">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1099">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d8a5-1100">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1100">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d8a5-1101">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1101">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="2d8a5-1102">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1102">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="2d8a5-1103">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1103">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="2d8a5-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1104">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1105">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1106">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1106">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="2d8a5-1107">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1107">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="2d8a5-1108">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1108">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="2d8a5-1109">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1109">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="2d8a5-1110">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1110">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="2d8a5-1111">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1111">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="2d8a5-1112">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1112">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="2d8a5-1113">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1113">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="2d8a5-1114">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1114">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="2d8a5-1115">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1115">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="2d8a5-1116">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1116">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="2d8a5-1117">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1117">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="2d8a5-1118">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1118">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="2d8a5-1119">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1119">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="2d8a5-1120">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1120">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="2d8a5-1121">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1121">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-1122">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1122">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-1123">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1123">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="2d8a5-1124">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1124">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-1125">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1125">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-1126">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1126">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1127">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1127">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1128">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1128">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="2d8a5-1129">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1129">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1130">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1130">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1131">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1131">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="2d8a5-1132">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1132">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="2d8a5-1133">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1133">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="2d8a5-1134">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1134">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="2d8a5-1135">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1135">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="2d8a5-1136">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1136">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d8a5-1137">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1137">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d8a5-1138">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1138">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="2d8a5-1139">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1139">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d8a5-1140">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1140">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="2d8a5-1141">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1141">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="2d8a5-1142">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1142">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="2d8a5-1143">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1143">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="2d8a5-1144">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1144">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="2d8a5-1145">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1145">General</span></span>
* <span data-ttu-id="2d8a5-1146">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1146">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="2d8a5-1147">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1147">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="2d8a5-1148">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1148">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="2d8a5-1149">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1149">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="2d8a5-1150">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1150">Az.Billing</span></span>
  - <span data-ttu-id="2d8a5-1151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1151">Az.Compute</span></span>
  - <span data-ttu-id="2d8a5-1152">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1152">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="2d8a5-1153">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1153">Az.EventHub</span></span>
  - <span data-ttu-id="2d8a5-1154">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1154">Az.IotHub</span></span>
  - <span data-ttu-id="2d8a5-1155">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1155">Az.KeyVault</span></span>
  - <span data-ttu-id="2d8a5-1156">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1156">Az.Monitor</span></span>
  - <span data-ttu-id="2d8a5-1157">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1157">Az.Network</span></span>
  - <span data-ttu-id="2d8a5-1158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1158">Az.Resources</span></span>
  - <span data-ttu-id="2d8a5-1159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1159">Az.Storage</span></span>
  - <span data-ttu-id="2d8a5-1160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1160">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-1161">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1161">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-1162">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1162">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="2d8a5-1163">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1163">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="2d8a5-1164">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1164">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1165">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1165">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1166">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1166">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1167">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1168">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1168">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="2d8a5-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1169">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="2d8a5-1170">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1170">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-1171">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1171">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="2d8a5-1172">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1172">[#11354]</span></span>
* <span data-ttu-id="2d8a5-1173">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1173">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="2d8a5-1174">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1174">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="2d8a5-1175">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1175">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="2d8a5-1176">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1176">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="2d8a5-1177">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1177">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="2d8a5-1178">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1178">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="2d8a5-1179">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1179">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="2d8a5-1180">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1180">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="2d8a5-1181">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1181">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1182">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1183">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1183">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="2d8a5-1184">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1184">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-1185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1185">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-1186">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1186">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="2d8a5-1187">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1187">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1188">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-1189">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1189">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-1190">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1190">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-1191">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1191">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="2d8a5-1192">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1192">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1193">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1193">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="2d8a5-1194">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1194">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-1195">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1195">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-1196">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1196">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-1197">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1197">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-1198">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1198">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1199">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1199">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1200">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1200">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="2d8a5-1201">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1201">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d8a5-1202">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1202">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="2d8a5-1203">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1203">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="2d8a5-1204">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1204">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="2d8a5-1205">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1205">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-1206">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1206">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-1207">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1207">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-1208">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1208">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-1209">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1209">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="2d8a5-1210">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1210">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="2d8a5-1211">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1211">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="2d8a5-1212">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1212">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="2d8a5-1213">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1213">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="2d8a5-1214">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1214">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1215">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1215">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1216">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1216">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="2d8a5-1217">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1217">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="2d8a5-1218">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1218">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="2d8a5-1219">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1219">Added example.</span></span>
* <span data-ttu-id="2d8a5-1220">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1220">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="2d8a5-1221">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1221">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1222">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1223">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1223">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="2d8a5-1224">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1224">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="2d8a5-1225">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1225">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="2d8a5-1226">Az.Support</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1226">Az.Support</span></span>
* <span data-ttu-id="2d8a5-1227">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1227">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-1228">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1228">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-1229">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1229">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="2d8a5-1230">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1230">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="2d8a5-1231">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1231">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="2d8a5-1232">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1232">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="2d8a5-1233">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1233">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="2d8a5-1234">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1234">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1235">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1236">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1236">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="2d8a5-1237">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1237">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="2d8a5-1238">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1238">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-1239">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1239">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-1240">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1240">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="2d8a5-1241">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1241">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="2d8a5-1242">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1242">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="2d8a5-1243">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1243">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-1244">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1244">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-1245">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1245">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-1246">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1246">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-1247">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1247">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2d8a5-1248">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1248">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1249">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1249">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d8a5-1250">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1250">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d8a5-1251">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1251">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d8a5-1252">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1252">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="2d8a5-1253">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1253">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="2d8a5-1254">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1254">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1255">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1255">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d8a5-1256">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1256">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d8a5-1257">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1257">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="2d8a5-1258">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1258">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="2d8a5-1259">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1259">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2d8a5-1260">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1260">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2d8a5-1261">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1261">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="2d8a5-1262">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1262">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1263">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1263">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="2d8a5-1264">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1264">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="2d8a5-1265">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1265">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-1266">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1266">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-1267">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1267">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1268">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1269">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1269">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="2d8a5-1270">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1270">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="2d8a5-1271">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1271">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="2d8a5-1272">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1272">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1273">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1274">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1274">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="2d8a5-1275">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1275">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="2d8a5-1276">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1276">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="2d8a5-1277">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1277">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="2d8a5-1278">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1278">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="2d8a5-1279">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1279">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="2d8a5-1280">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1280">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="2d8a5-1281">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1281">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="2d8a5-1282">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1282">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2d8a5-1283">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1283">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2d8a5-1284">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1284">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="2d8a5-1285">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1285">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="2d8a5-1286">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1286">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="2d8a5-1287">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1287">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1288">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1288">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1289">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1289">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="2d8a5-1290">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1290">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="2d8a5-1291">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1291">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="2d8a5-1292">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1292">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="2d8a5-1293">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1293">Remove an LTR backup</span></span>
    - <span data-ttu-id="2d8a5-1294">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1294">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="2d8a5-1295">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1295">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="2d8a5-1296">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1296">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="2d8a5-1297">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1297">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1298">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1299">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1299">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="2d8a5-1300">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1300">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="2d8a5-1301">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1301">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="2d8a5-1302">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1302">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="2d8a5-1303">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1303">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-1304">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1304">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-1305">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1305">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="2d8a5-1306">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1306">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="2d8a5-1307">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1307">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="2d8a5-1308">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1308">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="2d8a5-1309">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1309">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="2d8a5-1310">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1310">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d8a5-1311">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1311">Highlights since the last major release</span></span>
* <span data-ttu-id="2d8a5-1312">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1312">Updated client side telemetry.</span></span>
* <span data-ttu-id="2d8a5-1313">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1313">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="2d8a5-1314">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1314">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1315">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1315">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1316">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1316">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-1317">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1317">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-1318">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1318">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-1319">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1319">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-1320">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1320">Updated SDK to 7.0</span></span>
* <span data-ttu-id="2d8a5-1321">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1321">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1322">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1322">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1323">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1323">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-1324">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1324">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-1325">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1325">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-1326">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1326">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-1327">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1327">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2d8a5-1328">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1328">New Cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1329">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1329">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d8a5-1330">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1330">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d8a5-1331">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1331">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2d8a5-1332">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1332">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-1333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1333">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-1334">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1334">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-1335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1335">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-1336">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1336">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="2d8a5-1337">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1337">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="2d8a5-1338">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1338">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1339">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1339">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1340">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1340">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-1341">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1341">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2d8a5-1342">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1342">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2d8a5-1343">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1343">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="2d8a5-1344">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1344">No new cmdlets are added.</span></span> <span data-ttu-id="2d8a5-1345">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1345">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-1346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1346">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-1347">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1347">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1348">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1348">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1349">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1349">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="2d8a5-1350">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1350">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="2d8a5-1351">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1351">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="2d8a5-1352">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1352">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="2d8a5-1353">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1353">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="2d8a5-1354">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1354">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="2d8a5-1355">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1355">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="2d8a5-1356">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1356">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1357">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1358">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1358">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="2d8a5-1359">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1359">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="2d8a5-1360">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1360">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2d8a5-1361">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1361">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2d8a5-1362">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1362">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d8a5-1363">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1363">Az.StorageSync</span></span>
* <span data-ttu-id="2d8a5-1364">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1364">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="2d8a5-1365">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1365">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d8a5-1366">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1366">Highlights since the last major release</span></span>
* <span data-ttu-id="2d8a5-1367">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1367">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="2d8a5-1368">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1368">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1369">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1370">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1370">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="2d8a5-1371">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1371">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-1373">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1373">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="2d8a5-1374">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1374">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="2d8a5-1375">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1375">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="2d8a5-1376">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1376">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1377">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1377">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1378">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1378">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="2d8a5-1379">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1379">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="2d8a5-1380">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1380">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="2d8a5-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1381">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="2d8a5-1382">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1382">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1383">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1383">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1384">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1384">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2d8a5-1385">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1385">Az.DeploymentManager</span></span>
* <span data-ttu-id="2d8a5-1386">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1386">Adds LIST operations for resources</span></span>
* <span data-ttu-id="2d8a5-1387">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1387">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-1388">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1388">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-1389">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1389">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-1390">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1390">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-1391">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1391">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1392">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1392">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1393">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1393">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="2d8a5-1394">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1394">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="2d8a5-1395">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1395">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-1396">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1396">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="2d8a5-1397">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1397">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="2d8a5-1398">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1398">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="2d8a5-1399">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1399">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="2d8a5-1400">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1400">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="2d8a5-1401">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1401">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1402">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="2d8a5-1403">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1403">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="2d8a5-1404">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1404">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="2d8a5-1405">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1405">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-1406">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1406">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-1407">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1407">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="2d8a5-1408">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1408">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="2d8a5-1409">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1409">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="2d8a5-1410">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1410">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-1411">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1411">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-1412">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1412">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="2d8a5-1413">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1413">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1414">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1414">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1415">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1415">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="2d8a5-1416">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1416">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1417">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1417">Az.Sql</span></span>
<span data-ttu-id="2d8a5-1418">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1418">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1419">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1419">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1420">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1420">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="2d8a5-1421">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1421">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d8a5-1422">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1422">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="2d8a5-1423">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1423">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-1424">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1424">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-1425">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1425">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="2d8a5-1426">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1426">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="2d8a5-1427">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1427">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1428">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1428">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1429">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1429">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-1430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1430">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-1431">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1431">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1432">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1433">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1433">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2d8a5-1434">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1434">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d8a5-1435">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1435">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2d8a5-1436">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1436">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2d8a5-1437">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1437">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d8a5-1438">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1438">Get the Edge Storage Container</span></span>
* <span data-ttu-id="2d8a5-1439">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1439">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d8a5-1440">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1440">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="2d8a5-1441">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1441">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d8a5-1442">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1442">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="2d8a5-1443">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1443">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2d8a5-1444">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1444">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="2d8a5-1445">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1445">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d8a5-1446">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1446">Get the Edge Storage Account</span></span>
* <span data-ttu-id="2d8a5-1447">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1447">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d8a5-1448">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1448">Create new Edge Storage Account</span></span>
* <span data-ttu-id="2d8a5-1449">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1449">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2d8a5-1450">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1450">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="2d8a5-1451">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1451">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="2d8a5-1452">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1452">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="2d8a5-1453">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1453">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="2d8a5-1454">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1454">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1455">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1456">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1456">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="2d8a5-1457">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1457">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="2d8a5-1458">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1458">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="2d8a5-1459">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1459">Az.DevTestLabs</span></span>
* <span data-ttu-id="2d8a5-1460">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1460">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-1461">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1461">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-1462">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1462">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-1463">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1463">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-1464">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1464">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2d8a5-1465">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1465">Az.MachineLearning</span></span>
* <span data-ttu-id="2d8a5-1466">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1466">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="2d8a5-1467">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1467">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d8a5-1468">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1468">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="2d8a5-1469">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1469">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d8a5-1470">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1470">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d8a5-1471">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1471">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="2d8a5-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1472">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="2d8a5-1473">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1473">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1474">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1474">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1475">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1475">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-1476">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1476">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-1477">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1477">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="2d8a5-1478">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1478">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2d8a5-1479">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2d8a5-1480">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1480">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1481">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1482">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1482">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1483">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1484">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1484">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="2d8a5-1485">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1485">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2d8a5-1486">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1486">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2d8a5-1487">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1487">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1488">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1488">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1489">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1489">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="2d8a5-1490">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1490">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="2d8a5-1491">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1491">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="2d8a5-1492">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1492">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="2d8a5-1493">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1493">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="2d8a5-1494">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1494">General</span></span>
* <span data-ttu-id="2d8a5-1495">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1495">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1496">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1496">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1497">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1497">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="2d8a5-1498">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1498">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d8a5-1499">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1499">Az.Batch</span></span>
* <span data-ttu-id="2d8a5-1500">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1500">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1501">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1501">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1502">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1502">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-1503">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1503">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-1504">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1504">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="2d8a5-1505">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1505">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d8a5-1506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1506">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d8a5-1507">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1507">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-1508">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1508">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-1509">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1509">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="2d8a5-1510">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1510">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="2d8a5-1511">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1511">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-1512">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1512">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-1513">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1513">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="2d8a5-1514">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1514">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="2d8a5-1515">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1515">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1516">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1516">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1517">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1517">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1518">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1519">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1519">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="2d8a5-1520">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1520">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1521">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1522">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1522">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1523">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1523">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1524">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1524">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="2d8a5-1525">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1525">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="2d8a5-1526">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1526">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="2d8a5-1527">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1527">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="2d8a5-1528">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1528">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="2d8a5-1529">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1529">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="2d8a5-1530">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1530">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="2d8a5-1531">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1531">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="2d8a5-1532">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1532">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="2d8a5-1533">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1533">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="2d8a5-1534">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1534">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="2d8a5-1535">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1535">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="2d8a5-1536">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1536">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="2d8a5-1537">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1537">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d8a5-1538">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1538">Highlights since the last major release</span></span>
* <span data-ttu-id="2d8a5-1539">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1539">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="2d8a5-1540">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1540">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1541">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1542">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1542">VM Reapply feature</span></span>
    - <span data-ttu-id="2d8a5-1543">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1543">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="2d8a5-1544">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1544">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="2d8a5-1545">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1545">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="2d8a5-1546">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1546">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="2d8a5-1547">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1547">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d8a5-1548">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1548">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="2d8a5-1549">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1549">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="2d8a5-1550">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1550">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="2d8a5-1551">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1551">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="2d8a5-1552">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1552">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2d8a5-1553">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1553">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2d8a5-1554">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1554">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d8a5-1555">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1555">Get the Order</span></span>
* <span data-ttu-id="2d8a5-1556">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1556">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d8a5-1557">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1557">Create new Order</span></span>
* <span data-ttu-id="2d8a5-1558">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1558">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2d8a5-1559">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1559">Remove the Order</span></span>
* <span data-ttu-id="2d8a5-1560">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1560">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="2d8a5-1561">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1561">Now creates Local Share</span></span>
* <span data-ttu-id="2d8a5-1562">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1562">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="2d8a5-1563">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1563">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="2d8a5-1564">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1564">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="2d8a5-1565">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1565">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="2d8a5-1566">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1566">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d8a5-1567">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1567">Gets the information about Triggers</span></span>
* <span data-ttu-id="2d8a5-1568">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1568">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d8a5-1569">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1569">Create new Triggers</span></span>
* <span data-ttu-id="2d8a5-1570">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1570">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2d8a5-1571">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1571">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1572">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1572">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1573">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1573">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="2d8a5-1574">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1574">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-1575">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1575">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-1576">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1576">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-1577">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1577">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-1578">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1578">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-1579">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1579">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-1580">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1580">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="2d8a5-1581">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1581">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="2d8a5-1582">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1582">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="2d8a5-1583">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1583">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1584">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1584">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1585">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1585">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="2d8a5-1586">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1586">Az.PrivateDns</span></span>
* <span data-ttu-id="2d8a5-1587">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1587">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-1588">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1588">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-1589">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1589">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="2d8a5-1590">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1590">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="2d8a5-1591">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1591">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d8a5-1592">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1592">Az.RedisCache</span></span>
* <span data-ttu-id="2d8a5-1593">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1593">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="2d8a5-1594">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1594">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="2d8a5-1595">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1595">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1596">Az.Resources</span></span>
- <span data-ttu-id="2d8a5-1597">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1597">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="2d8a5-1598">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1598">Updated create policy definition help example</span></span>
- <span data-ttu-id="2d8a5-1599">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1599">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="2d8a5-1600">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1600">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="2d8a5-1601">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1601">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1602">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1603">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1603">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="2d8a5-1604">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1604">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="2d8a5-1605">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1605">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="2d8a5-1606">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1606">General</span></span>
* <span data-ttu-id="2d8a5-1607">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1607">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1608">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1609">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1609">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2d8a5-1610">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1610">Az.Advisor</span></span>
* <span data-ttu-id="2d8a5-1611">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1611">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d8a5-1612">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1612">Az.Batch</span></span>
* <span data-ttu-id="2d8a5-1613">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1613">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="2d8a5-1614">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1614">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="2d8a5-1615">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1615">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="2d8a5-1616">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1616">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="2d8a5-1617">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1617">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="2d8a5-1618">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1618">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="2d8a5-1619">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1619">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="2d8a5-1620">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1620">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="2d8a5-1621">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1621">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="2d8a5-1622">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1622">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2d8a5-1623">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1623">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="2d8a5-1624">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1624">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="2d8a5-1625">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1625">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2d8a5-1626">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1626">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="2d8a5-1627">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1627">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="2d8a5-1628">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1628">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="2d8a5-1629">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1629">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="2d8a5-1630">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1630">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="2d8a5-1631">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1631">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="2d8a5-1632">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1632">This operation is no longer supported.</span></span>
* <span data-ttu-id="2d8a5-1633">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1633">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2d8a5-1634">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1634">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2d8a5-1635">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1635">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="2d8a5-1636">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1636">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="2d8a5-1637">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1637">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="2d8a5-1638">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1638">New non-verified images are also now returned.</span></span> <span data-ttu-id="2d8a5-1639">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1639">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="2d8a5-1640">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1640">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="2d8a5-1641">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1641">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="2d8a5-1642">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1642">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="2d8a5-1643">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1643">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="2d8a5-1644">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1644">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="2d8a5-1645">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1645">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="2d8a5-1646">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1646">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="2d8a5-1647">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1647">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="2d8a5-1648">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1648">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-1649">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1649">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-1650">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1650">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="2d8a5-1651">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1651">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1652">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1652">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1653">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1653">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="2d8a5-1654">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1654">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="2d8a5-1655">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1655">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="2d8a5-1656">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1656">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d8a5-1657">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1657">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="2d8a5-1658">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1658">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="2d8a5-1659">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1659">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d8a5-1660">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1660">Breaking changes</span></span>
    - <span data-ttu-id="2d8a5-1661">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1661">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="2d8a5-1662">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1662">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1663">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1663">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1664">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1664">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-1665">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1665">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-1666">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1666">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="2d8a5-1667">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1667">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="2d8a5-1668">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1668">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="2d8a5-1669">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1669">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="2d8a5-1670">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1670">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="2d8a5-1671">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1671">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-1672">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1672">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-1673">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1673">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-1674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1674">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-1675">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1675">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="2d8a5-1676">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1676">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="2d8a5-1677">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1677">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="2d8a5-1678">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1678">Removed five cmdlets:</span></span>
    - <span data-ttu-id="2d8a5-1679">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1679">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d8a5-1680">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1680">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d8a5-1681">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1681">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2d8a5-1682">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1682">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="2d8a5-1683">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1683">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="2d8a5-1684">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1684">Added three cmdlets:</span></span>
    - <span data-ttu-id="2d8a5-1685">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1685">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2d8a5-1686">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1686">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2d8a5-1687">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1687">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="2d8a5-1688">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1688">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="2d8a5-1689">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1689">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="2d8a5-1690">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1690">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="2d8a5-1691">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1691">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="2d8a5-1692">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1692">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="2d8a5-1693">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1693">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="2d8a5-1694">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1694">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="2d8a5-1695">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1695">Added some scenario test cases.</span></span>
* <span data-ttu-id="2d8a5-1696">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1696">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-1697">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1697">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-1698">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1698">Breaking changes:</span></span>
    - <span data-ttu-id="2d8a5-1699">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1699">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d8a5-1700">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1700">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d8a5-1701">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1701">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d8a5-1702">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1702">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d8a5-1703">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1703">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="2d8a5-1704">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="2d8a5-1705">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1705">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="2d8a5-1706">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1706">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="2d8a5-1707">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1707">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d8a5-1708">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1708">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2d8a5-1709">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1709">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2d8a5-1710">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1710">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-1711">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1711">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-1712">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1712">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="2d8a5-1713">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1713">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="2d8a5-1714">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1714">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="2d8a5-1715">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1715">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="2d8a5-1716">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1716">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="2d8a5-1717">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1717">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="2d8a5-1718">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1718">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="2d8a5-1719">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1719">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="2d8a5-1720">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1720">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1721">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1721">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1722">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1722">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1723">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1723">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1724">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1724">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="2d8a5-1725">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1725">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-1726">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1726">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-1727">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1727">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-1728">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1728">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-1729">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1729">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-1730">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1730">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2d8a5-1731">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1731">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="2d8a5-1732">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1732">New cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-1733">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1733">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="2d8a5-1734">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1734">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="2d8a5-1735">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1735">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="2d8a5-1736">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1736">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="2d8a5-1737">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1737">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="2d8a5-1738">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1738">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="2d8a5-1739">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1739">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="2d8a5-1740">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1740">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="2d8a5-1741">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1741">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-1742">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1742">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="2d8a5-1743">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1743">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d8a5-1744">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1744">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d8a5-1745">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1745">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2d8a5-1746">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1746">Set-AzVirtualHub</span></span>
* <span data-ttu-id="2d8a5-1747">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1747">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="2d8a5-1748">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1748">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d8a5-1749">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1749">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2d8a5-1750">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1750">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2d8a5-1751">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1751">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="2d8a5-1752">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1752">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="2d8a5-1753">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1753">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="2d8a5-1754">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1754">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-1755">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1755">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="2d8a5-1756">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1756">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d8a5-1757">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1757">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d8a5-1758">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1758">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d8a5-1759">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1759">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d8a5-1760">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1760">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2d8a5-1761">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1761">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="2d8a5-1762">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1762">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="2d8a5-1763">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1763">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-1764">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1764">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="2d8a5-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1765">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="2d8a5-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1766">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="2d8a5-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="2d8a5-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1768">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="2d8a5-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1769">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="2d8a5-1770">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1770">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d8a5-1771">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1771">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="2d8a5-1772">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1772">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="2d8a5-1773">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1773">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="2d8a5-1774">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1774">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="2d8a5-1775">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1775">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2d8a5-1776">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1776">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="2d8a5-1777">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1777">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="2d8a5-1778">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1778">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="2d8a5-1779">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1779">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="2d8a5-1780">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1780">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="2d8a5-1781">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1781">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-1782">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1782">New-AzIpGroup</span></span>
        - <span data-ttu-id="2d8a5-1783">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1783">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="2d8a5-1784">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1784">Get-AzIpGroup</span></span>
        - <span data-ttu-id="2d8a5-1785">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1785">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-1786">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1786">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-1787">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1787">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1788">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1788">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1789">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1789">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="2d8a5-1790">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1790">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="2d8a5-1791">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1791">Removed deprecated aliases:</span></span>
* <span data-ttu-id="2d8a5-1792">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1792">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="2d8a5-1793">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1793">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="2d8a5-1794">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1794">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2d8a5-1795">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1795">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="2d8a5-1796">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1796">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="2d8a5-1797">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1797">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1798">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1798">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1799">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1799">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="2d8a5-1800">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1800">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2d8a5-1801">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1801">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2d8a5-1802">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1802">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="2d8a5-1803">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1803">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="2d8a5-1804">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1804">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="2d8a5-1805">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1805">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="2d8a5-1806">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1806">General</span></span>
* <span data-ttu-id="2d8a5-1807">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1807">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1808">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1808">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1809">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1809">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-1810">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1810">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-1811">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1811">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="2d8a5-1812">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1812">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-1813">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1813">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-1814">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1814">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d8a5-1815">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1815">Az.Batch</span></span>
* <span data-ttu-id="2d8a5-1816">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1816">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1817">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1818">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1818">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2d8a5-1819">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1819">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="2d8a5-1820">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1820">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="2d8a5-1821">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1821">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1822">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1822">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1823">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1823">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="2d8a5-1824">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1824">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="2d8a5-1825">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1825">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-1826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1826">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-1827">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1827">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2d8a5-1828">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1828">Az.HealthcareApis</span></span>
* <span data-ttu-id="2d8a5-1829">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1829">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="2d8a5-1830">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1830">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="2d8a5-1831">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1831">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="2d8a5-1832">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1832">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-1833">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1833">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-1834">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1834">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="2d8a5-1835">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1835">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-1836">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1836">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-1837">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1837">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="2d8a5-1838">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1838">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="2d8a5-1839">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1839">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="2d8a5-1840">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1840">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1841">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1841">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1842">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1842">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="2d8a5-1843">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1843">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="2d8a5-1844">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1844">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-1845">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1845">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="2d8a5-1846">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1846">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d8a5-1847">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1847">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="2d8a5-1848">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1848">Updated cmdlets:</span></span>
        - <span data-ttu-id="2d8a5-1849">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1849">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d8a5-1850">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1850">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d8a5-1851">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1851">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2d8a5-1852">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1852">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="2d8a5-1853">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1853">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="2d8a5-1854">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1854">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="2d8a5-1855">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1855">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d8a5-1856">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1856">Az.RedisCache</span></span>
* <span data-ttu-id="2d8a5-1857">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1857">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1858">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1858">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1859">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1859">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1860">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1860">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1861">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1861">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="2d8a5-1862">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1862">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2d8a5-1863">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1863">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="2d8a5-1864">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1864">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2d8a5-1865">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1865">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d8a5-1866">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1866">Az.StorageSync</span></span>
* <span data-ttu-id="2d8a5-1867">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1867">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-1868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1868">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-1869">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1869">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="2d8a5-1870">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1870">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-1871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1871">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-1872">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1872">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="2d8a5-1873">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1873">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="2d8a5-1874">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1874">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-1875">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1875">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-1876">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1876">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="2d8a5-1877">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1877">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="2d8a5-1878">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1878">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1879">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-1880">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1880">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="2d8a5-1881">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1881">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d8a5-1882">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1882">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="2d8a5-1883">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1883">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="2d8a5-1884">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1884">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="2d8a5-1885">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1885">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="2d8a5-1886">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1886">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="2d8a5-1887">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1887">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="2d8a5-1888">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1888">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-1889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1889">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-1890">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1890">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="2d8a5-1891">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1891">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-1892">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1892">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-1893">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1893">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-1894">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1894">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-1895">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1895">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="2d8a5-1896">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1896">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="2d8a5-1897">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1897">New cmdlets are:</span></span>
    - <span data-ttu-id="2d8a5-1898">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1898">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d8a5-1899">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1899">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d8a5-1900">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1900">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2d8a5-1901">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1901">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-1902">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1902">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-1903">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1903">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="2d8a5-1904">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1904">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="2d8a5-1905">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1905">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="2d8a5-1906">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1906">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="2d8a5-1907">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1907">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="2d8a5-1908">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1908">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="2d8a5-1909">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1909">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="2d8a5-1910">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1910">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="2d8a5-1911">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1911">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2d8a5-1912">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1912">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="2d8a5-1913">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1913">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2d8a5-1914">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1914">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="2d8a5-1915">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1915">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="2d8a5-1916">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1916">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="2d8a5-1917">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1917">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="2d8a5-1918">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1918">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="2d8a5-1919">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1919">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="2d8a5-1920">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1920">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="2d8a5-1921">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1921">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="2d8a5-1922">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1922">Overall improved help files</span></span>
* <span data-ttu-id="2d8a5-1923">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1923">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-1924">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1924">Az.Network</span></span>
* <span data-ttu-id="2d8a5-1925">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1925">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="2d8a5-1926">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1926">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="2d8a5-1927">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1927">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="2d8a5-1928">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1928">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="2d8a5-1929">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1929">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="2d8a5-1930">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1930">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="2d8a5-1931">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1931">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="2d8a5-1932">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1932">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="2d8a5-1933">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1933">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="2d8a5-1934">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1934">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="2d8a5-1935">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1935">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="2d8a5-1936">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1936">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="2d8a5-1937">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1937">New cmdlets</span></span>
        - <span data-ttu-id="2d8a5-1938">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1938">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="2d8a5-1939">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1939">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="2d8a5-1940">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1940">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-1941">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1941">New-VpnSite</span></span>
        - <span data-ttu-id="2d8a5-1942">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1942">Update-VpnSite</span></span>
        - <span data-ttu-id="2d8a5-1943">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1943">New-VpnConnection</span></span>
        - <span data-ttu-id="2d8a5-1944">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1944">Update-VpnConnection</span></span>
* <span data-ttu-id="2d8a5-1945">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1945">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-1946">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1946">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-1947">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1947">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="2d8a5-1948">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1948">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-1949">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1949">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-1950">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1950">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-1951">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1951">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-1952">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1952">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="2d8a5-1953">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1953">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="2d8a5-1954">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1954">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d8a5-1955">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1955">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d8a5-1956">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1956">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d8a5-1957">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1957">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="2d8a5-1958">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1958">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d8a5-1959">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1959">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d8a5-1960">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1960">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d8a5-1961">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1961">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d8a5-1962">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1962">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="2d8a5-1963">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1963">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2d8a5-1964">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1964">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2d8a5-1965">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1965">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2d8a5-1966">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1966">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="2d8a5-1967">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1967">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d8a5-1968">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1968">Az.SignalR</span></span>
* <span data-ttu-id="2d8a5-1969">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1969">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-1970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1970">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-1971">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1971">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="2d8a5-1972">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1972">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="2d8a5-1973">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1973">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2d8a5-1974">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1974">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="2d8a5-1975">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1975">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1976">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-1977">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1977">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2d8a5-1978">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1978">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="2d8a5-1979">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1979">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="2d8a5-1980">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1980">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="2d8a5-1981">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1981">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="2d8a5-1982">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1982">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="2d8a5-1983">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1983">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="2d8a5-1984">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1984">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d8a5-1985">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1985">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d8a5-1986">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1986">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2d8a5-1987">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1987">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-1988">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1988">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-1989">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1989">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="2d8a5-1990">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1990">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="2d8a5-1991">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1991">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="2d8a5-1992">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1992">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="2d8a5-1993">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1993">General</span></span>
* <span data-ttu-id="2d8a5-1994">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1994">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-1995">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1995">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-1996">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1996">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-1997">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1997">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-1998">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1998">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="2d8a5-1999">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="2d8a5-1999">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-2000">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2000">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-2001">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2001">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="2d8a5-2002">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2002">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="2d8a5-2003">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2003">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="2d8a5-2004">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2004">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="2d8a5-2005">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2005">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d8a5-2006">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2006">Az.Batch</span></span>
* <span data-ttu-id="2d8a5-2007">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2007">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-2008">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2008">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-2009">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2009">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2010">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2011">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2011">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="2d8a5-2012">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2012">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="2d8a5-2013">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2013">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="2d8a5-2014">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2014">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="2d8a5-2015">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2015">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="2d8a5-2016">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2016">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="2d8a5-2017">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2017">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="2d8a5-2018">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2018">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-2019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2019">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-2020">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2020">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="2d8a5-2021">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2021">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="2d8a5-2022">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2022">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="2d8a5-2023">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2023">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-2024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2024">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-2025">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2025">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-2026">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2026">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-2027">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2027">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="2d8a5-2028">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2028">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="2d8a5-2029">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2029">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="2d8a5-2030">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2030">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="2d8a5-2031">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2031">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d8a5-2032">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2032">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-2033">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2033">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-2034">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2034">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2035">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2035">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2036">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2036">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="2d8a5-2037">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2037">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="2d8a5-2038">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2038">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="2d8a5-2039">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2039">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="2d8a5-2040">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2040">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="2d8a5-2041">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2041">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="2d8a5-2042">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2042">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2043">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-2044">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2044">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="2d8a5-2045">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2045">Added example</span></span>
    - <span data-ttu-id="2d8a5-2046">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2046">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="2d8a5-2047">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2047">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="2d8a5-2048">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2048">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2049">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2050">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2050">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2051">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2051">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2052">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2052">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="2d8a5-2053">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2053">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="2d8a5-2054">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2054">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="2d8a5-2055">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2055">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d8a5-2056">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2056">Az.ServiceBus</span></span>
* <span data-ttu-id="2d8a5-2057">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2057">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="2d8a5-2058">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2058">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="2d8a5-2059">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2059">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-2060">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2060">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-2061">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2061">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="2d8a5-2062">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2062">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="2d8a5-2063">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2063">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="2d8a5-2064">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2064">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="2d8a5-2065">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2065">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="2d8a5-2066">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2066">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2067">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2067">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2068">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2068">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2069">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2069">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2070">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2070">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="2d8a5-2071">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2071">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="2d8a5-2072">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2072">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="2d8a5-2073">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2073">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="2d8a5-2074">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2074">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="2d8a5-2075">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2075">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2076">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2076">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2077">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2077">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="2d8a5-2078">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2078">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2079">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2080">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2080">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2d8a5-2081">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2081">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2d8a5-2082">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2082">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2083">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2083">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2084">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2084">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-2085">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2085">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-2086">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2086">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2087">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2087">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2088">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2088">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d8a5-2089">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2089">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d8a5-2090">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2090">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="2d8a5-2091">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2091">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-2092">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2092">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-2093">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2093">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="2d8a5-2094">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2094">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-2095">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2095">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-2096">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2096">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2d8a5-2097">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2097">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-2098">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2098">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-2099">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2099">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d8a5-2100">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2100">Az.LogicApp</span></span>
* <span data-ttu-id="2d8a5-2101">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2101">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="2d8a5-2102">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2102">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2d8a5-2103">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2103">Az.ManagedServices</span></span>
* <span data-ttu-id="2d8a5-2104">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2104">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2105">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2105">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2106">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2106">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="2d8a5-2107">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2107">New cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2108">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2108">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d8a5-2109">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2109">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d8a5-2110">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2110">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-2111">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2111">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-2112">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2112">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-2113">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2113">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2d8a5-2114">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2114">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="2d8a5-2115">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2115">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="2d8a5-2116">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2116">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="2d8a5-2117">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2117">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="2d8a5-2118">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2118">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="2d8a5-2119">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2119">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="2d8a5-2120">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2120">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="2d8a5-2121">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2121">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="2d8a5-2122">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2122">Updated cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2123">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2123">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d8a5-2124">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2124">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2d8a5-2125">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2125">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2d8a5-2126">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2126">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d8a5-2127">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2127">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="2d8a5-2128">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2128">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-2129">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2129">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2d8a5-2130">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2130">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2d8a5-2131">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2131">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="2d8a5-2132">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2132">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="2d8a5-2133">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2133">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="2d8a5-2134">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2134">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-2135">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2135">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-2136">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2136">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="2d8a5-2137">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2137">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2138">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2138">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2139">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2139">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2d8a5-2140">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2140">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="2d8a5-2141">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2141">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="2d8a5-2142">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2142">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2d8a5-2143">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2143">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="2d8a5-2144">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2144">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2d8a5-2145">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2145">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="2d8a5-2146">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2146">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2d8a5-2147">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2147">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="2d8a5-2148">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2148">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2149">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2149">Az.Resources</span></span>
- <span data-ttu-id="2d8a5-2150">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2150">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="2d8a5-2151">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2151">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d8a5-2152">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2152">Az.ServiceBus</span></span>
* <span data-ttu-id="2d8a5-2153">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2153">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2d8a5-2154">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2154">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2155">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2156">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2156">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="2d8a5-2157">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2157">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="2d8a5-2158">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2158">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2159">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2159">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2160">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2160">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d8a5-2161">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2161">Az.StorageSync</span></span>
* <span data-ttu-id="2d8a5-2162">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2162">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="2d8a5-2163">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2163">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2164">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2164">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2165">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2165">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="2d8a5-2166">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2166">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="2d8a5-2167">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2167">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="2d8a5-2168">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2168">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2169">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2170">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2170">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2d8a5-2171">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2171">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2d8a5-2172">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2172">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2d8a5-2173">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2173">Az.Advisor</span></span>
* <span data-ttu-id="2d8a5-2174">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2174">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2d8a5-2175">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2175">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-2176">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2176">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-2177">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2177">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2d8a5-2178">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2178">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2d8a5-2179">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2179">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2d8a5-2180">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2180">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2d8a5-2181">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2181">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2d8a5-2182">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2182">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2d8a5-2183">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2183">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2184">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2184">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2185">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2185">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2186">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2186">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2187">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2187">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-2188">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2188">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-2189">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2189">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d8a5-2190">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2190">Az.EventGrid</span></span>
* <span data-ttu-id="2d8a5-2191">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2191">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-2192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2192">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-2193">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2193">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2194">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2195">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2195">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2d8a5-2196">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2196">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-2197">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2197">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-2198">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2198">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2d8a5-2199">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2199">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-2200">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2200">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-2201">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2201">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2202">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2202">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2203">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2203">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2204">Az.Resources</span></span>
    - <span data-ttu-id="2d8a5-2205">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2205">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2d8a5-2206">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2206">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2d8a5-2207">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2207">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2d8a5-2208">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2208">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d8a5-2209">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2209">Az.ServiceBus</span></span>
* <span data-ttu-id="2d8a5-2210">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2210">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2211">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2212">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2212">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2d8a5-2213">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2213">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2d8a5-2214">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2214">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d8a5-2215">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2215">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d8a5-2216">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2216">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2d8a5-2217">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2217">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2d8a5-2218">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2218">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2d8a5-2219">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2219">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2d8a5-2220">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2220">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2221">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2221">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2222">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2222">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2d8a5-2223">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2223">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2d8a5-2224">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2224">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2d8a5-2225">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2225">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2d8a5-2226">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2226">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2d8a5-2227">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2227">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2d8a5-2228">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2228">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2d8a5-2229">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2229">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2d8a5-2230">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2230">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2d8a5-2231">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2231">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2d8a5-2232">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2232">Az.StorageSync</span></span>
* <span data-ttu-id="2d8a5-2233">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2233">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2d8a5-2234">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2234">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2235">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2236">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2236">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2d8a5-2237">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2237">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2d8a5-2238">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2238">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2d8a5-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2239">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2d8a5-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2240">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2241">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2241">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2242">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2242">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2d8a5-2243">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2243">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2d8a5-2244">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2244">Az.Dns</span></span>
* <span data-ttu-id="2d8a5-2245">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2245">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d8a5-2246">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2246">Az.EventGrid</span></span>
* <span data-ttu-id="2d8a5-2247">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2247">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2d8a5-2248">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2248">New cmdlets:</span></span>
    - <span data-ttu-id="2d8a5-2249">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2249">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d8a5-2250">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2250">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d8a5-2251">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2251">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d8a5-2252">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2252">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2d8a5-2253">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2253">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2d8a5-2254">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2254">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d8a5-2255">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2255">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2d8a5-2256">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2256">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2d8a5-2257">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2257">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2d8a5-2258">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2258">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2d8a5-2259">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2259">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2d8a5-2260">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2260">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2d8a5-2261">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2261">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2d8a5-2262">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2262">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="2d8a5-2263">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2263">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2d8a5-2264">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2264">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2d8a5-2265">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2265">Updated cmdlets:</span></span>
    - <span data-ttu-id="2d8a5-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2266">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2d8a5-2267">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2267">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2d8a5-2268">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2268">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2d8a5-2269">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2269">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2d8a5-2270">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2270">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2d8a5-2271">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2271">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2d8a5-2272">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2272">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2d8a5-2273">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2273">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2d8a5-2274">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2274">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="2d8a5-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2275">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2d8a5-2276">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2276">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2d8a5-2277">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2277">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2d8a5-2278">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2278">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2d8a5-2279">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2279">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-2280">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2280">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-2281">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2281">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2d8a5-2282">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2282">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2d8a5-2283">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2283">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2d8a5-2284">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2284">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2285">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2285">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2286">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2286">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2d8a5-2287">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2287">New cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2288">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2d8a5-2289">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2289">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2d8a5-2290">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2290">New cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2291">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2291">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2d8a5-2292">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2292">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2d8a5-2293">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2293">New cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2294">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2294">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d8a5-2295">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2295">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d8a5-2296">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2296">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2d8a5-2297">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2297">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2d8a5-2298">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2298">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2d8a5-2299">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2299">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2d8a5-2300">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2300">New cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2301">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2301">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d8a5-2302">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2302">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d8a5-2303">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2303">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2d8a5-2304">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2304">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2d8a5-2305">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2305">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2d8a5-2306">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2306">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2d8a5-2307">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2307">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2d8a5-2308">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2308">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2d8a5-2309">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2309">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2d8a5-2310">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2310">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2d8a5-2311">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2311">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2d8a5-2312">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2312">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2d8a5-2313">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2313">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2d8a5-2314">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2314">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2d8a5-2315">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2315">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2d8a5-2316">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2316">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2d8a5-2317">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2317">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2d8a5-2318">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2318">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2d8a5-2319">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2319">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-2320">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2320">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2d8a5-2321">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2321">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2d8a5-2322">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2322">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2d8a5-2323">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2323">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="2d8a5-2324">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2324">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="2d8a5-2325">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2325">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2d8a5-2326">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2326">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2d8a5-2327">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2327">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-2328">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2328">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-2329">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2329">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2330">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2331">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2331">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2d8a5-2332">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2332">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2d8a5-2333">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2333">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2d8a5-2334">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2334">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-2335">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2335">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-2336">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2336">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2337">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2338">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2338">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2d8a5-2339">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2339">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2d8a5-2340">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2340">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2d8a5-2341">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2341">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d8a5-2342">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2342">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d8a5-2343">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2343">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2d8a5-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2344">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2d8a5-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2345">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2346">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2346">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2347">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2347">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2d8a5-2348">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2348">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d8a5-2349">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2349">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2d8a5-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2350">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2351">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2351">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2352">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2352">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2d8a5-2353">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2353">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2d8a5-2354">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2354">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2d8a5-2355">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2355">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-2356">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2356">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2357">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2357">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2358">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2358">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2d8a5-2359">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2359">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-2360">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2360">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-2361">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2361">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2d8a5-2362">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2362">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2363">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2363">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2364">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2364">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2d8a5-2365">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2365">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-2366">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2366">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-2367">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2367">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2368">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2369">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2369">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d8a5-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="2d8a5-2371">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2371">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-2372">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2372">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-2373">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2373">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2d8a5-2374">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2374">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2375">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2375">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2376">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2376">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2d8a5-2377">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2377">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2d8a5-2378">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2378">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2d8a5-2379">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2379">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2380">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2380">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2381">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2381">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2d8a5-2382">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2382">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-2383">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2383">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-2384">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2384">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2d8a5-2385">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2385">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2d8a5-2386">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2386">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2d8a5-2387">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2387">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2d8a5-2388">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2388">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2d8a5-2389">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2389">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2d8a5-2390">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2390">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2d8a5-2391">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2391">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2d8a5-2392">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2392">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2d8a5-2393">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2393">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2d8a5-2394">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2394">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2d8a5-2395">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2395">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2d8a5-2396">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2396">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2d8a5-2397">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2397">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2d8a5-2398">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2398">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2d8a5-2399">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2399">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2d8a5-2400">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2400">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2d8a5-2401">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2401">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2d8a5-2402">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2402">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="2d8a5-2403">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2403">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2d8a5-2404">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2404">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2d8a5-2405">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2405">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2d8a5-2406">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2406">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2d8a5-2407">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2407">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="2d8a5-2408">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2408">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2d8a5-2409">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2409">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2d8a5-2410">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2410">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2d8a5-2411">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2411">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2d8a5-2412">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2412">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2d8a5-2413">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2413">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2d8a5-2414">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2414">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="2d8a5-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2415">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2d8a5-2416">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2416">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2d8a5-2417">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2417">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d8a5-2418">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2418">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2d8a5-2419">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2419">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2d8a5-2420">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2420">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2d8a5-2421">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2421">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2d8a5-2422">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2422">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2d8a5-2423">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2423">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d8a5-2424">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2424">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2d8a5-2425">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2425">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2d8a5-2426">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2426">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2d8a5-2427">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2427">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2d8a5-2428">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2428">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2d8a5-2429">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2429">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2d8a5-2430">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2430">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2d8a5-2431">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2431">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2d8a5-2432">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2432">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2d8a5-2433">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2433">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2d8a5-2434">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2434">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2d8a5-2435">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2435">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2d8a5-2436">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2436">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2d8a5-2437">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2437">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2d8a5-2438">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2438">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2d8a5-2439">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2439">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2d8a5-2440">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2440">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2d8a5-2441">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2441">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2d8a5-2442">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2442">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2d8a5-2443">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2443">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2d8a5-2444">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2444">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2d8a5-2445">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2445">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2d8a5-2446">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2446">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2d8a5-2447">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2447">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2d8a5-2448">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2448">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2d8a5-2449">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2449">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2d8a5-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2450">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2d8a5-2451">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2451">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2d8a5-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2452">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2d8a5-2453">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2453">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2d8a5-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2454">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2d8a5-2455">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2455">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2d8a5-2456">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2456">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2d8a5-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2457">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2d8a5-2458">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2458">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="2d8a5-2459">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2459">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2d8a5-2460">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2460">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2461">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2462">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2462">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2d8a5-2463">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2463">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2d8a5-2464">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2d8a5-2465">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2465">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2d8a5-2466">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2466">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2d8a5-2467">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2467">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2d8a5-2468">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2468">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2469">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2469">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2470">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2470">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2d8a5-2471">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2471">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-2472">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2472">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-2473">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2473">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-2474">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2474">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-2475">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2475">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2476">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2476">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2477">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2477">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2d8a5-2478">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2478">Updated cmdlet:</span></span>
        - <span data-ttu-id="2d8a5-2479">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2479">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2d8a5-2480">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2480">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2481">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2482">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2482">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2483">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2484">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2484">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2d8a5-2485">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2485">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2486">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2487">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2487">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-2488">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2488">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-2489">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2489">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2d8a5-2490">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2490">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2491">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2491">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2492">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2492">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2d8a5-2493">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2493">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2d8a5-2494">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2494">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2d8a5-2495">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2495">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2d8a5-2496">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2496">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2d8a5-2497">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2497">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="2d8a5-2498">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2498">Breaking changes</span></span>
    - <span data-ttu-id="2d8a5-2499">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2499">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2d8a5-2500">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2500">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2d8a5-2501">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2501">Az.DeploymentManager</span></span>
* <span data-ttu-id="2d8a5-2502">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2502">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2d8a5-2503">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2503">Az.Dns</span></span>
* <span data-ttu-id="2d8a5-2504">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2504">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2d8a5-2505">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2505">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2d8a5-2506">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2506">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-2507">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2507">Az.FrontDoor</span></span>
* <span data-ttu-id="2d8a5-2508">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2508">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2d8a5-2509">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2509">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-2510">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2510">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-2511">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2511">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2d8a5-2512">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2512">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2d8a5-2513">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2513">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2d8a5-2514">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2514">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2d8a5-2515">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2515">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2d8a5-2516">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2516">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2d8a5-2517">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2517">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-2518">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2518">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-2519">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2519">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="2d8a5-2520">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2520">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2d8a5-2521">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2521">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2d8a5-2522">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2522">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2d8a5-2523">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2523">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2d8a5-2524">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2524">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2d8a5-2525">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2525">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2d8a5-2526">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2526">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d8a5-2527">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2527">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d8a5-2528">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2528">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d8a5-2529">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2529">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d8a5-2530">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2530">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2d8a5-2531">[Mais](/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2531">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2d8a5-2532">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2532">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2533">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2533">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2534">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2534">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2d8a5-2535">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2535">New cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2536">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2536">New-AzNatGateway</span></span>
        - <span data-ttu-id="2d8a5-2537">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2537">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2d8a5-2538">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2538">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2d8a5-2539">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2539">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2d8a5-2540">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2540">Updated cmdlets</span></span>
        - <span data-ttu-id="2d8a5-2541">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2541">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2d8a5-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2542">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2d8a5-2543">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2543">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2d8a5-2544">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2544">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2d8a5-2545">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2545">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-2546">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2546">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-2547">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2547">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2d8a5-2548">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2548">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2d8a5-2549">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2549">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2550">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2550">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2551">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2551">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2d8a5-2552">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2552">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2d8a5-2553">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2553">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2d8a5-2554">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2554">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2d8a5-2555">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2555">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2d8a5-2556">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2556">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2d8a5-2557">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2557">Az.Relay</span></span>
* <span data-ttu-id="2d8a5-2558">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2558">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d8a5-2559">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2559">Az.ServiceBus</span></span>
* <span data-ttu-id="2d8a5-2560">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2560">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2561">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2562">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2562">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2d8a5-2563">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2563">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2d8a5-2564">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2564">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2d8a5-2565">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2565">New-AzStorageAccount</span></span>
* <span data-ttu-id="2d8a5-2566">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2566">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2d8a5-2567">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2567">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2d8a5-2568">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2568">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2d8a5-2569">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2569">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2570">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2570">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2571">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2571">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2d8a5-2572">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2572">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2d8a5-2573">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2573">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d8a5-2574">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2574">Highlights since the last major release</span></span>
* <span data-ttu-id="2d8a5-2575">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2575">General availability of `Az` module</span></span>
* <span data-ttu-id="2d8a5-2576">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2576">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d8a5-2577">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2577">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d8a5-2578">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2578">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d8a5-2579">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2579">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d8a5-2580">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2580">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2581">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2581">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2582">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2582">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2583">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2583">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2d8a5-2584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2584">Az.Batch</span></span>
* <span data-ttu-id="2d8a5-2585">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2585">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-2586">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2586">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-2587">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2587">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-2588">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2588">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-2589">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2590">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2590">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2591">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2591">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2d8a5-2592">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2592">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d8a5-2593">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2593">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-2594">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2594">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-2595">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2595">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-2596">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2596">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-2597">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2597">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d8a5-2598">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2598">Az.EventGrid</span></span>
* <span data-ttu-id="2d8a5-2599">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2599">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-2600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2600">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-2601">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2601">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2d8a5-2602">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2602">Az.HDInsight</span></span>
* <span data-ttu-id="2d8a5-2603">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2603">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-2604">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2604">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-2605">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2605">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-2606">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2606">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-2607">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2607">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d8a5-2608">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2608">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2d8a5-2609">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2609">Az.MachineLearning</span></span>
* <span data-ttu-id="2d8a5-2610">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2d8a5-2611">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2611">Az.Media</span></span>
* <span data-ttu-id="2d8a5-2612">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-2613">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2613">Az.Monitor</span></span>
  * <span data-ttu-id="2d8a5-2614">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2614">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2d8a5-2615">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2615">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2d8a5-2616">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2616">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2d8a5-2617">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2617">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2d8a5-2618">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2618">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2d8a5-2619">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2619">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2d8a5-2620">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2620">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2621">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2622">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2622">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d8a5-2623">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2623">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2d8a5-2624">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2624">Az.NotificationHubs</span></span>
* <span data-ttu-id="2d8a5-2625">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2625">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-2626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2626">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-2627">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2627">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2d8a5-2628">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2628">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d8a5-2629">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2629">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2630">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2630">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2631">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2631">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d8a5-2632">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2632">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2d8a5-2633">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2633">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2d8a5-2634">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2634">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d8a5-2635">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2635">Az.RedisCache</span></span>
* <span data-ttu-id="2d8a5-2636">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2636">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2637">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2638">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2638">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2639">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2640">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2640">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2d8a5-2641">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2641">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d8a5-2642">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2642">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2d8a5-2643">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2643">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2d8a5-2644">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2644">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2d8a5-2645">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2645">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2d8a5-2646">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2646">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2647">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2647">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2648">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2648">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2d8a5-2649">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2649">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2d8a5-2650">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2650">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2d8a5-2651">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2651">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2d8a5-2652">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2652">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d8a5-2653">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2653">Highlights since the last major release</span></span>
* <span data-ttu-id="2d8a5-2654">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2654">General availability of `Az` module</span></span>
* <span data-ttu-id="2d8a5-2655">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2655">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d8a5-2656">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2656">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d8a5-2657">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2657">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d8a5-2658">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2658">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d8a5-2659">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2659">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2660">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2660">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2661">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2661">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2662">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2662">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d8a5-2663">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2663">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d8a5-2664">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2664">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2d8a5-2665">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2665">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2666">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2666">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2667">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2667">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2d8a5-2668">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2668">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2d8a5-2669">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2669">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2670">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2670">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2671">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2671">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2d8a5-2672">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2672">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2d8a5-2673">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2673">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d8a5-2674">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2674">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-2675">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2675">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-2676">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2676">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2d8a5-2677">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2677">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2678">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2678">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2679">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2679">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2d8a5-2680">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2680">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2d8a5-2681">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2681">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2d8a5-2682">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2682">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2d8a5-2683">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2683">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2d8a5-2684">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2684">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2685">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2685">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2686">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2686">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2687">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2687">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2688">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2688">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2d8a5-2689">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2689">New-AzStorageContext</span></span>
* <span data-ttu-id="2d8a5-2690">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2690">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2d8a5-2691">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2691">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2d8a5-2692">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2692">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2d8a5-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2693">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2d8a5-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2694">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2d8a5-2695">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2695">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2d8a5-2696">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2696">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2d8a5-2697">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2697">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2d8a5-2698">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2698">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2d8a5-2699">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2699">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2d8a5-2700">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2700">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2d8a5-2701">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2701">Highlights since the last major release</span></span>
* <span data-ttu-id="2d8a5-2702">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2702">General availability of `Az` module</span></span>
* <span data-ttu-id="2d8a5-2703">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2703">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2d8a5-2704">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2704">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2d8a5-2705">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2705">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2d8a5-2706">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2706">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d8a5-2707">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2707">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2708">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2708">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2709">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2709">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2710">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2710">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2d8a5-2711">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2711">Dynamic grouping</span></span>
    * <span data-ttu-id="2d8a5-2712">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2712">Pre-Post script</span></span>
    * <span data-ttu-id="2d8a5-2713">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2713">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2714">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2714">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2715">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2715">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2d8a5-2716">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2716">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-2717">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2717">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-2718">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2718">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2719">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2720">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2720">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2d8a5-2721">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2721">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2722">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2723">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2723">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2d8a5-2724">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2724">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2725">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2725">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2726">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2726">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2d8a5-2727">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2727">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2728">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2729">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2729">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2730">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2731">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2731">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2d8a5-2732">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2732">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d8a5-2733">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2733">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d8a5-2734">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2734">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2d8a5-2735">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2735">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2d8a5-2736">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2736">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2d8a5-2737">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2737">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2738">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2739">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2739">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="2d8a5-2740">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2740">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2741">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2741">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2742">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2742">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2d8a5-2743">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2743">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2744">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2744">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2745">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2745">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d8a5-2746">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2746">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2d8a5-2747">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2747">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-2748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2748">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-2749">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2749">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2750">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2751">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2751">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-2752">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2752">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-2753">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2753">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d8a5-2754">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2754">Az.LogicApp</span></span>
* <span data-ttu-id="2d8a5-2755">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2755">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2756">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2756">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2757">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2757">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2758">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2758">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2759">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2759">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2d8a5-2760">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2760">SDK Update</span></span>
* <span data-ttu-id="2d8a5-2761">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2761">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2d8a5-2762">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2762">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2763">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2763">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2764">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2764">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2d8a5-2765">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2765">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2d8a5-2766">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2766">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2d8a5-2767">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2767">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2d8a5-2768">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2768">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2d8a5-2769">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2769">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2770">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2771">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2771">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2d8a5-2772">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2772">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2773">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2773">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2774">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2774">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2d8a5-2775">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2775">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2d8a5-2776">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2776">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d8a5-2777">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2777">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2778">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2778">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2779">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2779">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2d8a5-2780">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2780">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2d8a5-2781">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2781">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-2782">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2782">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-2783">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2783">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2784">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2785">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2785">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2d8a5-2786">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2786">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2d8a5-2787">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2787">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2d8a5-2788">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2788">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-2789">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2789">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-2790">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2790">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2d8a5-2791">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2791">Az.EventHub</span></span>
* <span data-ttu-id="2d8a5-2792">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2792">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-2793">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2793">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-2794">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2794">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d8a5-2795">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2795">Az.LogicApp</span></span>
* <span data-ttu-id="2d8a5-2796">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2796">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2d8a5-2797">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2797">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2d8a5-2798">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2798">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2d8a5-2799">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2799">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d8a5-2800">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2800">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d8a5-2801">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2801">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2d8a5-2802">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2802">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2d8a5-2803">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2803">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2d8a5-2804">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2804">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d8a5-2805">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2805">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d8a5-2806">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2806">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2d8a5-2807">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2807">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2d8a5-2808">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2808">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2d8a5-2809">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2809">Az.Monitor</span></span>
* <span data-ttu-id="2d8a5-2810">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2810">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2811">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2811">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2812">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2812">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-2813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2813">Az.OperationalInsights</span></span>
* <span data-ttu-id="2d8a5-2814">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2814">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2d8a5-2815">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2815">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="2d8a5-2816">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2816">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2817">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2817">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2818">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2818">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d8a5-2819">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2d8a5-2820">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2d8a5-2821">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2821">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2822">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2823">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2823">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2d8a5-2824">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2824">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2825">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2825">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2826">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2826">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2d8a5-2827">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2827">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2828">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2828">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2829">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2829">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d8a5-2830">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2830">Az.AnalysisServices</span></span>
<span data-ttu-id="2d8a5-2831">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2831">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2832">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2832">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2833">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2833">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2d8a5-2834">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2834">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2d8a5-2835">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2835">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2836">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2836">Az.RecoveryServices</span></span>
<span data-ttu-id="2d8a5-2837">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2837">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2838">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2838">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2839">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2839">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="2d8a5-2840">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2840">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2d8a5-2841">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2841">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="2d8a5-2842">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2842">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2843">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2843">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2844">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2844">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2d8a5-2845">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2845">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2d8a5-2846">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2846">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2d8a5-2847">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2847">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2848">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2848">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2849">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2849">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2d8a5-2850">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2850">Az.AnalysisServices</span></span>
* <span data-ttu-id="2d8a5-2851">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2851">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-2852">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2852">Az.RecoveryServices</span></span>
* <span data-ttu-id="2d8a5-2853">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2853">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2d8a5-2854">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2854">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2855">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2855">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2856">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2856">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2d8a5-2857">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2857">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d8a5-2858">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2858">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2d8a5-2859">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2859">Az.Aks</span></span>
* <span data-ttu-id="2d8a5-2860">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2860">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2d8a5-2861">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2861">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-2862">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2862">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2d8a5-2863">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2863">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2d8a5-2864">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2864">Az.Cdn</span></span>
* <span data-ttu-id="2d8a5-2865">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2865">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2866">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2866">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2867">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2867">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2d8a5-2868">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2868">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2d8a5-2869">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2869">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2d8a5-2870">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2870">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2d8a5-2871">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2871">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2d8a5-2872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2872">Az.DataFactory</span></span>
* <span data-ttu-id="2d8a5-2873">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2873">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-2874">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2874">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-2875">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2875">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2d8a5-2876">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2876">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2d8a5-2877">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2877">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-2878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2878">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-2879">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2879">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-2880">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2880">Az.KeyVault</span></span>
* <span data-ttu-id="2d8a5-2881">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2881">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2882">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2882">Az.Network</span></span>
* <span data-ttu-id="2d8a5-2883">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2883">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2884">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2884">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2885">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2885">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2d8a5-2886">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2886">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2d8a5-2887">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2887">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2d8a5-2888">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2888">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2d8a5-2889">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2d8a5-2890">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2890">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2d8a5-2891">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2891">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-2892">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2892">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-2893">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2893">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2d8a5-2894">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2894">Fix some error messages.</span></span>
* <span data-ttu-id="2d8a5-2895">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2895">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2d8a5-2896">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2896">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d8a5-2897">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2897">Az.SignalR</span></span>
* <span data-ttu-id="2d8a5-2898">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2898">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2899">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2899">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2900">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2900">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d8a5-2901">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2901">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2d8a5-2902">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2902">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2d8a5-2903">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2903">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2904">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2904">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2905">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2905">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d8a5-2906">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2906">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2d8a5-2907">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2907">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2d8a5-2908">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2908">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2d8a5-2909">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2909">Az.TrafficManager</span></span>
* <span data-ttu-id="2d8a5-2910">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2910">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2911">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2911">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2912">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2912">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2d8a5-2913">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2913">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2d8a5-2914">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2914">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2d8a5-2915">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2915">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2916">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2916">Az.Accounts</span></span>
* <span data-ttu-id="2d8a5-2917">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2917">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-2918">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2918">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-2919">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2919">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2d8a5-2920">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2920">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2d8a5-2921">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2921">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-2922">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2922">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-2923">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2923">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2d8a5-2924">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2924">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2d8a5-2925">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2925">Az.EventGrid</span></span>
* <span data-ttu-id="2d8a5-2926">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2926">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2d8a5-2927">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2927">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2d8a5-2928">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2928">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d8a5-2929">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2929">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d8a5-2930">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2930">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d8a5-2931">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2931">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2d8a5-2932">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2932">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2d8a5-2933">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2933">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2d8a5-2934">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2934">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2d8a5-2935">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2935">Dead letter endpoint.</span></span>
* <span data-ttu-id="2d8a5-2936">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2936">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2d8a5-2937">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2937">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2d8a5-2938">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2938">Az.IotHub</span></span>
* <span data-ttu-id="2d8a5-2939">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2939">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2d8a5-2940">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2940">Az.LogicApp</span></span>
* <span data-ttu-id="2d8a5-2941">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2941">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-2942">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2942">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-2943">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2943">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2d8a5-2944">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2944">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2d8a5-2945">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2945">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d8a5-2946">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2946">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2d8a5-2947">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2947">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2d8a5-2948">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2948">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2d8a5-2949">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2949">Az.SignalR</span></span>
* <span data-ttu-id="2d8a5-2950">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2950">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-2951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2951">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-2952">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2952">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2d8a5-2953">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2953">Az.Storage</span></span>
* <span data-ttu-id="2d8a5-2954">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2954">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2d8a5-2955">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2955">New-AzStorageContext</span></span>
* <span data-ttu-id="2d8a5-2956">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2956">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2d8a5-2957">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2957">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-2958">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2958">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-2959">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2959">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2d8a5-2960">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2960">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2d8a5-2961">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2961">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2d8a5-2962">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2962">General</span></span>

- <span data-ttu-id="2d8a5-2963">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2963">General Availability of Az Module</span></span>
- <span data-ttu-id="2d8a5-2964">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2964">Online help for each module</span></span>
- <span data-ttu-id="2d8a5-2965">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2965">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2d8a5-2966">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2966">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2d8a5-2967">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2967">Az.Accounts</span></span>
- <span data-ttu-id="2d8a5-2968">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2968">Changed from Az.Profile</span></span>
- <span data-ttu-id="2d8a5-2969">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2969">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-2970">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2970">Az.ApiManagement</span></span>
- <span data-ttu-id="2d8a5-2971">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2971">Fixes for #7002</span></span>
- <span data-ttu-id="2d8a5-2972">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2972">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2d8a5-2973">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2973">Az.Batch</span></span>
- <span data-ttu-id="2d8a5-2974">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2974">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2d8a5-2975">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2975">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2d8a5-2976">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2d8a5-2977">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2977">Az.Billing</span></span>
- <span data-ttu-id="2d8a5-2978">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2978">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2d8a5-2979">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2979">Az.CognitivServices</span></span>
- <span data-ttu-id="2d8a5-2980">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2980">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2d8a5-2981">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2981">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d8a5-2982">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2982">Az.ContainerInstance</span></span>
- <span data-ttu-id="2d8a5-2983">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2983">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2d8a5-2984">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2984">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2d8a5-2985">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2985">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-2986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2986">Az.DataLakeStore</span></span>
- <span data-ttu-id="2d8a5-2987">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2987">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2d8a5-2988">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2988">Az.Monitor</span></span>
- <span data-ttu-id="2d8a5-2989">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2989">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2d8a5-2990">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2990">Az.KeyVault</span></span>
- <span data-ttu-id="2d8a5-2991">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2991">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2d8a5-2992">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2992">Az.MachineLearning</span></span>
- <span data-ttu-id="2d8a5-2993">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2993">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2d8a5-2994">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2994">Az.Media</span></span>
- <span data-ttu-id="2d8a5-2995">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2995">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d8a5-2996">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2996">Az.Network</span></span>
<span data-ttu-id="2d8a5-2997">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2997">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2d8a5-2998">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2998">New cmdlets added:</span></span>
        - <span data-ttu-id="2d8a5-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-2999">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d8a5-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3000">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d8a5-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3001">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d8a5-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3002">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d8a5-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3003">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2d8a5-3004">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3004">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2d8a5-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3005">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2d8a5-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3006">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2d8a5-3007">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3007">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2d8a5-3008">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3008">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2d8a5-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3009">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d8a5-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3010">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2d8a5-3011">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3011">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2d8a5-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3012">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2d8a5-3013">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3013">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2d8a5-3014">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3014">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2d8a5-3015">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3015">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d8a5-3016">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3016">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2d8a5-3017">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3017">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2d8a5-3018">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3018">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2d8a5-3019">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3019">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2d8a5-3020">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3020">Az.OperationalInsights</span></span>
- <span data-ttu-id="2d8a5-3021">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3021">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2d8a5-3022">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3022">Az.Profile</span></span>
- <span data-ttu-id="2d8a5-3023">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3023">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-3024">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3024">Az.RecoveryServices</span></span>
- <span data-ttu-id="2d8a5-3025">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3025">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2d8a5-3026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3026">Az.Resources</span></span>
- <span data-ttu-id="2d8a5-3027">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3027">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-3028">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3028">Az.ServiceFabric</span></span>
- <span data-ttu-id="2d8a5-3029">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3029">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2d8a5-3030">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3030">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2d8a5-3031">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3031">Az.SIgnalR</span></span>
- <span data-ttu-id="2d8a5-3032">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3032">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2d8a5-3033">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3033">Az.Sql</span></span>
- <span data-ttu-id="2d8a5-3034">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3034">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2d8a5-3035">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3035">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2d8a5-3036">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3036">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d8a5-3037">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3037">Az.Storage</span></span>
- <span data-ttu-id="2d8a5-3038">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3038">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d8a5-3039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3039">Az.Websites</span></span>
- <span data-ttu-id="2d8a5-3040">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3040">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2d8a5-3041">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3041">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2d8a5-3042">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3042">General</span></span>

* <span data-ttu-id="2d8a5-3043">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3043">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d8a5-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3044">Az.Compute</span></span>

* <span data-ttu-id="2d8a5-3045">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3045">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-3046">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3046">Az.DataLakeStore</span></span>

* <span data-ttu-id="2d8a5-3047">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3047">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2d8a5-3048">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3048">Az.FrontDoor</span></span>

* <span data-ttu-id="2d8a5-3049">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3049">Fixed some broken links</span></span>
    - <span data-ttu-id="2d8a5-3050">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3050">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2d8a5-3051">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3051">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2d8a5-3052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3052">Az.RecoveryServices</span></span>

* <span data-ttu-id="2d8a5-3053">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3053">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2d8a5-3054">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3054">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d8a5-3055">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3055">Az.Resources</span></span>

* <span data-ttu-id="2d8a5-3056">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3056">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2d8a5-3057">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3057">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2d8a5-3058">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3058">Az.Sql</span></span>

* <span data-ttu-id="2d8a5-3059">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3059">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2d8a5-3060">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3060">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2d8a5-3061">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3061">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2d8a5-3062">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3062">Az.Storage</span></span>

* <span data-ttu-id="2d8a5-3063">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3063">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2d8a5-3064">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3064">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2d8a5-3065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d8a5-3066">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3066">Support Static Website configuration</span></span>
    - <span data-ttu-id="2d8a5-3067">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3067">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2d8a5-3068">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3068">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2d8a5-3069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3069">Az.Websites</span></span>

* <span data-ttu-id="2d8a5-3070">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3070">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="2d8a5-3071">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3071">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2d8a5-3072">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3072">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2d8a5-3073">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3073">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2d8a5-3074">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3074">Az.ApiManagement</span></span>
* <span data-ttu-id="2d8a5-3075">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3075">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2d8a5-3076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3076">Az.Automation</span></span>
* <span data-ttu-id="2d8a5-3077">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3077">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2d8a5-3078">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3078">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2d8a5-3079">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3079">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2d8a5-3080">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3080">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2d8a5-3081">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3081">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2d8a5-3082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3082">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-3083">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3083">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2d8a5-3084">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3084">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2d8a5-3085">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3085">Az.ContainerInstance</span></span>
* <span data-ttu-id="2d8a5-3086">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3086">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2d8a5-3087">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3087">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d8a5-3088">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3088">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2d8a5-3089">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3089">Az.Network</span></span>
* <span data-ttu-id="2d8a5-3090">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3090">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2d8a5-3091">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3091">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2d8a5-3092">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3092">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="2d8a5-3093">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3093">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2d8a5-3094">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3094">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d8a5-3095">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3095">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2d8a5-3096">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3096">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2d8a5-3097">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3097">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2d8a5-3098">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3098">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2d8a5-3099">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3099">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2d8a5-3100">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3100">Az.Relay</span></span>
* <span data-ttu-id="2d8a5-3101">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3101">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2d8a5-3102">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3102">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-3103">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3103">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2d8a5-3104">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3104">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2d8a5-3105">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3105">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-3106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3106">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-3107">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3107">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2d8a5-3108">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3108">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-3109">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3109">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2d8a5-3110">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3110">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d8a5-3111">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3111">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d8a5-3112">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3112">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d8a5-3113">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3113">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2d8a5-3114">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3114">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d8a5-3115">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3115">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d8a5-3116">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3116">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2d8a5-3117">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3117">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2d8a5-3118">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3118">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2d8a5-3119">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3119">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2d8a5-3120">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3120">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2d8a5-3121">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3121">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d8a5-3122">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3122">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2d8a5-3123">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3123">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2d8a5-3124">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3124">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2d8a5-3125">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3125">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2d8a5-3126">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3126">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d8a5-3127">Geral</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3127">General</span></span>
* <span data-ttu-id="2d8a5-3128">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3128">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2d8a5-3129">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3129">Az.Profile</span></span>
* <span data-ttu-id="2d8a5-3130">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3130">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2d8a5-3131">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3131">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2d8a5-3132">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3132">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2d8a5-3133">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3133">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2d8a5-3134">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3134">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2d8a5-3135">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3135">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2d8a5-3136">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3136">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-3137">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3137">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-3138">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3138">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-3139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3139">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-3140">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3140">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2d8a5-3141">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3141">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2d8a5-3142">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3142">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-3143">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3143">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-3144">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3144">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2d8a5-3145">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3145">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2d8a5-3146">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3146">Az.Insights</span></span>
* <span data-ttu-id="2d8a5-3147">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3147">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2d8a5-3148">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3148">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2d8a5-3149">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3149">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2d8a5-3150">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3150">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-3151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3151">Az.Network</span></span>
* <span data-ttu-id="2d8a5-3152">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3152">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2d8a5-3153">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3153">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2d8a5-3154">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3154">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2d8a5-3155">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3155">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2d8a5-3156">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3156">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2d8a5-3157">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3157">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2d8a5-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3158">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2d8a5-3159">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3159">Az.PolicyInsights</span></span>
* <span data-ttu-id="2d8a5-3160">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3160">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-3161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3161">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-3162">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3162">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2d8a5-3163">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3163">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2d8a5-3164">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3164">Az.ServiceBus</span></span>
* <span data-ttu-id="2d8a5-3165">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3165">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2d8a5-3166">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3166">Az.ServiceFabric</span></span>
* <span data-ttu-id="2d8a5-3167">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3167">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2d8a5-3168">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3168">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2d8a5-3169">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3169">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2d8a5-3170">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3170">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2d8a5-3171">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3171">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2d8a5-3172">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3172">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2d8a5-3173">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3173">Az.Profile</span></span>
* <span data-ttu-id="2d8a5-3174">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3174">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2d8a5-3175">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3175">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-3176">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3176">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-3177">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3177">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2d8a5-3178">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3178">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2d8a5-3179">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3179">Az.DataLakeStore</span></span>
* <span data-ttu-id="2d8a5-3180">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3180">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2d8a5-3181">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3181">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2d8a5-3182">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3182">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d8a5-3183">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3183">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2d8a5-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3184">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-3185">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3185">Az.Network</span></span>
* <span data-ttu-id="2d8a5-3186">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3186">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2d8a5-3187">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3187">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-3188">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3188">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-3189">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3189">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2d8a5-3190">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3190">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2d8a5-3191">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3191">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2d8a5-3192">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3192">Azure.Storage</span></span>
* <span data-ttu-id="2d8a5-3193">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3193">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2d8a5-3194">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3194">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2d8a5-3195">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3195">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2d8a5-3196">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3196">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2d8a5-3197">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3197">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2d8a5-3198">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3198">Az.CognitiveServices</span></span>
* <span data-ttu-id="2d8a5-3199">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3199">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2d8a5-3200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3200">Az.Compute</span></span>
* <span data-ttu-id="2d8a5-3201">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3201">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2d8a5-3202">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3202">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2d8a5-3203">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3203">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2d8a5-3204">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3204">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2d8a5-3205">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3205">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2d8a5-3206">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3206">Az.Network</span></span>
* <span data-ttu-id="2d8a5-3207">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3207">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2d8a5-3208">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3208">new cmdlets added</span></span>
    - <span data-ttu-id="2d8a5-3209">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3209">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d8a5-3210">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3210">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d8a5-3211">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3211">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d8a5-3212">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3212">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2d8a5-3213">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3213">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2d8a5-3214">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3214">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2d8a5-3215">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3215">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2d8a5-3216">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3216">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2d8a5-3217">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3217">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2d8a5-3218">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3218">Az.RedisCache</span></span>
* <span data-ttu-id="2d8a5-3219">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3219">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2d8a5-3220">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3220">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2d8a5-3221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3221">Az.Resources</span></span>
* <span data-ttu-id="2d8a5-3222">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3222">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2d8a5-3223">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3223">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2d8a5-3224">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3224">Az.Sql</span></span>
* <span data-ttu-id="2d8a5-3225">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3225">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2d8a5-3226">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3226">Az.Websites</span></span>
* <span data-ttu-id="2d8a5-3227">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3227">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2d8a5-3228">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3228">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2d8a5-3229">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3229">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2d8a5-3230">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="2d8a5-3230">Initial Release</span></span>