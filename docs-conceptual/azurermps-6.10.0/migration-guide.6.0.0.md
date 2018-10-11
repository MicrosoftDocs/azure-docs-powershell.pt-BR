---
title: Alterações interruptivas no Microsoft Azure PowerShell 6.0.0
description: Este guia de migração contém uma lista de alterações da falha criadas para o Azure PowerShell na versão de lançamento 6.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 227bec0f7eb24b0941e9e21d37524b290c4b83a5
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/11/2018
ms.locfileid: "48889019"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="cf143-103">Alterações interruptivas no Microsoft Azure PowerShell 6.0.0</span><span class="sxs-lookup"><span data-stu-id="cf143-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="cf143-104">Este documento serve como uma notificação de alterações interruptivas e como um guia de migração para consumidores dos cmdlets do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf143-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="cf143-105">Cada seção descreve o motivo da alteração significativa e o caminho de migração de menor resistência.</span><span class="sxs-lookup"><span data-stu-id="cf143-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="cf143-106">Para obter um contexto detalhado, consulte a solicitação de pull associada a cada alteração.</span><span class="sxs-lookup"><span data-stu-id="cf143-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="cf143-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="cf143-107">Table of Contents</span></span>

- [<span data-ttu-id="cf143-108">Alterações da falha gerais</span><span class="sxs-lookup"><span data-stu-id="cf143-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="cf143-109">Versão mínima do PowerShell necessária aumentada para 5.0</span><span class="sxs-lookup"><span data-stu-id="cf143-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="cf143-110">Salvamento automático de contexto habilitado por padrão</span><span class="sxs-lookup"><span data-stu-id="cf143-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="cf143-111">Remoção do alias Marcas</span><span class="sxs-lookup"><span data-stu-id="cf143-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="cf143-112">Alterações de falha nos cmdlets do AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cf143-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="cf143-113">Alterações de falha nos cmdlets do AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cf143-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="cf143-114">Alterações de falha nos cmdlets do AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="cf143-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="cf143-115">Alterações de falha nos cmdlets do AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="cf143-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="cf143-116">Alterações de falha nos cmdlets do AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cf143-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="cf143-117">Alterações de falha nos cmdlets do AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cf143-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="cf143-118">Alterações de falha nos cmdlets do AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cf143-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="cf143-119">Alterações de falha nos cmdlets do AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cf143-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="cf143-120">Alterações de falha nos cmdlets do AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="cf143-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="cf143-121">Módulos removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="cf143-122">Alterações da falha gerais</span><span class="sxs-lookup"><span data-stu-id="cf143-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="cf143-123">Versão mínima do PowerShell necessária aumentada para 5.0</span><span class="sxs-lookup"><span data-stu-id="cf143-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="cf143-124">Anteriormente, o Azure PowerShell precisava de _pelo menos_ a versão 3.0 do PowerShell para executar qualquer cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf143-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="cf143-125">Mais para frente, este requisito será aumentado para a versão 5.0 do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf143-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="cf143-126">Para informações sobre a atualização para o PowerShell 5.0, consulte [esta tabela](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="cf143-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="cf143-127">Salvamento automático de contexto habilitado por padrão</span><span class="sxs-lookup"><span data-stu-id="cf143-127">Context autosave enabled by default</span></span>

<span data-ttu-id="cf143-128">O salvamento automático do contexto é o armazenamento de informações de conexão do Azure que pode ser usado entre novas e diferentes sessões do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cf143-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="cf143-129">Para obter mais informações sobre o salvamento automático de contexto, consulte [este documento](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="cf143-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="cf143-130">Anteriormente, por padrão, o salvamento automático do contexto era desabilitado, significando que as informações de autenticação do Azure do usuário não eram armazenadas entre as sessões até o `Enable-AzureRmContextAutosave` cmdlet ser executado para ativar a persistência do contexto.</span><span class="sxs-lookup"><span data-stu-id="cf143-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="cf143-131">Mais adiante, o salvamento automático do contexto será habilitado por padrão, significando que os usuários _sem nenhuma configuração de salvamento automático gravada_  terão seu contexto armazenado na próxima vez que entrarem.</span><span class="sxs-lookup"><span data-stu-id="cf143-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="cf143-132">Os usuários podem recusar essa funcionalidade usando o cmdlet `Disable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="cf143-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="cf143-133">_Observação_: os usuários que desabilitaram previamente o salvamento automático de contexto ou os usuários com salvamento automático de contexto habilitado e contextos existentes não serão afetados por essa alteração</span><span class="sxs-lookup"><span data-stu-id="cf143-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="cf143-134">Remoção do alias Marcas</span><span class="sxs-lookup"><span data-stu-id="cf143-134">Removal of Tags alias</span></span>

<span data-ttu-id="cf143-135">O alias `Tags` para o parâmetro `Tag` foi removido de vários cmdlets.</span><span class="sxs-lookup"><span data-stu-id="cf143-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="cf143-136">Abaixo está uma lista de módulos (e os cmdlets correspondentes) afetados por isso:</span><span class="sxs-lookup"><span data-stu-id="cf143-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="cf143-137">Alterações de falha nos cmdlets do AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cf143-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="cf143-138">**Diversos**</span><span class="sxs-lookup"><span data-stu-id="cf143-138">**Miscellaneous**</span></span>
- <span data-ttu-id="cf143-139">A propriedade de nome do sku aninhados em tipos `PSDisk` e `PSSnapshot` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="cf143-140">A propriedade de tipo de conta de armazenamento aninhada nos tipos `PSVirtualMachine`, `PSVirtualMachineScaleSet` e `PSImage` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="cf143-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="cf143-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="cf143-142">Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="cf143-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="cf143-144">Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="cf143-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="cf143-146">Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="cf143-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="cf143-148">O parâmetro `Managed` foi removido em favor de `Sku`</span><span class="sxs-lookup"><span data-stu-id="cf143-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="cf143-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="cf143-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="cf143-150">Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="cf143-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="cf143-152">Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="cf143-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="cf143-154">Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="cf143-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="cf143-156">Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="cf143-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="cf143-158">Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="cf143-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="cf143-160">O parâmetro `DisableWAD` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="cf143-161">Diagnóstico do Windows Azure está desabilitado por padrão</span><span class="sxs-lookup"><span data-stu-id="cf143-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="cf143-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="cf143-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="cf143-163">Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="cf143-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="cf143-165">Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="cf143-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="cf143-167">Os valores aceitos para o parâmetro `ManagedDisk` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="cf143-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="cf143-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="cf143-169">Os valores aceitos para o parâmetro `ManagedDiskStorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente</span><span class="sxs-lookup"><span data-stu-id="cf143-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="cf143-170">Alterações de falha nos cmdlets do AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cf143-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="cf143-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="cf143-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="cf143-172">Os parâmetros `PerFileThreadCount` e `ConcurrentFileCount` foram removidos.</span><span class="sxs-lookup"><span data-stu-id="cf143-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="cf143-173">Use o parâmetro `Concurrency` no futuro</span><span class="sxs-lookup"><span data-stu-id="cf143-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="cf143-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="cf143-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="cf143-175">Os parâmetros `PerFileThreadCount` e `ConcurrentFileCount` foram removidos.</span><span class="sxs-lookup"><span data-stu-id="cf143-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="cf143-176">Use o parâmetro `Concurrency` no futuro</span><span class="sxs-lookup"><span data-stu-id="cf143-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="cf143-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="cf143-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="cf143-178">O parâmetro `Clean` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="cf143-179">Alterações de falha nos cmdlets do AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="cf143-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="cf143-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="cf143-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="cf143-181">O parâmetro `Force` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="cf143-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="cf143-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="cf143-183">O parâmetro `Force` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="cf143-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="cf143-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="cf143-185">O parâmetro `Force` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="cf143-186">Alterações de falha nos cmdlets do AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="cf143-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="cf143-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="cf143-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="cf143-188">Os aliases dos parâmetros `AutoscaleProfiles` e `Notifications` foram removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="cf143-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="cf143-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="cf143-190">Os aliases dos parâmetros `Categories` e `Locations` foram removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="cf143-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="cf143-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="cf143-192">O alias do parâmetro `Actions` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="cf143-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="cf143-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="cf143-194">O alias do parâmetro `Actions` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="cf143-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="cf143-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="cf143-196">Os aliases dos parâmetros `MaxRecords` e `MaxEvents` foram removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="cf143-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="cf143-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="cf143-198">O alias do parâmetro `MetricNames` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="cf143-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="cf143-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="cf143-200">Os aliases dos parâmetros `CustomEmails` e `SendToServiceOwners` foram removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="cf143-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="cf143-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="cf143-202">O alias do parâmetro `Properties` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="cf143-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="cf143-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="cf143-204">Os aliases dos parâmetros `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` e `Webhooks` foram removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="cf143-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="cf143-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="cf143-206">Os aliases dos parâmetros `Rules`, `ScheduleDays`, `ScheduleHours` e `ScheduleMinutes` foram removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="cf143-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="cf143-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="cf143-208">O alias do parâmetro `Properties` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="cf143-209">Alterações de falha nos cmdlets do AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cf143-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="cf143-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="cf143-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="cf143-211">O parâmetro `CertificatePolicy` se tornou obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cf143-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="cf143-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="cf143-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="cf143-213">O cmdlet não aceita parâmetros individuais que compõem o token de acesso. Em vez disso, o cmdlet substitui parâmetros explícitos de token, como `Service` ou `Permissions`, com um parâmetro `TemplateUri` genérico, correspondente a um token de acesso de exemplo definido em outro lugar (supostamente usando cmdlets do PowerShell de armazenamento ou composto manualmente, de acordo com a documentação de armazenamento). O cmdlet retém o parâmetro `ValidityPeriod`.</span><span class="sxs-lookup"><span data-stu-id="cf143-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="cf143-214">Para obter mais informações sobre a composição de tokens de acesso compartilhados para o Armazenamento do Azure, consulte as páginas de documentação, respectivamente:</span><span class="sxs-lookup"><span data-stu-id="cf143-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="cf143-215">[Criação de um serviço SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)</span><span class="sxs-lookup"><span data-stu-id="cf143-215">[Constructing a Service SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="cf143-216">[Criação de uma conta SAS] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="cf143-216">[Constructing an Account SAS] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="cf143-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="cf143-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="cf143-218">O parâmetro `IssuerProvider` se tornou obrigatório.</span><span class="sxs-lookup"><span data-stu-id="cf143-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="cf143-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="cf143-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="cf143-220">A saída desse cmdlet mudou de `CertificateBundle` para `PSKeyVaultCertificate`.</span><span class="sxs-lookup"><span data-stu-id="cf143-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="cf143-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="cf143-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="cf143-222">`ResourceGroupName` foi removido do conjunto de parâmetros `InputObject` e, em vez disso, é obtido no `InputObject` da propriedade do parâmetro `ResourceId`.</span><span class="sxs-lookup"><span data-stu-id="cf143-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="cf143-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="cf143-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="cf143-224">A permissão `all` foi removida do `PermissionsToKeys`, `PermissionsToSecrets`, e `PermissionsToCertificates`.</span><span class="sxs-lookup"><span data-stu-id="cf143-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="cf143-225">**Geral**</span><span class="sxs-lookup"><span data-stu-id="cf143-225">**General**</span></span>
- <span data-ttu-id="cf143-226">A propriedade `ValueFromPipelineByPropertyName` foi removida de todos os cmdlets nos quais foram habilitados o direcionamento por `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="cf143-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="cf143-227">Os cmdlets afetados são:</span><span class="sxs-lookup"><span data-stu-id="cf143-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="cf143-228">Os níveis `ConfirmImpact` foram removidos de todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="cf143-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="cf143-229">Os cmdlets afetados são:</span><span class="sxs-lookup"><span data-stu-id="cf143-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="cf143-230">O `IKeyVaultDataServiceClient` foi atualizado para que todas as operações de Certificado retornem PSTypes em vez de tipos SDK.</span><span class="sxs-lookup"><span data-stu-id="cf143-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="cf143-231">Isso inclui:</span><span class="sxs-lookup"><span data-stu-id="cf143-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="cf143-232">Alterações de falha nos cmdlets do AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cf143-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="cf143-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="cf143-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="cf143-234">O parâmetro `ProbeEnabled` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="cf143-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="cf143-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="cf143-236">O alias do parâmetro `AlloowGatewayTransit` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="cf143-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="cf143-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="cf143-238">O parâmetro `ProbeEnabled` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="cf143-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="cf143-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="cf143-240">O parâmetro `ProbeEnabled` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="cf143-241">Alterações de falha nos cmdlets do AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cf143-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="cf143-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="cf143-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="cf143-243">Os parâmetros `Subnet` e `VirtualNetwork` foram removidos em favor de `SubnetId`</span><span class="sxs-lookup"><span data-stu-id="cf143-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="cf143-244">O parâmetro `RedisVersion` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="cf143-245">O parâmetro `MaxMemoryPolicy` foi removido em favor de `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="cf143-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="cf143-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="cf143-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="cf143-247">O parâmetro `MaxMemoryPolicy` foi removido em favor de `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="cf143-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="cf143-248">Alterações de falha nos cmdlets do AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cf143-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="cf143-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="cf143-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="cf143-250">Esse cmdlet foi removido e a funcionalidade foi movida para `Get-AzureRmResource`</span><span class="sxs-lookup"><span data-stu-id="cf143-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="cf143-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="cf143-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="cf143-252">Esse cmdlet foi removido e a funcionalidade foi movida para `Get-AzureRmResourceGroup`</span><span class="sxs-lookup"><span data-stu-id="cf143-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="cf143-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="cf143-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="cf143-254">O parâmetro `AtScopeAndBelow` foi removido.</span><span class="sxs-lookup"><span data-stu-id="cf143-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="cf143-255">Alterações de falha nos cmdlets do AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="cf143-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="cf143-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="cf143-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="cf143-257">O parâmetro `EnableEncryptionService` foi removido</span><span class="sxs-lookup"><span data-stu-id="cf143-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="cf143-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="cf143-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="cf143-259">Os parâmetros `EnableEncryptionService` e `DisableEncryptionService` foram removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="cf143-260">Módulos removidos</span><span class="sxs-lookup"><span data-stu-id="cf143-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="cf143-261">O serviço de Ferramentas de Gerenciamento de Servidor se tornou [obsoleto no ano passado](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)e, como resultado, o módulo correspondente para SMT, `AzureRM.ServerManagement`, foi removido do `AzureRM` e parará de enviar no futuro.</span><span class="sxs-lookup"><span data-stu-id="cf143-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="cf143-262">O módulo `AzureRM.SiteRecovery` está sendo substituído pelo `AzureRM.RecoveryServices.SiteRecovery`, que é um superconjunto funcional do módulo `AzureRM.SiteRecovery` e inclui um novo conjunto de cmdlets equivalentes.</span><span class="sxs-lookup"><span data-stu-id="cf143-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="cf143-263">A lista completa de mapeamentos de antigos para novos cmdlets pode ser encontrada abaixo:</span><span class="sxs-lookup"><span data-stu-id="cf143-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="cf143-264">Cmdlet preterido</span><span class="sxs-lookup"><span data-stu-id="cf143-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="cf143-265">Cmdlet equivalente</span><span class="sxs-lookup"><span data-stu-id="cf143-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="cf143-266">Aliases</span><span class="sxs-lookup"><span data-stu-id="cf143-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
