---
title: Alterações interruptivas no Microsoft Azure PowerShell 5.0.0
description: Este guia de migração contém uma lista de alterações da falha criadas para o Azure PowerShell na versão de lançamento 5.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: f8dc413a91876e53e62d25cc38ac3b3ef6afda8e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534577"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="8d99c-103">Alterações interruptivas no Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="8d99c-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="8d99c-104">Este documento serve como uma notificação de alterações interruptivas e como um guia de migração para consumidores dos cmdlets do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d99c-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="8d99c-105">Cada seção descreve o motivo da alteração significativa e o caminho de migração de menor resistência.</span><span class="sxs-lookup"><span data-stu-id="8d99c-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="8d99c-106">Para obter um contexto detalhado, consulte a solicitação de pull associada a cada alteração.</span><span class="sxs-lookup"><span data-stu-id="8d99c-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="8d99c-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="8d99c-107">Table of Contents</span></span>

- [<span data-ttu-id="8d99c-108">Alterações interruptivas em cmdlets de ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d99c-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="8d99c-109">Alterações interruptivas em cmdlets do Lote</span><span class="sxs-lookup"><span data-stu-id="8d99c-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="8d99c-110">Alterações interruptivas em cmdlets de Computação</span><span class="sxs-lookup"><span data-stu-id="8d99c-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="8d99c-111">Alterações interruptivas em cmdlets do Hub de Eventos</span><span class="sxs-lookup"><span data-stu-id="8d99c-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="8d99c-112">Alterações interruptivas em cmdlets do Insights</span><span class="sxs-lookup"><span data-stu-id="8d99c-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="8d99c-113">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="8d99c-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="8d99c-114">Alterações interruptivas em cmdlets de Recursos</span><span class="sxs-lookup"><span data-stu-id="8d99c-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="8d99c-115">Alterações interruptivas em mdlets do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d99c-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="8d99c-116">Alterações interruptivas em cmdlets de ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8d99c-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="8d99c-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="8d99c-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="8d99c-118">Os parâmetros "UserName" e "Password" foram substituídos por uma PSCredential</span><span class="sxs-lookup"><span data-stu-id="8d99c-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="8d99c-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="8d99c-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="8d99c-120">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="8d99c-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="8d99c-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="8d99c-122">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="8d99c-123">Alterações interruptivas nos cmdlets do Lote</span><span class="sxs-lookup"><span data-stu-id="8d99c-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="8d99c-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="8d99c-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="8d99c-125">O parâmetro `Password` foi substituído por uma cadeia de caracteres Secure</span><span class="sxs-lookup"><span data-stu-id="8d99c-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="8d99c-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="8d99c-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="8d99c-127">O parâmetro `Password` foi substituído por uma cadeia de caracteres Secure</span><span class="sxs-lookup"><span data-stu-id="8d99c-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="8d99c-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="8d99c-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="8d99c-129">O parâmetro `Password` foi substituído por uma cadeia de caracteres Secure</span><span class="sxs-lookup"><span data-stu-id="8d99c-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="8d99c-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="8d99c-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="8d99c-131">A opção `RunElevated` foi removida e substituída por `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="8d99c-132">Isso também afeta a propriedade `RunElevated` em `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="8d99c-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="8d99c-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="8d99c-134">O construtor `PSMultiInstanceSettings` não precisa mais de um parâmetro `numberOfInstances` obrigatório, mas obtém um parâmetro `coordinationCommandLine` obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8d99c-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="8d99c-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="8d99c-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="8d99c-136">A propriedade `RunElevated` foi removida em `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="8d99c-137">A propriedade `UserIdentity` foi adicionada para substituir `RunElevated`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="8d99c-138">Isso também afeta a propriedade `RunElevated` em `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="8d99c-139">**Vários tipos**</span><span class="sxs-lookup"><span data-stu-id="8d99c-139">**Multiple types**</span></span>

- <span data-ttu-id="8d99c-140">A propriedade `SchedulingError` foi renomeada em `PSExitConditions` para `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="8d99c-141">**Vários tipos**</span><span class="sxs-lookup"><span data-stu-id="8d99c-141">**Multiple types**</span></span>

- <span data-ttu-id="8d99c-142">A propriedade `SchedulingError` foi renomeada em `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` e `PSTaskExecutionInformation` para `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="8d99c-143">`FailureInformation` é retornado sempre que há uma falha de tarefa.</span><span class="sxs-lookup"><span data-stu-id="8d99c-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="8d99c-144">Isso inclui todos os casos de erro de agendamento anteriores, bem como códigos de saída de tarefa diferentes de zero e falhas de carregamento de arquivo do novo recurso de arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="8d99c-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="8d99c-145">Isso é estruturado da mesma forma como antes e, portanto, nenhuma alteração de código será necessária ao usar esse tipo.</span><span class="sxs-lookup"><span data-stu-id="8d99c-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="8d99c-146">Isso também tem impacto sobre: Get-AzureBatchPool, Get-AzureBatchSubtask e Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="8d99c-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="8d99c-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="8d99c-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="8d99c-148">`TargetDedicated` foi removido e substituído por `TargetDedicatedComputeNodes` e `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="8d99c-149">`TargetDedicatedComputeNodes` tem um alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="8d99c-150">Isso também tem impacto sobre: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="8d99c-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="8d99c-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="8d99c-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="8d99c-152">As propriedades `TargetDedicated` e `CurrentDedicated` foram renomeadas em `PSCloudPool` para `TargetDedicatedComputeNodes` e `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="8d99c-153">**Tipo PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="8d99c-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="8d99c-154">`ResizeError` foi renomeado para `ResizeErrors` em `PSCloudPool` e agora é uma coleção.</span><span class="sxs-lookup"><span data-stu-id="8d99c-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="8d99c-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="8d99c-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="8d99c-156">A propriedade `TargetDedicated` foi renomeada em `PSPoolSpecification` para `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="8d99c-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="8d99c-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="8d99c-158">`Name` foi removido e substituído por `Path`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="8d99c-159">`Path` tem um alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="8d99c-160">Isso também tem impacto sobre: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="8d99c-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="8d99c-161">Tipo **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="8d99c-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="8d99c-162">A propriedade `Name` foi renomeada em `PSNodeFile` para `Path`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="8d99c-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="8d99c-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="8d99c-164">As propriedades `PreviousState` e `State` de `PSSubtaskInformation` não são mais do tipo `TaskState`, mas do tipo `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="8d99c-165">Ao contrário de `TaskState`, `SubtaskState` não tem nenhum valor `Active`, pois subtarefas não podem ficar em um estado `Active`.</span><span class="sxs-lookup"><span data-stu-id="8d99c-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="8d99c-166">Alterações interruptivas em cmdlets de Computação</span><span class="sxs-lookup"><span data-stu-id="8d99c-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="8d99c-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="8d99c-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="8d99c-168">Os parâmetros "UserName" e "Password" foram substituídos por uma PSCredential</span><span class="sxs-lookup"><span data-stu-id="8d99c-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="8d99c-169">Alterações interruptivas em cmdlets do Hub de Eventos</span><span class="sxs-lookup"><span data-stu-id="8d99c-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-171">O cmdlet 'New-AzureRmEventHubNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-172">Use o cmdlet 'New-AzureRmEventHubAuthorizationRule'</span><span class="sxs-lookup"><span data-stu-id="8d99c-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-174">O cmdlet 'Get-AzureRmEventHubNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-175">Use o cmdlet 'Get-AzureRmEventHubAuthorizationRule'</span><span class="sxs-lookup"><span data-stu-id="8d99c-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-177">O cmdlet 'Set-AzureRmEventHubNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-178">Use o cmdlet 'Set-AzureRmEventHubAuthorizationRule'</span><span class="sxs-lookup"><span data-stu-id="8d99c-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-180">O cmdlet 'Remove-AzureRmEventHubNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-181">Use o cmdlet 'Remove-AzureRmEventHubAuthorizationRule'</span><span class="sxs-lookup"><span data-stu-id="8d99c-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="8d99c-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="8d99c-183">O cmdlet 'New-AzureRmEventHubNamespaceKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-184">Use o cmdlet 'New-AzureRmEventHubKey'</span><span class="sxs-lookup"><span data-stu-id="8d99c-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="8d99c-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="8d99c-186">O cmdlet 'Get-AzureRmEventHubNamespaceKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-187">Use o cmdlet 'Get-AzureRmEventHubKey'</span><span class="sxs-lookup"><span data-stu-id="8d99c-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="8d99c-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="8d99c-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="8d99c-189">As propriedades 'Status' e 'Enabled' de NamespceAttributes serão removidas.</span><span class="sxs-lookup"><span data-stu-id="8d99c-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="8d99c-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="8d99c-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="8d99c-191">As propriedades 'Status' e 'Enabled' de NamespceAttributes serão removidas.</span><span class="sxs-lookup"><span data-stu-id="8d99c-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="8d99c-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="8d99c-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="8d99c-193">As propriedades 'Status' e 'Enabled' de NamespceAttributes serão removidas.</span><span class="sxs-lookup"><span data-stu-id="8d99c-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="8d99c-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="8d99c-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="8d99c-195">A propriedade 'EventHubPath' de ConsumerGroupAttributes será removida.</span><span class="sxs-lookup"><span data-stu-id="8d99c-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="8d99c-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="8d99c-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="8d99c-197">A propriedade 'EventHubPath' de ConsumerGroupAttributes será removida.</span><span class="sxs-lookup"><span data-stu-id="8d99c-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="8d99c-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="8d99c-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="8d99c-199">A propriedade 'EventHubPath' de ConsumerGroupAttributes será removida.</span><span class="sxs-lookup"><span data-stu-id="8d99c-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="8d99c-200">Alterações interruptivas em cmdlets do Insights</span><span class="sxs-lookup"><span data-stu-id="8d99c-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="8d99c-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="8d99c-202">O cmdlet **Add-AzureRMLogAlertRule** foi preterido</span><span class="sxs-lookup"><span data-stu-id="8d99c-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="8d99c-203">Depois de 1º de outubro, o uso desse cmdlet não terá qualquer efeito, já que essa funcionalidade está sendo transferida para os Alertas de Log de Atividade.</span><span class="sxs-lookup"><span data-stu-id="8d99c-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="8d99c-204">Consulte https://aka.ms/migratemealerts para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8d99c-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="8d99c-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="8d99c-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="8d99c-206">O cmdlet **Get-AzureRMUsage** foi preterido</span><span class="sxs-lookup"><span data-stu-id="8d99c-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="8d99c-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="8d99c-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="8d99c-208">Alteração de saída: o campo EventChannels do objeto EventData (retornado por esses cmdlets) está sendo preterido por estar retornando um valor constante (Admin, Operation).</span><span class="sxs-lookup"><span data-stu-id="8d99c-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="8d99c-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="8d99c-210">Alteração de saída: a saída desse cmdlet será nivelada, ou seja, eliminará o campo de propriedades para melhorar a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d99c-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="8d99c-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="8d99c-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="8d99c-212">Alteração de saída: o campo AutoscaleSettingResourceName será preterido porque é sempre igual ao campo Name.</span><span class="sxs-lookup"><span data-stu-id="8d99c-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="8d99c-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="8d99c-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="8d99c-214">Alteração de saída: o tipo da saída será alterado para retornar um único objeto que contém a ID da solicitação e o código de status.</span><span class="sxs-lookup"><span data-stu-id="8d99c-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="8d99c-215">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="8d99c-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="8d99c-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="8d99c-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="8d99c-217">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="8d99c-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="8d99c-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="8d99c-219">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="8d99c-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="8d99c-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="8d99c-221">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="8d99c-222">Alterações interruptivas em cmdlets de Recursos</span><span class="sxs-lookup"><span data-stu-id="8d99c-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="8d99c-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="8d99c-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="8d99c-224">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="8d99c-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="8d99c-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="8d99c-226">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="8d99c-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="8d99c-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="8d99c-228">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="8d99c-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="8d99c-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="8d99c-230">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="8d99c-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="8d99c-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="8d99c-232">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="8d99c-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="8d99c-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="8d99c-234">O parâmetro "Password" foi substituído por uma SecureString</span><span class="sxs-lookup"><span data-stu-id="8d99c-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="8d99c-235">Alterações interruptivas em cmdlets do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8d99c-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8d99c-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-237">O cmdlet 'Get-AzureRmServiceBusTopicAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-238">Use o cmdlet 'Get-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="8d99c-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="8d99c-240">O cmdlet 'Get-AzureRmServiceBusTopicKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-241">Use o cmdlet 'Get-AzureRmServiceBusKey'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8d99c-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-243">O cmdlet 'New-AzureRmServiceBusTopicAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-244">Use o cmdlet 'New-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="8d99c-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="8d99c-246">O cmdlet 'New-AzureRmServiceBusTopicKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-247">Use o cmdlet 'New-AzureRmServiceBusKey'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8d99c-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-249">O cmdlet 'Remove-AzureRmServiceBusTopicAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-250">Use o cmdlet 'Remove-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="8d99c-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-252">O cmdlet 'Set-AzureRmServiceBusTopicAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-253">Use o cmdlet 'Set-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="8d99c-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="8d99c-255">O cmdlet 'New-AzureRmServiceBusNamespaceKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-256">Use o cmdlet 'New-AzureRmServiceBusKey'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8d99c-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-258">O cmdlet 'Get-AzureRmServiceBusQueueAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-259">Use o cmdlet 'Get-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="8d99c-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="8d99c-261">O cmdlet 'Get-AzureRmServiceBusQueueKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-262">Use o cmdlet 'Get-AzureRmServiceBusKey'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8d99c-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-264">O cmdlet 'New-AzureRmServiceBusQueueAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-265">Use o cmdlet 'New-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="8d99c-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="8d99c-267">O cmdlet 'New-AzureRmServiceBusQueueKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-268">Use o cmdlet 'New-AzureRmServiceBusKey'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8d99c-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-270">O cmdlet 'Remove-AzureRmServiceBusQueueAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-271">Use o cmdlet 'GRemove AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="8d99c-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-273">O cmdlet 'Set-AzureRmServiceBusQueueAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-274">Use o cmdlet 'Set-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-276">O cmdlet 'Get-AzureRmServiceBusNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-277">Use o cmdlet 'Get-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="8d99c-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="8d99c-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="8d99c-279">O cmdlet 'Get-AzureRmServiceBusNamespaceKey' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-280">Use o cmdlet 'Get-AzureRmServiceBusKey'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-282">O cmdlet 'New-AzureRmServiceBusNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-283">Use o cmdlet 'New-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-285">O cmdlet 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-286">Use o cmdlet 'Remove-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="8d99c-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="8d99c-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="8d99c-288">O cmdlet 'Set-AzureRmServiceBusNamespaceAuthorizationRule' foi removido.</span><span class="sxs-lookup"><span data-stu-id="8d99c-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="8d99c-289">Use o cmdlet 'Set-AzureRmServiceBusAuthorizationRule'.</span><span class="sxs-lookup"><span data-stu-id="8d99c-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="8d99c-290">**Tipo NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="8d99c-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="8d99c-291">As propriedades a seguir foram removidas</span><span class="sxs-lookup"><span data-stu-id="8d99c-291">The following properties have been removed</span></span>
    - <span data-ttu-id="8d99c-292">habilitado</span><span class="sxs-lookup"><span data-stu-id="8d99c-292">Enabled</span></span>
    - <span data-ttu-id="8d99c-293">Status</span><span class="sxs-lookup"><span data-stu-id="8d99c-293">Status</span></span>
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="8d99c-294">**Tipo QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="8d99c-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="8d99c-295">As seguintes propriedades foram marcadas como obsoletas:</span><span class="sxs-lookup"><span data-stu-id="8d99c-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="8d99c-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="8d99c-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="8d99c-297">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8d99c-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="8d99c-298">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="8d99c-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="8d99c-299">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="8d99c-299">SupportOrdering</span></span>

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="8d99c-300">**Tipo TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="8d99c-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="8d99c-301">As seguintes propriedades foram marcadas como obsoletas:</span><span class="sxs-lookup"><span data-stu-id="8d99c-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="8d99c-302">Location</span><span class="sxs-lookup"><span data-stu-id="8d99c-302">Location</span></span>
    - <span data-ttu-id="8d99c-303">IsExpress</span><span class="sxs-lookup"><span data-stu-id="8d99c-303">IsExpress</span></span>
    - <span data-ttu-id="8d99c-304">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="8d99c-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="8d99c-305">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="8d99c-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="8d99c-306">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="8d99c-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="8d99c-307">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8d99c-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="8d99c-308">**Tipo SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="8d99c-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="8d99c-309">As seguintes propriedades foram marcadas como obsoletas</span><span class="sxs-lookup"><span data-stu-id="8d99c-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="8d99c-310">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="8d99c-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="8d99c-311">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8d99c-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="8d99c-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="8d99c-312">IsReadOnly</span></span>
    - <span data-ttu-id="8d99c-313">Location</span><span class="sxs-lookup"><span data-stu-id="8d99c-313">Location</span></span>
   
```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```