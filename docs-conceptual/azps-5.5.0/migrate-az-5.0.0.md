---
title: Guia de migração para o Az 5.0.0
description: Este guia de migração contém uma lista de alterações da falha feitas no Azure PowerShell no lançamento do Az versão 5.0.0.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100011906"
---
# <a name="migration-guide-for-az-500"></a>Guia de Migração para o Az 5.0.0

Este documento descreverá as alterações do Az entre as versões 4.0.0 e 5.0.0.

- [Guia de Migração para o Az 5.0.0](#migration-guide-for-az-500)
  - [Az.Aks](#azaks)
    - [New-AzAksCluster](#new-azakscluster)
    - [Set-AzAksCluster](#set-azakscluster)
  - [Az.ContainerRegistry](#azcontainerregistry)
    - [New-AzContainerRegistry](#new-azcontainerregistry)
  - [Az.Functions](#azfunctions)
    - [Get-AzFunctionApp](#get-azfunctionapp)
    - [New-AzFunctionApp](#new-azfunctionapp)
  - [Az.KeyVault](#azkeyvault)
    - [New-AzKeyVault](#new-azkeyvault)
    - [Update-AzKeyVault](#update-azkeyvault)
    - [Get-AzKeyVaultSecret](#get-azkeyvaultsecret)
  - [Az.ManagedServices](#azmanagedservices)
    - [Get-AzManagedServicesDefinition](#get-azmanagedservicesdefinition)
    - [New-AzManagedServicesAssignment](#new-azmanagedservicesassignment)
    - [Remove-AzManagedServicesAssignment](#remove-azmanagedservicesassignment)
    - [Remove-AzManagedServicesDefinition](#remove-azmanagedservicesdefinition)
  - [Az.ResourceManager](#azresourcemanager)
    - [Get-AzManagementGroupDeployment](#get-azmanagementgroupdeployment)
    - [Get-AzManagementGroupDeploymentOperation](#get-azmanagementgroupdeploymentoperation)
    - [Get-AzDeployment](#get-azdeployment)
    - [Get-AzDeploymentOperation](#get-azdeploymentoperation)
    - [Get-AzDeploymentWhatIfResult](#get-azdeploymentwhatifresult)
    - [Get-AzTenantDeployment](#get-aztenantdeployment)
    - [Get-AzTenantDeploymentOperation](#get-aztenantdeploymentoperation)
    - [New-AzManagementGroupDeployment](#new-azmanagementgroupdeployment)
    - [New-AzDeployment](#new-azdeployment)
    - [New-AzTenantDeployment](#new-aztenantdeployment)
    - [Remove-AzManagementGroupDeployment](#remove-azmanagementgroupdeployment)
    - [Remove-AzDeployment](#remove-azdeployment)
    - [Remove-AzTenantDeployment](#remove-aztenantdeployment)
    - [Save-AzManagementGroupDeploymentTemplate](#save-azmanagementgroupdeploymenttemplate)
    - [Save-AzDeploymentTemplate](#save-azdeploymenttemplate)
    - [Save-AzTenantDeploymentTemplate](#save-aztenantdeploymenttemplate)
    - [Stop-AzManagementGroupDeployment](#stop-azmanagementgroupdeployment)
    - [Stop-AzDeployment](#stop-azdeployment)
    - [Stop-AzTenantDeployment](#stop-aztenantdeployment)
    - [Test-AzManagementGroupDeployment](#test-azmanagementgroupdeployment)
    - [Test-AzDeployment](#test-azdeployment)
    - [Test-AzTenantDeployment](#test-aztenantdeployment)
    - [Get-AzResourceGroupDeployment](#get-azresourcegroupdeployment)
    - [Get-AzResourceGroupDeploymentOperation](#get-azresourcegroupdeploymentoperation)
    - [Get-AzResourceGroupDeploymentWhatIfResult](#get-azresourcegroupdeploymentwhatifresult)
    - [New-AzResourceGroupDeployment](#new-azresourcegroupdeployment)
    - [Remove-AzResourceGroupDeployment](#remove-azresourcegroupdeployment)
    - [Save-AzResourceGroupDeploymentTemplate](#save-azresourcegroupdeploymenttemplate)
    - [Stop-AzResourceGroupDeployment](#stop-azresourcegroupdeployment)
    - [Test-AzResourceGroupDeployment](#test-azresourcegroupdeployment)
    - [Get-AzManagementGroupDeploymentWhatIfResult](#get-azmanagementgroupdeploymentwhatifresult)
    - [Get-AzTenantDeploymentWhatIfResult](#get-aztenantdeploymentwhatifresult)
  - [Az.Sql](#azsql)
    - [Set-AzSqlServerActiveDirectoryAdministrator](#set-azsqlserveractivedirectoryadministrator)
  - [Az.Synapse](#azsynapse)
    - [New-AzSynapseSqlPool](#new-azsynapsesqlpool)
    - [Update-AzSynapseSqlPool](#update-azsynapsesqlpool)
  - [Az.Network](#aznetwork)
    - [Approve-AzPrivateEndpointConnection](#approve-azprivateendpointconnection)
    - [Deny-AzPrivateEndpointConnection](#deny-azprivateendpointconnection)
    - [Get-AzPrivateEndpointConnection](#get-azprivateendpointconnection)
    - [Remove-AzPrivateEndpointConnection](#remove-azprivateendpointconnection)
    - [Set-AzPrivateEndpointConnection](#set-azprivateendpointconnection)
    - [New-AzNetworkWatcherConnectionMonitorEndpointObject](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a>Az.Aks

### <a name="new-azakscluster"></a>New-AzAksCluster

- Não é mais compatível com o parâmetro `NodeOsType`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original. Ele sempre será `Linux`.
- Não é mais compatível com o alias `ClientIdAndSecret` para o parâmetro `ServicePrincipalIdAndSecret`.
- O valor padrão de `NodeVmSetType` foi alterado de `AvailabilitySet` para `VirtualMachineScaleSets`.
- O valor padrão de `NetworkPlugin` foi alterado de `none` para `azure`.

#### <a name="before"></a>Antes

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a>Depois

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a>Set-AzAksCluster

Não é mais compatível com o alias `ClientIdAndSecret` para o parâmetro `ServicePrincipalIdAndSecret`.

#### <a name="before"></a>Antes

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a>Depois

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a>Az.ContainerRegistry

### <a name="new-azcontainerregistry"></a>New-AzContainerRegistry

Não é mais compatível com o parâmetro `StorageAccountName` e nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a>Depois

`Classic` foi preterido e `StorageAccountName` foi removido, pois ele só funcionava com um Registro de Contêiner Clássico.

## <a name="azfunctions"></a>Az.Functions

### <a name="get-azfunctionapp"></a>Get-AzFunctionApp

Remoção do parâmetro de opção `IncludeSlot` de todos os parâmetros, exceto de um conjunto de parâmetros de `Get-AzFunctionApp`. O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados quando `-IncludeSlot` for especificado.
Essa funcionalidade foi interrompida na versão anterior do cmdlet. No entanto, isso foi corrigido.

### <a name="new-azfunctionapp"></a>New-AzFunctionApp

- Correção de `-DisableApplicationInsights` em `New-AzFunctionApp` para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.
- Remoção do suporte para criar aplicativos de funções do PowerShell 6.2, pois o PowerShell 6.2 é EOL. As diretrizes atuais para os clientes é criar aplicativos de funções do PowerShell 7.0 como alternativa.
- Alteração da versão de runtime padrão da 6.2 para a 7.0 no Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro `RuntimeVersion` não for especificado.
- Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro `RuntimeVersion` não for especificado. No entanto, os usuários ainda poderão criar aplicativos de funções do Node 10 especificando `-Runtime Node` e `-RuntimeVersion 10`. Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro `RuntimeVersion` não for especificado. No entanto, os usuários ainda poderão criar aplicativos de funções do Python 3.7 especificando `-Runtime Python` e `-RuntimeVersion 3.7`.

#### <a name="before"></a>Antes

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a>Depois

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a>Az.KeyVault

### <a name="new-azkeyvault"></a>New-AzKeyVault

Não é mais compatível com o parâmetro `DisableSoftDelete` e nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a>Depois

A capacidade de atualizar a configuração de exclusão reversível será preterida no Az.KeyVault 3.0.0. Leia mais: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="update-azkeyvault"></a>Update-AzKeyVault

Não é mais compatível com os parâmetros `EnableSoftDelete` e `SoftDeleteRetentionInDays`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a>Depois

A capacidade de atualizar a configuração de exclusão reversível será preterida no Az.KeyVault 3.0.0. Leia mais: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="get-azkeyvaultsecret"></a>Get-AzKeyVaultSecret

A propriedade `SecretValueText` do tipo `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` foi removida. A propriedade `SecretValueText` foi substituída por `SecretValue`.

#### <a name="before"></a>Antes

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a>Depois

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a>Az.ManagedServices

### <a name="get-azmanagedservicesdefinition"></a>Get-AzManagedServicesDefinition

Não é mais compatível com o parâmetro `ResourceId` e nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Depois

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a>New-AzManagedServicesAssignment

Não é mais compatível com os parâmetros `RegistrationDefinitionName` e `RegistrationDefinitionResourceId`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a>Depois

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a>Remove-AzManagedServicesAssignment

Não é mais compatível com os parâmetros `Id` e `ResourceId`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a>Depois

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a>Remove-AzManagedServicesDefinition

Não é mais compatível com os parâmetros `Id` e `ResourceId`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Depois

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a>Az.ResourceManager

### <a name="get-azmanagementgroupdeployment"></a>Get-AzManagementGroupDeployment

Não é mais compatível com o parâmetro `ApiVersion` e nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a>Depois

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a>Get-AzManagementGroupDeploymentOperation

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-azdeployment"></a>Get-AzDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentoperation"></a>Get-AzDeploymentOperation

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentwhatifresult"></a>Get-AzDeploymentWhatIfResult

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeployment"></a>Get-AzTenantDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentoperation"></a>Get-AzTenantDeploymentOperation

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="new-azmanagementgroupdeployment"></a>New-AzManagementGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="new-azdeployment"></a>New-AzDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="new-aztenantdeployment"></a>New-AzTenantDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="remove-azmanagementgroupdeployment"></a>Remove-AzManagementGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="remove-azdeployment"></a>Remove-AzDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="remove-aztenantdeployment"></a>Remove-AzTenantDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="save-azmanagementgroupdeploymenttemplate"></a>Save-AzManagementGroupDeploymentTemplate

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="save-azdeploymenttemplate"></a>Save-AzDeploymentTemplate

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="save-aztenantdeploymenttemplate"></a>Save-AzTenantDeploymentTemplate

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="stop-azmanagementgroupdeployment"></a>Stop-AzManagementGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="stop-azdeployment"></a>Stop-AzDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="stop-aztenantdeployment"></a>Stop-AzTenantDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="test-azmanagementgroupdeployment"></a>Test-AzManagementGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="test-azdeployment"></a>Test-AzDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="test-aztenantdeployment"></a>Test-AzTenantDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeployment"></a>Get-AzResourceGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentoperation"></a>Get-AzResourceGroupDeploymentOperation

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentwhatifresult"></a>Get-AzResourceGroupDeploymentWhatIfResult

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="new-azresourcegroupdeployment"></a>New-AzResourceGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="remove-azresourcegroupdeployment"></a>Remove-AzResourceGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="save-azresourcegroupdeploymenttemplate"></a>Save-AzResourceGroupDeploymentTemplate

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="stop-azresourcegroupdeployment"></a>Stop-AzResourceGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="test-azresourcegroupdeployment"></a>Test-AzResourceGroupDeployment

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a>Get-AzManagementGroupDeploymentWhatIfResult

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentwhatifresult"></a>Get-AzTenantDeploymentWhatIfResult

O mesmo ocorre com `Get-AzManagementGroupDeployment`.

## <a name="azsql"></a>Az.Sql

### <a name="set-azsqlserveractivedirectoryadministrator"></a>Set-AzSqlServerActiveDirectoryAdministrator

Não é mais compatível com o parâmetro `IsAzureADOnlyAuthentication` e nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a>Depois

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a>Az.Synapse

### <a name="new-azsynapsesqlpool"></a>New-AzSynapseSqlPool

Não é mais compatível com os parâmetros: `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` e `RestorePoint`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a>Depois

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a>Update-AzSynapseSqlPool

Não é mais compatível com os parâmetros `Suspend` e `Resume`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.

## <a name="aznetwork"></a>Az.Network

### <a name="approve-azprivateendpointconnection"></a>Approve-AzPrivateEndpointConnection

Não é mais compatível com o parâmetro `PrivateLinkResourceType` e nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a>Depois

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a>Deny-AzPrivateEndpointConnection

O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.

### <a name="get-azprivateendpointconnection"></a>Get-AzPrivateEndpointConnection

O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.

### <a name="remove-azprivateendpointconnection"></a>Remove-AzPrivateEndpointConnection

O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.

### <a name="set-azprivateendpointconnection"></a>Set-AzPrivateEndpointConnection

O mesmo ocorre com `Approve-AzPrivateEndpointConnection`.

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a>New-AzNetworkWatcherConnectionMonitorEndpointObject

Não é mais compatível com os parâmetros `FilterType` e `FilterItem`. Além disso, nenhum alias foi encontrado para o nome do parâmetro original.

#### <a name="before"></a>Antes

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a>After (após)

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
