---
title: Guia de migração para o Az 2.0.0
description: Este guia de migração contém uma lista das alterações da falha feitas no Azure PowerShell no lançamento da versão 2.0 do Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2d8a3c04388bfc5028811f6d1b6caf2c6fce4147
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240073"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="31d41-103">Guia de migração para o Az 2.0.0</span><span class="sxs-lookup"><span data-stu-id="31d41-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="31d41-104">Este documento descreve as alterações entre as versões 1.0.0 e 2.0.0 do Az</span><span class="sxs-lookup"><span data-stu-id="31d41-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="31d41-105">Sumário</span><span class="sxs-lookup"><span data-stu-id="31d41-105">Table of Contents</span></span>
- [<span data-ttu-id="31d41-106">Alterações de falhas para módulos</span><span class="sxs-lookup"><span data-stu-id="31d41-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="31d41-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31d41-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="31d41-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31d41-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="31d41-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31d41-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="31d41-110">Alterações de falhas para módulos</span><span class="sxs-lookup"><span data-stu-id="31d41-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="31d41-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="31d41-111">Az.Compute</span></span>

- <span data-ttu-id="31d41-112">Remoção do parâmetro `Managed` dos cmdlets `New-AzAvailabilitySet` e `Update-AzAvailabilitySet` a favor do uso de ```Sku = Aligned```</span><span class="sxs-lookup"><span data-stu-id="31d41-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-113">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-114">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="31d41-115">Para fins de consistência, remoção do parâmetro `Image` dos conjuntos de parâmetros 'ByName' e 'ByResourceId' em `Update-AzImage`</span><span class="sxs-lookup"><span data-stu-id="31d41-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="31d41-116">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-116">Before</span></span>

  <span data-ttu-id="31d41-117">Observe que o código abaixo é funcional, mas o ImageName passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.</span><span class="sxs-lookup"><span data-stu-id="31d41-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-118">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="31d41-119">Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Restart-AzVM`</span><span class="sxs-lookup"><span data-stu-id="31d41-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="31d41-120">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-120">Before</span></span>

  <span data-ttu-id="31d41-121">Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.</span><span class="sxs-lookup"><span data-stu-id="31d41-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-122">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="31d41-123">Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Start-AzVM`</span><span class="sxs-lookup"><span data-stu-id="31d41-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="31d41-124">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-124">Before</span></span>

  <span data-ttu-id="31d41-125">Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.</span><span class="sxs-lookup"><span data-stu-id="31d41-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-126">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="31d41-127">Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Stop-AzVM`</span><span class="sxs-lookup"><span data-stu-id="31d41-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="31d41-128">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-128">Before</span></span>

  <span data-ttu-id="31d41-129">Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.</span><span class="sxs-lookup"><span data-stu-id="31d41-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-130">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="31d41-131">Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Remove-AzVM`</span><span class="sxs-lookup"><span data-stu-id="31d41-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="31d41-132">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-132">Before</span></span>

  <span data-ttu-id="31d41-133">Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.</span><span class="sxs-lookup"><span data-stu-id="31d41-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-134">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="31d41-135">Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Set-AzVM`</span><span class="sxs-lookup"><span data-stu-id="31d41-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="31d41-136">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-136">Before</span></span>

  <span data-ttu-id="31d41-137">Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.</span><span class="sxs-lookup"><span data-stu-id="31d41-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-138">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="31d41-139">Para fins de consistência, remoção do parâmetro `Name` dos conjuntos de parâmetros 'ByObject' e 'ByResourceId' em `Save-AzVMImage`</span><span class="sxs-lookup"><span data-stu-id="31d41-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="31d41-140">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-140">Before</span></span>
  <span data-ttu-id="31d41-141">Observe que o código abaixo é funcional, mas o Name passado não é usado; portanto, a remoção desse parâmetro não tem nenhum impacto funcional.</span><span class="sxs-lookup"><span data-stu-id="31d41-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="31d41-142">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="31d41-143">Adição da propriedade ProtectionPolicy para encapsular a propriedade `ProtectFromScaleIn` em `PSVirtualMachineScaleSetVM`</span><span class="sxs-lookup"><span data-stu-id="31d41-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-144">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-145">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="31d41-146">Adição da propriedade ```EncryptionSettingsCollection``` para delimitar a propriedade `EncryptionSettings` em `PSDisk`</span><span class="sxs-lookup"><span data-stu-id="31d41-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-147">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-148">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="31d41-149">Adição da propriedade ```EncryptionSettingsCollection``` para delimitar a propriedade `EncryptionSettings` em `PSSnapshot`</span><span class="sxs-lookup"><span data-stu-id="31d41-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-150">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-151">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="31d41-152">Remoção da propriedade `VirtualMachineProfile` de `PSVirtualMachineScaleSet`</span><span class="sxs-lookup"><span data-stu-id="31d41-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-153">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-154">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="31d41-155">O cmdlet `Set-AzVMBootDiagnostic` removeu o alias para `Set-AzVMBootDiagnostics`</span><span class="sxs-lookup"><span data-stu-id="31d41-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-156">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-156">Before</span></span>

  <span data-ttu-id="31d41-157">Uso do alias preterido</span><span class="sxs-lookup"><span data-stu-id="31d41-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-158">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="31d41-159">O cmdlet `Export-AzLogAnalyticThrottledRequest` removeu o alias para `Export-AzLogAnalyticThrottledRequests`</span><span class="sxs-lookup"><span data-stu-id="31d41-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-160">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-160">Before</span></span>

  <span data-ttu-id="31d41-161">Uso do alias preterido</span><span class="sxs-lookup"><span data-stu-id="31d41-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-162">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="31d41-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="31d41-163">Az.HDInsight</span></span>

- <span data-ttu-id="31d41-164">Remoção dos cmdlets `Grant-AzHDInsightHttpServicesAccess` e `Revoke-AzHDInsightHttpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="31d41-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="31d41-165">Eles não são mais necessários porque o acesso HTTP está sempre habilitado em todos os clusters do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31d41-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="31d41-166">Adição de um novo cmdlet `Set-AzHDInsightGatewayCredential`.</span><span class="sxs-lookup"><span data-stu-id="31d41-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="31d41-167">Use esse cmdlet para alterar o nome de usuário e a senha HTTP do gateway (substitui `Grant-AzHDInsightHttpServicesAccess`).</span><span class="sxs-lookup"><span data-stu-id="31d41-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="31d41-168">Atualização do cmdlet `Get-AzHDInsightJobOutput` para dar suporte ao acesso granular baseado em função à chave de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="31d41-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="31d41-169">Os usuários com as funções Operador do Cluster HDInsight, Colaborador ou Proprietário não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="31d41-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="31d41-170">Os usuários com apenas a função Leitor precisarão especificar o parâmetro `DefaultStorageAccountKey` explicitamente.</span><span class="sxs-lookup"><span data-stu-id="31d41-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="31d41-171">Para obter mais informações sobre essas alterações de acesso baseado em função, confira [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)</span><span class="sxs-lookup"><span data-stu-id="31d41-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](https://aka.ms/hdi-config-update)</span></span>

  #### <a name="before"></a><span data-ttu-id="31d41-172">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-173">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="31d41-174">Os usuários com apenas a função Leitor para o cmdlet Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="31d41-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="31d41-175">Antes de</span><span class="sxs-lookup"><span data-stu-id="31d41-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="31d41-176">After (após)</span><span class="sxs-lookup"><span data-stu-id="31d41-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="31d41-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="31d41-177">Az.Storage</span></span>

- <span data-ttu-id="31d41-178">Os namespaces para os tipos retornados de cmdlets de Blob, Fila e Arquivo foram alterados de `Microsoft.WindowsAzure.Storage` para `Microsoft.Azure.Storage`.</span><span class="sxs-lookup"><span data-stu-id="31d41-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="31d41-179">Embora essa não seja tecnicamente uma alteração da falha de acordo com a política de alteração da falha, ela pode exigir algumas alterações no código que usa os métodos do SDK do .NET de Armazenamento para interagir com os objetos retornados desses cmdlets.</span><span class="sxs-lookup"><span data-stu-id="31d41-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="31d41-180">Exemplo 1:  Adicionar uma mensagem a uma fila (alterar o namespace do objeto CloudQueueMessage)</span><span class="sxs-lookup"><span data-stu-id="31d41-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="31d41-181">Antes:</span><span class="sxs-lookup"><span data-stu-id="31d41-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="31d41-182">Após:</span><span class="sxs-lookup"><span data-stu-id="31d41-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="31d41-183">Exemplo 2:  Efetuar fetch de atributos de blob/arquivo com AccessCondition (alterar o namespace do objeto AccessCondition)</span><span class="sxs-lookup"><span data-stu-id="31d41-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="31d41-184">Antes:</span><span class="sxs-lookup"><span data-stu-id="31d41-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="31d41-185">Após:</span><span class="sxs-lookup"><span data-stu-id="31d41-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="31d41-186">Embora essa não seja tecnicamente uma alteração da falha, você observará diferenças de saída na propriedade Sku.Name das contas de armazenamento retornadas das alterações em `New/Get/Set-AzStorageAccount` são descritas a seguir.</span><span class="sxs-lookup"><span data-stu-id="31d41-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="31d41-187">(Após a alteração, o SkuName de saída e de entrada são alinhados.)</span><span class="sxs-lookup"><span data-stu-id="31d41-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="31d41-188">"StandardLRS" -> "Standard_LRS";</span><span class="sxs-lookup"><span data-stu-id="31d41-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="31d41-189">"StandardGRS" -> "Standard_GRS";</span><span class="sxs-lookup"><span data-stu-id="31d41-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="31d41-190">"StandardRAGRS" -> "Standard_RAGRS";</span><span class="sxs-lookup"><span data-stu-id="31d41-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="31d41-191">"StandardZRS" -> "Standard_ZRS";</span><span class="sxs-lookup"><span data-stu-id="31d41-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="31d41-192">"PremiumLRS" -> "Premium_LRS";</span><span class="sxs-lookup"><span data-stu-id="31d41-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="31d41-193">O comportamento do serviço padrão ao criar uma conta de armazenamento sem especificar um tipo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="31d41-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="31d41-194">Nas versões anteriores, quando uma conta de armazenamento era criada sem nenhum `Kind` especificado, o tipo de conta de armazenamento de `Storage` era usado na nova versão `StorageV2` é o valor `Kind` padrão.</span><span class="sxs-lookup"><span data-stu-id="31d41-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="31d41-195">Caso você precise criar uma conta de armazenamento V1 com o tipo 'Storage', adicione o parâmetro '-Kind Storage'</span><span class="sxs-lookup"><span data-stu-id="31d41-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="31d41-196">Exemplo: Criar uma conta de armazenamento (alteração de Tipo Padrão)</span><span class="sxs-lookup"><span data-stu-id="31d41-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="31d41-197">Antes:</span><span class="sxs-lookup"><span data-stu-id="31d41-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="31d41-198">Após:</span><span class="sxs-lookup"><span data-stu-id="31d41-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```
