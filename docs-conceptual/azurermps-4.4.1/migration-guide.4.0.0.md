---
title: Alterações interruptivas no Microsoft Azure PowerShell 4.0.0
description: Este guia de migração contém uma lista de alterações da falha criadas para o Azure PowerShell na versão de lançamento 4.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3e5be2d8279b28e683fbe8a03b812c658fcecf33
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243966"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="6101d-103">Alterações interruptivas no Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="6101d-103">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="6101d-104">Este documento serve como uma notificação de alterações interruptivas e como um guia de migração para consumidores dos cmdlets do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6101d-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="6101d-105">Cada seção descreve o motivo da alteração significativa e o caminho de migração de menor resistência.</span><span class="sxs-lookup"><span data-stu-id="6101d-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="6101d-106">Para obter um contexto detalhado, consulte a solicitação de pull associada a cada alteração.</span><span class="sxs-lookup"><span data-stu-id="6101d-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="6101d-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="6101d-107">Table of Contents</span></span>

- [<span data-ttu-id="6101d-108">Alterações interruptivas em cmdlets de Computação</span><span class="sxs-lookup"><span data-stu-id="6101d-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="6101d-109">Alterações interruptivas em cmdlets do Hub de Eventos</span><span class="sxs-lookup"><span data-stu-id="6101d-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="6101d-110">Alterações interruptivas em cmdlets do Insights</span><span class="sxs-lookup"><span data-stu-id="6101d-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="6101d-111">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="6101d-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="6101d-112">Alterações interruptivas em cmdlets do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6101d-112">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="6101d-113">Alterações interruptivas em cmdlets do Sql</span><span class="sxs-lookup"><span data-stu-id="6101d-113">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="6101d-114">Alterações interruptivas em cmdlets de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="6101d-114">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="6101d-115">Alterações interruptivas em cmdlets de Perfil</span><span class="sxs-lookup"><span data-stu-id="6101d-115">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="6101d-116">Alterações interruptivas em cmdlets de Computação</span><span class="sxs-lookup"><span data-stu-id="6101d-116">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="6101d-117">Os seguintes tipos de saída foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="6101d-117">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="6101d-118">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6101d-118">PSVirtualMachine</span></span>
- <span data-ttu-id="6101d-119">As principais propriedades `DataDiskNames` e `NetworkInterfaceIDs` do enésimo objeto `PSVirtualMachine` foram removidas do tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="6101d-119">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="6101d-120">Essas propriedades sempre estiveram disponíveis nas propriedades `StorageProfile` e `NetworkProfile` do objeto `PSVirtualMachine` e essa será a maneira como elas serão acessadas no futuro.</span><span class="sxs-lookup"><span data-stu-id="6101d-120">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="6101d-121">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6101d-121">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="6101d-122">Alterações interruptivas em cmdlets do Hub de Eventos</span><span class="sxs-lookup"><span data-stu-id="6101d-122">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="6101d-123">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="6101d-123">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="6101d-124">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6101d-124">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="6101d-125">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="6101d-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="6101d-126">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="6101d-126">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="6101d-127">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="6101d-127">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="6101d-128">Alterações interruptivas em cmdlets do Insights</span><span class="sxs-lookup"><span data-stu-id="6101d-128">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="6101d-129">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="6101d-129">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="6101d-130">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="6101d-130">Get-AzureRmUsage</span></span>
- <span data-ttu-id="6101d-131">Este cmdlet foi preterido.</span><span class="sxs-lookup"><span data-stu-id="6101d-131">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="6101d-132">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="6101d-132">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="6101d-133">A saída deste cmdlet mudou de uma lista com um único objeto para um único objeto. Esse objeto inclui a requestId e o código de status.</span><span class="sxs-lookup"><span data-stu-id="6101d-133">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="6101d-134">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6101d-134">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="6101d-135">Este cmdlet foi preterido.</span><span class="sxs-lookup"><span data-stu-id="6101d-135">This cmdlet has been deprecated.</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="6101d-136">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="6101d-136">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="6101d-137">Cada elemento da saída (uma lista de objetos) deste cmdlet é bidimensional, ou seja, em vez de retornar os objetos com a estrutura `{ Id, Location, Name, Tags, Properties }`, ele retornará objetos com a estrutura `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, que é todos os atributos de um Recurso do Azure mais todos os atributos de um AlertRuleResource no nível superior.</span><span class="sxs-lookup"><span data-stu-id="6101d-137">Each element of the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"

    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"

    Write-Host $rules(0).Id

    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled

    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="6101d-138">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="6101d-138">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="6101d-139">O campo `AutoscaleSettingResourceName` foi preterido, já que sempre tem o mesmo valor do que o campo `Name`.</span><span class="sxs-lookup"><span data-stu-id="6101d-139">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting

# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```

### <a name="remove-azurermlogprofile"></a><span data-ttu-id="6101d-140">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6101d-140">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="6101d-141">A saída desse cmdlet mudará de `Boolean` para um objeto que contém `RequestId` e `StatusCode`</span><span class="sxs-lookup"><span data-stu-id="6101d-141">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```

### <a name="add-azurermlogprofile"></a><span data-ttu-id="6101d-142">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="6101d-142">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="6101d-143">A saída desse cmdlet deixará de ser um objeto que inclui a requestId, o código de status e o recurso atualizado ou recém-criado</span><span class="sxs-lookup"><span data-stu-id="6101d-143">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>

```powershell-interactive
# Old
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId

```

### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="6101d-144">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="6101d-144">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="6101d-145">O comando será renomeado para `Update-AzureRmDiagnosticSettings`</span><span class="sxs-lookup"><span data-stu-id="6101d-145">The command is going to be renamed to `Update-AzureRmDiagnosticSettings`</span></span>

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="6101d-146">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="6101d-146">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="6101d-147">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="6101d-147">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="6101d-148">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6101d-148">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="6101d-149">O parâmetro `EnableBgp` foi alterado para obter um `boolean` em vez de um `string`</span><span class="sxs-lookup"><span data-stu-id="6101d-149">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="6101d-150">Alterações interruptivas em cmdlets do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6101d-150">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="6101d-151">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="6101d-151">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="6101d-152">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="6101d-152">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="6101d-153">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="6101d-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="6101d-154">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="6101d-154">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="6101d-155">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="6101d-155">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="6101d-156">Alterações interruptivas nos cmdlets do Sql</span><span class="sxs-lookup"><span data-stu-id="6101d-156">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="6101d-157">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="6101d-157">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="6101d-158">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6101d-158">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="6101d-159">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="6101d-159">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="6101d-160">O parâmetro `GracePeriodWithDataLossHour` foi renomeado para `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="6101d-160">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="6101d-161">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6101d-161">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="6101d-162">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="6101d-162">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="6101d-163">O parâmetro `GracePeriodWithDataLossHour` foi renomeado para `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="6101d-163">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="6101d-164">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6101d-164">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="6101d-165">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="6101d-165">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="6101d-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6101d-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="6101d-167">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="6101d-167">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="6101d-168">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6101d-168">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="6101d-169">O parâmetro `PartnerResourceGroupName` foi removido</span><span class="sxs-lookup"><span data-stu-id="6101d-169">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="6101d-170">O parâmetro `PartnerServerName` foi removido</span><span class="sxs-lookup"><span data-stu-id="6101d-170">`PartnerServerName` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="6101d-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6101d-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="6101d-172">O valor `Usage_Anomaly` não é mais válido para o parâmetro `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="6101d-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="6101d-173">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6101d-173">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="6101d-174">O valor `Usage_Anomaly` não é mais válido para o parâmetro `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="6101d-174">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="6101d-175">Alterações interruptivas em cmdlets do Armazenamento</span><span class="sxs-lookup"><span data-stu-id="6101d-175">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="6101d-176">As propriedades do tipo de saída a seguir foram afetadas nesta versão:</span><span class="sxs-lookup"><span data-stu-id="6101d-176">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="6101d-177">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="6101d-177">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="6101d-178">As propriedades a seguir foram removidas desse tipo (_observação_: eles ainda podem ser encontrados na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="6101d-178">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="6101d-179">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6101d-179">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`

### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="6101d-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="6101d-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="6101d-181">As propriedades a seguir foram removidas desse tipo (_observação_: elas ainda podem ser encontradas na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="6101d-181">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="6101d-182">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6101d-182">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`

### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="6101d-183">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="6101d-183">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="6101d-184">As propriedades a seguir foram removidas desse tipo (_observação_: elas ainda podem ser encontradas na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="6101d-184">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="6101d-185">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6101d-185">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`

### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="6101d-186">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="6101d-186">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="6101d-187">As propriedades a seguir foram removidas desse tipo (_observação_: elas ainda podem ser encontradas na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="6101d-187">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="6101d-188">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="6101d-188">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`

```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="6101d-189">Alterações interruptivas em cmdlets de Perfil</span><span class="sxs-lookup"><span data-stu-id="6101d-189">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="6101d-190">Os seguintes cmdlets e tipos de saída de cmdlet foram alterados nesta versão.</span><span class="sxs-lookup"><span data-stu-id="6101d-190">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="6101d-191">Alterações interruptivas de Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="6101d-191">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="6101d-192">O parâmetro ```EnvironmentName``` foi removido e substituído por ```Environment```. O parâmetro ```Environment``` agora usa uma cadeia de caracteres e não um objeto ```AzureEnvironment```</span><span class="sxs-lookup"><span data-stu-id="6101d-192">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="6101d-193">Select-AzureRmProfile foi renomeado para Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6101d-193">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="6101d-194">```Select-AzureRmProfile``` foi renomeado para ```Import-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="6101d-194">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="6101d-195">Save-AzureRmProfile foi renomeado para Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="6101d-195">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="6101d-196">```Save-AzureRmProfile``` foi renomeado para ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="6101d-196">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="6101d-197">Alterações interruptivas na saída do Tipo PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6101d-197">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="6101d-198">A propriedade ```TokenCache``` foi alterada para um tipo que implementa ```IAzureTokenCache``` em vez de um ```byte[]```</span><span class="sxs-lookup"><span data-stu-id="6101d-198">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="6101d-199">Alterações interruptivas no tipo de saída PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="6101d-199">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="6101d-200">A propriedade ```AccountType``` foi alterada para ```Type```</span><span class="sxs-lookup"><span data-stu-id="6101d-200">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="6101d-201">Alterações interruptivas no tipo de saída PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="6101d-201">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="6101d-202">A propriedade ```SubscriptionId``` foi alterada para ```Id```</span><span class="sxs-lookup"><span data-stu-id="6101d-202">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- <span data-ttu-id="6101d-203">A propriedade ```SubscriptionName``` foi alterada para ```Name```</span><span class="sxs-lookup"><span data-stu-id="6101d-203">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="6101d-204">Alterações interruptivas no tipo de saída PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="6101d-204">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="6101d-205">A propriedade ```TenantId``` foi alterada para ```Id```</span><span class="sxs-lookup"><span data-stu-id="6101d-205">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- <span data-ttu-id="6101d-206">A propriedade ```Domain``` foi alterada para ```Directory```</span><span class="sxs-lookup"><span data-stu-id="6101d-206">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
