# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="82e68-101">Alterações interruptivas no Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="82e68-101">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

<span data-ttu-id="82e68-102">Este documento serve como uma notificação de alterações interruptivas e como um guia de migração para consumidores dos cmdlets do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="82e68-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="82e68-103">Cada seção descreve o motivo da alteração significativa e o caminho de migração de menor resistência.</span><span class="sxs-lookup"><span data-stu-id="82e68-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="82e68-104">Para obter um contexto detalhado, consulte a solicitação de pull associada a cada alteração.</span><span class="sxs-lookup"><span data-stu-id="82e68-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="82e68-105">Sumário</span><span class="sxs-lookup"><span data-stu-id="82e68-105">Table of Contents</span></span>

- [<span data-ttu-id="82e68-106">Alterações interruptivas em cmdlets de Computação</span><span class="sxs-lookup"><span data-stu-id="82e68-106">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="82e68-107">Alterações interruptivas em cmdlets do Hub de Eventos</span><span class="sxs-lookup"><span data-stu-id="82e68-107">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="82e68-108">Alterações interruptivas em cmdlets do Insights</span><span class="sxs-lookup"><span data-stu-id="82e68-108">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="82e68-109">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="82e68-109">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="82e68-110">Alterações interruptivas em cmdlets do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82e68-110">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="82e68-111">Alterações interruptivas em cmdlets do Sql</span><span class="sxs-lookup"><span data-stu-id="82e68-111">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="82e68-112">Alterações interruptivas em cmdlets de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="82e68-112">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="82e68-113">Alterações interruptivas em cmdlets de Perfil</span><span class="sxs-lookup"><span data-stu-id="82e68-113">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="82e68-114">Alterações interruptivas em cmdlets de Computação</span><span class="sxs-lookup"><span data-stu-id="82e68-114">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="82e68-115">Os seguintes tipos de saída foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="82e68-115">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="82e68-116">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="82e68-116">PSVirtualMachine</span></span>
- <span data-ttu-id="82e68-117">As principais propriedades `DataDiskNames` e `NetworkInterfaceIDs` do enésimo objeto `PSVirtualMachine` foram removidas do tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="82e68-117">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="82e68-118">Essas propriedades sempre estiveram disponíveis nas propriedades `StorageProfile` e `NetworkProfile` do objeto `PSVirtualMachine` e essa será a maneira como elas serão acessadas no futuro.</span><span class="sxs-lookup"><span data-stu-id="82e68-118">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="82e68-119">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="82e68-119">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="82e68-120">Alterações interruptivas em cmdlets do Hub de Eventos</span><span class="sxs-lookup"><span data-stu-id="82e68-120">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="82e68-121">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="82e68-121">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="82e68-122">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="82e68-122">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="82e68-123">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="82e68-123">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="82e68-124">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="82e68-124">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="82e68-125">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="82e68-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="82e68-126">Alterações interruptivas em cmdlets do Insights</span><span class="sxs-lookup"><span data-stu-id="82e68-126">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="82e68-127">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="82e68-127">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="82e68-128">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="82e68-128">Get-AzureRmUsage</span></span>
- <span data-ttu-id="82e68-129">Este cmdlet foi preterido.</span><span class="sxs-lookup"><span data-stu-id="82e68-129">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="82e68-130">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="82e68-130">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="82e68-131">A saída deste cmdlet mudou de uma lista com um único objeto para um único objeto. Esse objeto inclui a requestId e o código de status.</span><span class="sxs-lookup"><span data-stu-id="82e68-131">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell
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
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="82e68-132">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="82e68-132">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="82e68-133">Este cmdlet foi preterido.</span><span class="sxs-lookup"><span data-stu-id="82e68-133">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="82e68-134">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="82e68-134">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="82e68-135">Cada elemento da saída (uma lista de objetos) deste cmdlet é bidimensional, ou seja, em vez de retornar os objetos com a estrutura `{ Id, Location, Name, Tags, Properties }`, ele retornará objetos com a estrutura `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, que é todos os atributos de um Recurso do Azure mais todos os atributos de um AlertRuleResource no nível superior.</span><span class="sxs-lookup"><span data-stu-id="82e68-135">Each element of the the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell
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
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="82e68-136">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="82e68-136">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="82e68-137">O campo `AutoscaleSettingResourceName` foi preterido, já que sempre tem o mesmo valor do que o campo `Name`.</span><span class="sxs-lookup"><span data-stu-id="82e68-137">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell
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
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="82e68-138">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="82e68-138">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="82e68-139">A saída desse cmdlet mudará de `Boolean` para um objeto que contém `RequestId` e `StatusCode`</span><span class="sxs-lookup"><span data-stu-id="82e68-139">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell
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
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="82e68-140">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="82e68-140">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="82e68-141">A saída desse cmdlet deixará de ser um objeto que inclui a requestId, o código de status e o recurso atualizado ou recém-criado</span><span class="sxs-lookup"><span data-stu-id="82e68-141">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="82e68-142">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="82e68-142">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="82e68-143">O comando será renomeado para `Update-AzureRmDiagnsoticSettings`</span><span class="sxs-lookup"><span data-stu-id="82e68-143">The command is going to be renamed to `Update-AzureRmDiagnsoticSettings`</span></span>

```powershell
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="82e68-144">Alterações interruptivas em cmdlets de Rede</span><span class="sxs-lookup"><span data-stu-id="82e68-144">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="82e68-145">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="82e68-145">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="82e68-146">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="82e68-146">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="82e68-147">O parâmetro `EnableBgp` foi alterado para obter um `boolean` em vez de um `string`</span><span class="sxs-lookup"><span data-stu-id="82e68-147">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="82e68-148">Alterações interruptivas em cmdlets do ServiceBus</span><span class="sxs-lookup"><span data-stu-id="82e68-148">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="82e68-149">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="82e68-149">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="82e68-150">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="82e68-150">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="82e68-151">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="82e68-151">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="82e68-152">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="82e68-152">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="82e68-153">A propriedade `ResourceGroupName` foi removida do tipo de saída `NamespaceAttributes`</span><span class="sxs-lookup"><span data-stu-id="82e68-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="82e68-154">Alterações interruptivas nos cmdlets do Sql</span><span class="sxs-lookup"><span data-stu-id="82e68-154">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="82e68-155">Os seguintes cmdlets foram afetados nesta versão:</span><span class="sxs-lookup"><span data-stu-id="82e68-155">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="82e68-156">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82e68-156">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="82e68-157">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="82e68-157">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="82e68-158">O parâmetro `GracePeriodWithDataLossHour` foi renomeado para `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="82e68-158">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="82e68-159">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82e68-159">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="82e68-160">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="82e68-160">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="82e68-161">O parâmetro `GracePeriodWithDataLossHour` foi renomeado para `GracePeriodWithDataLossHours`</span><span class="sxs-lookup"><span data-stu-id="82e68-161">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="82e68-162">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82e68-162">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="82e68-163">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="82e68-163">`Tag` parameter has been removed</span></span>

```powershell
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="82e68-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82e68-164">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="82e68-165">O parâmetro `Tag` foi removido</span><span class="sxs-lookup"><span data-stu-id="82e68-165">`Tag` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="82e68-166">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="82e68-166">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="82e68-167">O parâmetro `PartnerResourceGroupName` foi removido</span><span class="sxs-lookup"><span data-stu-id="82e68-167">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="82e68-168">O parâmetro `PartnerServerName` foi removido</span><span class="sxs-lookup"><span data-stu-id="82e68-168">`PartnerServerName` parameter has been removed</span></span>

```powershell
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="82e68-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="82e68-169">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="82e68-170">O valor `Usage_Anomaly` não é mais válido para o parâmetro `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="82e68-170">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="82e68-171">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="82e68-171">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="82e68-172">O valor `Usage_Anomaly` não é mais válido para o parâmetro `ExcludedDetectionType`</span><span class="sxs-lookup"><span data-stu-id="82e68-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="82e68-173">Alterações interruptivas em cmdlets do Armazenamento</span><span class="sxs-lookup"><span data-stu-id="82e68-173">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="82e68-174">As propriedades do tipo de saída a seguir foram afetadas nesta versão:</span><span class="sxs-lookup"><span data-stu-id="82e68-174">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="82e68-175">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="82e68-175">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="82e68-176">As propriedades a seguir foram removidas desse tipo (_observação_: eles ainda podem ser encontrados na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="82e68-176">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="82e68-177">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="82e68-177">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="82e68-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="82e68-178">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="82e68-179">As propriedades a seguir foram removidas desse tipo (_observação_: elas ainda podem ser encontradas na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="82e68-179">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="82e68-180">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="82e68-180">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="82e68-181">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="82e68-181">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="82e68-182">As propriedades a seguir foram removidas desse tipo (_observação_: elas ainda podem ser encontradas na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="82e68-182">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="82e68-183">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="82e68-183">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="82e68-184">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="82e68-184">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="82e68-185">As propriedades a seguir foram removidas desse tipo (_observação_: elas ainda podem ser encontradas na propriedade `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="82e68-185">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="82e68-186">Essa alteração afeta os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="82e68-186">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell
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

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="82e68-187">Alterações interruptivas em cmdlets de Perfil</span><span class="sxs-lookup"><span data-stu-id="82e68-187">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="82e68-188">Os seguintes cmdlets e tipos de saída de cmdlet foram alterados nesta versão.</span><span class="sxs-lookup"><span data-stu-id="82e68-188">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="82e68-189">Alterações interruptivas de Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="82e68-189">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="82e68-190">O parâmetro ```EnvironmentName``` foi removido e substituído por ```Environment```. O parâmetro ```Environment``` agora usa uma cadeia de caracteres e não um objeto ```AzureEnvironment```</span><span class="sxs-lookup"><span data-stu-id="82e68-190">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="82e68-191">Select-AzureRmProfile foi renomeado para Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="82e68-191">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="82e68-192">```Select-AzureRmProfile``` foi renomeado para ```Import-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="82e68-192">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="82e68-193">Save-AzureRmProfile foi renomeado para Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="82e68-193">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="82e68-194">```Save-AzureRmProfile``` foi renomeado para ```Save-AzureRmContext```</span><span class="sxs-lookup"><span data-stu-id="82e68-194">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="82e68-195">Alterações interruptivas na saída do Tipo PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="82e68-195">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="82e68-196">A propriedade ```TokenCache``` foi alterada para um tipo que implementa ```IAzureTokenCache``` em vez de um ```byte[]```</span><span class="sxs-lookup"><span data-stu-id="82e68-196">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="82e68-197">Alterações interruptivas no tipo de saída PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="82e68-197">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="82e68-198">A propriedade ```AccountType``` foi alterada para ```Type```</span><span class="sxs-lookup"><span data-stu-id="82e68-198">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="82e68-199">Alterações interruptivas no tipo de saída PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="82e68-199">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="82e68-200">A propriedade ```SubscriptionId``` foi alterada para ```Id```</span><span class="sxs-lookup"><span data-stu-id="82e68-200">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell
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

- <span data-ttu-id="82e68-201">A propriedade ```SubscriptionName``` foi alterada para ```Name```</span><span class="sxs-lookup"><span data-stu-id="82e68-201">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell
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

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="82e68-202">Alterações interruptivas no tipo de saída PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="82e68-202">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="82e68-203">A propriedade ```TenantId``` foi alterada para ```Id```</span><span class="sxs-lookup"><span data-stu-id="82e68-203">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell
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

- <span data-ttu-id="82e68-204">A propriedade ```Domain``` foi alterada para ```Directory```</span><span class="sxs-lookup"><span data-stu-id="82e68-204">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
