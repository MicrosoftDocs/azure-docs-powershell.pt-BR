---
ms.openlocfilehash: 636fd0432d421f74fa74f3275abbc31ec5dc0b5c
ms.sourcegitcommit: 31f4facf815c2e25dc44e2fde0e1d2bd690bfc54
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/20/2020
ms.locfileid: "83688519"
---
# <a name="migration-guide-for-az-410"></a>Guia de migração para o Az 4.1.0

Este documento descreve as alterações entre as versões 3.0.0 e 4.1.0 do Az.

- [Guia de migração para o Az 4.1.0](#migration-guide-for-az-410)
  - [Az.ApiManagement](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [Az.Batch](#azbatch)
    - [`Get-AzBatchApplication`, `New-AzBatchApplication`](#get-azbatchapplication-new-azbatchapplication)
    - [`Get-AzBatchComputeNode`, `New-AzBatchPool`](#get-azbatchcomputenode-new-azbatchpool)
    - [`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [Az.Compute](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [Az.KeyVault](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [Az.Monitor](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [Az.Network](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [Az.OperationalInsights](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [Az.Resources](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [Az.Storage](#azstorage)
    - [`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [`New-AzStorageTable`, `Get-AzStorageTable`](#new-azstoragetable-get-azstoragetable)
    - [`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a>Az.ApiManagement

### `Add-AzApiManagementRegion`

O tipo de propriedade `Type` do tipo `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` foi alterado de `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` para `System.String`.

### `New-AzApiManagement`

- O cmdlet `New-AzApiManagement` não é mais compatível com o parâmetro `AssignIdentity` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `__AllParameterSets` para o cmdlet `New-AzApiManagement` foi removido.

### `Set-AzApiManagement`

- O cmdlet `Set-AzApiManagement` não é mais compatível com o parâmetro `AssignIdentity` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `__AllParameterSets` para o cmdlet `Set-AzApiManagement` foi removido.

### `Get-AzApiManagementProperty`

O cmdlet `Get-AzApiManagementProperty` foi removido e nenhum alias foi encontrado para o nome do cmdlet original.

### `New-AzApiManagementProperty`

O cmdlet `New-AzApiManagementProperty` foi removido e nenhum alias foi encontrado para o nome do cmdlet original.

### `Remove-AzApiManagementProperty`

O cmdlet `Remove-AzApiManagementProperty` foi removido e nenhum alias foi encontrado para o nome do cmdlet original.

### `Set-AzApiManagementProperty`

O cmdlet `Set-AzApiManagementProperty` foi removido e nenhum alias foi encontrado para o nome do cmdlet original.

## <a name="azbatch"></a>Az.Batch

### <a name="get-azbatchapplication-new-azbatchapplication"></a>`Get-AzBatchApplication`, `New-AzBatchApplication`

A propriedade `ApplicationPackages` do tipo `Microsoft.Azure.Commands.Batch.Models.PSApplication` foi removida.

### <a name="get-azbatchcomputenode-new-azbatchpool"></a>`Get-AzBatchComputeNode`, `New-AzBatchPool`

A propriedade `PublicIPs` do tipo `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` foi removida

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a>`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`

O tipo de propriedade `StorageUrlExpiry` do tipo `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` foi alterado de `System.DateTime` para `System.DateTime?`.

## <a name="azcompute"></a>Az.Compute

### `Remove-AzVmssDiagnosticsExtension`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVMImage`

- O cmdlet `Get-AzVMImage` não é mais compatível com o parâmetro `FilterExpression` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `ListVMImage` para o cmdlet `Get-AzVMImage` foi removido.

### `New-AzVMConfig`

- O cmdlet `New-AzVMConfig` não é mais compatível com o parâmetro `AssignIdentity` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `AssignIdentityParameterSet` para o cmdlet `New-AzVMConfig` foi removido.

### `Update-AzVM`

- O cmdlet `Update-AzVM` não é mais compatível com o parâmetro `AssignIdentity` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `AssignIdentityParameterSet` para o cmdlet `Update-AzVM` foi removido.

### `New-AzProximityPlacementGroup`

- O tipo genérico para a propriedade `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` foi alterado de `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` para `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- A propriedade `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` foi removida.

#### <a name="before"></a>Antes de

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- O tipo genérico para a propriedade `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` foi alterado de `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` para `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- A propriedade `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` foi removida.

#### <a name="before"></a>Antes de

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- O tipo genérico para a propriedade `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` foi alterado de `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` para `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- A propriedade `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` foi removida.

#### <a name="before"></a>Antes de

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssDataDisk`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssExtension`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssNetworkInterfaceConfiguration`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSecret`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSshPublicKey`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssWinRMListener`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmssConfig`

- O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- Não é mais compatível com o parâmetro `AutomaticRepairMaxInstanceRepairsPercent` e nenhum alias foi encontrado para o nome do parâmetro original.
- Não é mais compatível com o parâmetro `AssignIdentity` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `__AllParameterSets` foi removido.
- O conjunto de parâmetros `ExplicitIdentityParameterSet` foi removido.
- O conjunto de parâmetros `AssignIdentityParameterSet` foi removido.

### `Remove-AzVmssDataDisk`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssExtension`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssNetworkInterfaceConfiguration`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssBootDiagnostic`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOsProfile`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssRollingUpgradePolicy`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssStorageProfile`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmss`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Repair-AzVmssServiceFabricUpdateDomain`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVmss`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOrchestrationServiceState`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Update-AzVmss`

- O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- Não é mais compatível com o parâmetro `AutomaticRepairMaxInstanceRepairsPercent` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `__AllParameterSets` foi removido.
- O conjunto de parâmetros `ExplicitIdentityParameterSet` foi removido.

### `Add-AzVmssDiagnosticsExtension`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Disable-AzVmssDiskEncryption`

O tipo de propriedade `AutomaticRepairsPolicy` do tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` foi alterado de `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` para `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

## <a name="azkeyvault"></a>Az.KeyVault

### `New-AzKeyVaultCertificateOrganizationDetail`

O alias `New-AzKeyVaultCertificateOrganizationDetails` foi removido. Use `New-AzKeyVaultCertificateOrganizationDetail`.

#### <a name="before"></a>Antes de

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

O alias `New-AzKeyVaultCertificateAdministratorDetails` foi removido. Use `New-AzKeyVaultCertificateAdministratorDetail`.

#### <a name="before"></a>Antes de

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

`-EnableSoftDelete` foi removido, pois a exclusão temporária está habilitada por padrão. Use `-DisableSoftDelete` se você não deseja esse comportamento.

#### <a name="before"></a>Antes de

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a>Az.Monitor

### `Add-AzLogProfile`

O tipo de propriedade `RetentionPolicy` do tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` foi alterado de `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` para `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `Get-AzLogProfile`

O tipo de propriedade `RetentionPolicy` do tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` foi alterado de `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` para `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `New-AzMetricAlertRuleV2Criteria`

O conjunto de parâmetros `__AllParameterSets` para o cmdlet `New-AzMetricAlertRuleV2Criteria` foi removido.

## <a name="aznetwork"></a>Az.Network

### `Get-AzNetworkWatcherConnectionMonitor`

O tipo genérico para a propriedade `RoundTripTimeMs` foi alterado de `System.Nullable1[System.Int32]` para `System.Nullable1[System.Double]`.

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

O tipo genérico para o parâmetro `SuccessThresholdRoundTripTimeMs` foi alterado de `System.Nullable1[System.Int32]` para `System.Nullable1[System.Double]`.

## <a name="azoperationalinsights"></a>Az.OperationalInsights

### `Get-AzOperationalInsightsDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsApplicationInsightsDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsAzureActivityLogDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsCustomLogDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsLinuxSyslogDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsWindowsEventDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Remove-AzOperationalInsightsDataSource`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Disable-AzOperationalInsightsIISLogCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Enable-AzOperationalInsightsIISLogCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Get-AzOperationalInsightsSavedSearch`

A propriedade `Metadata` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` foi removida.

### `Get-AzOperationalInsightsSavedSearchResult`

O cmdlet `Get-AzOperationalInsightsSavedSearchResult` foi removido e nenhum alias foi encontrado para o nome do cmdlet original.

### `Get-AzOperationalInsightsSearchResult`

O cmdlet `Get-AzOperationalInsightsSearchResult` foi removido e nenhum alias foi encontrado para o nome do cmdlet original.

### `Get-AzOperationalInsightsStorageInsight`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsStorageInsight`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Remove-AzOperationalInsightsStorageInsight`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Set-AzOperationalInsightsStorageInsight`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Get-AzOperationalInsightsLinkTarget`

O cmdlet `Get-AzOperationalInsightsLinkTarget` foi removido e nenhum alias foi encontrado para o nome do cmdlet original.

### `Get-AzOperationalInsightsWorkspace`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `New-AzOperationalInsightsWorkspace`

- A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.
- O cmdlet `New-AzOperationalInsightsWorkspace` não é mais compatível com o parâmetro `CustomerId` e nenhum alias foi encontrado para o nome do parâmetro original.
- O conjunto de parâmetros `__AllParameterSets` para o cmdlet `New-AzOperationalInsightsWorkspace` foi removido.

### `Set-AzOperationalInsightsWorkspace`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

### `Invoke-AzOperationalInsightsQuery`

A propriedade `PortalUrl` do tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` foi removida.

## <a name="azresources"></a>Az.Resources

### `Get-AzDeploymentScript`

O tipo de propriedade `Status` do tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` foi alterado de `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` para `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzDeploymentScriptLog`

O tipo de propriedade `Status` do tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` foi alterado de `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` para `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Save-AzDeploymentScriptLog`

O tipo de propriedade `Status` do tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` foi alterado de `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` para `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

O parâmetro `TenantLevel` foi removido.

### `Get-AzPolicyAlias`

O tipo genérico para a propriedade `Aliases` foi alterado de `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` para `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.

### `New-AzPolicyAssignment`

- O cmdlet `New-AzPolicyAssignment` não dá mais suporte ao tipo `System.Management.Automation.PSObject` para o parâmetro `PolicyDefinition`.
- O cmdlet `New-AzPolicyAssignment` não dá mais suporte ao tipo `System.Management.Automation.PSObject` para o parâmetro `PolicySetDefinition`.

### `Remove-AzDeploymentScript`

O tipo de propriedade `Status` do tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` foi alterado de `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` para `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

## <a name="azstorage"></a>Az.Storage

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a>`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`

Valor de DefaultAction de NetWorkRule alterado de: Permitir = 1, Negar = 0, para: Permitir = 0, Negar = 1.

### <a name="new-azstoragetable-get-azstoragetable"></a>`New-AzStorageTable`, `Get-AzStorageTable`

O objeto de saída AzureStorageTable.CloudTable.ServiceClient tem duas propriedades removidas: ConnectionPolicy, ConsistencyLevel.

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a>`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`

Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará a propriedade filho da nova saída "CloudFile"

#### <a name="before"></a>Antes de

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a>`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`

Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará a propriedade filho da nova saída "CloudFileDirectory"

#### <a name="before"></a>Antes de

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a>`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`

Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará a propriedade sub-filho da nova saída "CloudFileShare"

#### <a name="before"></a>Antes de

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará a propriedade sub-filho da nova saída "CloudFileShare.Properties"

#### <a name="before"></a>Antes de

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

Ao remover subdiretórios de arquivos com o objeto Directory pai e -Path, não é mais possível inserir -Path do pipeline com a correspondência de tipo (cadeia de caracteres).

#### <a name="before"></a>Antes de

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>After (após)

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
