---
title: Alterações interruptivas no Microsoft Azure PowerShell 6.0.0
description: Este guia de migração contém uma lista de alterações da falha criadas para o Azure PowerShell na versão de lançamento 6.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: ab20dd07fb0c14d8066ad12185f8245be291e7ec
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84122247"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Alterações interruptivas no Microsoft Azure PowerShell 6.0.0

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Este documento serve como uma notificação de alterações interruptivas e como um guia de migração para consumidores dos cmdlets do Microsoft Azure PowerShell. Cada seção descreve o motivo da alteração significativa e o caminho de migração de menor resistência. Para obter um contexto detalhado, consulte a solicitação de pull associada a cada alteração.

## <a name="table-of-contents"></a>Sumário

- [Alterações da falha gerais](#general-breaking-changes)
  - [Versão mínima do PowerShell necessária aumentada para 5.0](#minimum-powershell-version-required-bumped-to-50)
  - [Salvamento automático de contexto habilitado por padrão](#context-autosave-enabled-by-default)
  - [Remoção do alias Marcas](#removal-of-tags-alias)
- [Alterações de falha nos cmdlets do AzureRM.Compute](#breaking-changes-to-azurermcompute-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.DataLakeStore](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.Dns](#breaking-changes-to-azurermdns-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.Insights](#breaking-changes-to-azurerminsights-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.KeyVault](#breaking-changes-to-azurermkeyvault-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.Network](#breaking-changes-to-azurermnetwork-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.RedisCache](#breaking-changes-to-azurermrediscache-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.Resources](#breaking-changes-to-azurermresources-cmdlets)
- [Alterações de falha nos cmdlets do AzureRM.Storage](#breaking-changes-to-azurermstorage-cmdlets)
- [Módulos removidos](#removed-modules)
  - [`AzureRM.ServerManagement`](#azurermservermanagement)
  - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>Alterações da falha gerais

### <a name="minimum-powershell-version-required-bumped-to-50"></a>Versão mínima do PowerShell necessária aumentada para 5.0

Anteriormente, o Azure PowerShell precisava de _pelo menos_ a versão 3.0 do PowerShell para executar qualquer cmdlet. Mais para frente, este requisito será aumentado para a versão 5.0 do PowerShell. Para informações sobre a atualização para o PowerShell 5.0, consulte [esta tabela](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).

### <a name="context-autosave-enabled-by-default"></a>Salvamento automático de contexto habilitado por padrão

O salvamento automático do contexto é o armazenamento de informações de conexão do Azure que pode ser usado entre novas e diferentes sessões do PowerShell. Para obter mais informações sobre o salvamento automático de contexto, consulte [este documento](/powershell/azure/context-persistence).

Anteriormente, por padrão, o salvamento automático do contexto era desabilitado, significando que as informações de autenticação do Azure do usuário não eram armazenadas entre as sessões até o `Enable-AzureRmContextAutosave` cmdlet ser executado para ativar a persistência do contexto. Mais adiante, o salvamento automático do contexto será habilitado por padrão, significando que os usuários _sem nenhuma configuração de salvamento automático gravada_  terão seu contexto armazenado na próxima vez que entrarem. Os usuários podem recusar essa funcionalidade usando o cmdlet `Disable-AzureRmContextAutosave`.

> [!NOTE]
> Os usuários que desabilitaram previamente o salvamento automático de contexto ou os usuários com salvamento automático de contexto habilitado e contextos existentes não serão afetados por essa alteração.

### <a name="removal-of-tags-alias"></a>Remoção do alias Marcas

O alias `Tags` para o parâmetro `Tag` foi removido de vários cmdlets. Abaixo está uma lista de módulos (e os cmdlets correspondentes) afetados por isso:

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

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.Compute

**Diversos**

- A propriedade de nome do sku aninhados em tipos `PSDisk` e `PSSnapshot` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- A propriedade de tipo de conta de armazenamento aninhada nos tipos `PSVirtualMachine`, `PSVirtualMachineScaleSet` e `PSImage` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**

- Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**Add-AzureRmVMDataDisk**

- Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**Add-AzureRmVmssDataDisk**

- Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**New-AzureRmAvailabilitySet**
- O parâmetro `Managed` foi removido em favor de `Sku`

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**New-AzureRmDiskUpdateConfig**
- Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**New-AzureRmSnapshotConfig**
- Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**New-AzureRmSnapshotUpdateConfig**
- Os valores aceitos para o parâmetro `SkuName` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**Set-AzureRmImageOsDisk**
- Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**Set-AzureRmVMAEMExtension**
- O parâmetro `DisableWAD` foi removido
    -  Diagnóstico do Windows Azure está desabilitado por padrão

**Set-AzureRmVMDataDisk**
- Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**Set-AzureRmVMOSDisk**
- Os valores aceitos para o parâmetro `StorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**Set-AzureRmVmssStorageProfile**
- Os valores aceitos para o parâmetro `ManagedDisk` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

**Update-AzureRmVmss**
- Os valores aceitos para o parâmetro `ManagedDiskStorageAccountType` alterado de `StandardLRS` e `PremiumLRS` para `Standard_LRS` e `Premium_LRS`, respectivamente

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.DataLakeStore

**Export-AzureRmDataLakeStoreItem**
- Os parâmetros `PerFileThreadCount` e `ConcurrentFileCount` foram removidos. Use o parâmetro `Concurrency` no futuro

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- Os parâmetros `PerFileThreadCount` e `ConcurrentFileCount` foram removidos. Use o parâmetro `Concurrency` no futuro

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- O parâmetro `Clean` foi removido

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.Dns

**New-AzureRmDnsRecordSet**
- O parâmetro `Force` foi removido

**Remove-AzureRmDnsRecordSet**
- O parâmetro `Force` foi removido

**Remove-AzureRmDnsZone**
- O parâmetro `Force` foi removido

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.Insights

**Add-AzureRmAutoscaleSetting**
- Os aliases dos parâmetros `AutoscaleProfiles` e `Notifications` foram removidos

**Add-AzureRmLogProfile**
- Os aliases dos parâmetros `Categories` e `Locations` foram removidos

**Add-AzureRmMetricAlertRule**
- O alias do parâmetro `Actions` foi removido

**Add-AzureRmWebtestAlertRule**
- O alias do parâmetro `Actions` foi removido

**Get-AzureRmLog**
- Os aliases dos parâmetros `MaxRecords` e `MaxEvents` foram removidos

**Get-AzureRmMetricDefinition**
- O alias do parâmetro `MetricNames` foi removido

**New-AzureRmAlertRuleEmail**
- Os aliases dos parâmetros `CustomEmails` e `SendToServiceOwners` foram removidos

**New-AzureRmAlertRuleWebhook**
- O alias do parâmetro `Properties` foi removido

**New-AzureRmAutoscaleNotification**
- Os aliases dos parâmetros `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` e `Webhooks` foram removidos

**New-AzureRmAutoscaleProfile**
- Os aliases dos parâmetros `Rules`, `ScheduleDays`, `ScheduleHours` e `ScheduleMinutes` foram removidos

**New-AzureRmAutoscaleWebhook**
- O alias do parâmetro `Properties` foi removido

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.KeyVault

**Add-AzureKeyVaultCertificate**
- O parâmetro `CertificatePolicy` se tornou obrigatório.

**Set-AzureKeyVaultManagedStorageSasDefinition**
- O cmdlet não aceita parâmetros individuais que compõem o token de acesso. Em vez disso, o cmdlet substitui parâmetros explícitos de token, como `Service` ou `Permissions`, com um parâmetro `TemplateUri` genérico, correspondente a um token de acesso de exemplo definido em outro lugar (supostamente usando cmdlets do PowerShell de armazenamento ou composto manualmente, de acordo com a documentação de armazenamento). O cmdlet retém o parâmetro `ValidityPeriod`.

Para obter mais informações sobre a composição de tokens de acesso compartilhados para o Armazenamento do Azure, consulte as páginas de documentação, respectivamente:

- [Constructing a Service SAS (Criação de uma SAS de serviço)](/rest/api/storageservices/Constructing-a-Service-SAS)
- [Constructing an Account SAS (Criação de uma SAS de conta)](/rest/api/storageservices/constructing-an-account-sas)

```powershell-interactive
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- O parâmetro `IssuerProvider` se tornou obrigatório.

**Undo-AzureKeyVaultCertificateRemoval**
- A saída desse cmdlet mudou de `CertificateBundle` para `PSKeyVaultCertificate`.

**Undo-AzureRmKeyVaultRemoval**
- `ResourceGroupName` foi removido do conjunto de parâmetros `InputObject` e, em vez disso, é obtido no `InputObject` da propriedade do parâmetro `ResourceId`.

**Set-AzureRmKeyVaultAccessPolicy**
- A permissão `all` foi removida do `PermissionsToKeys`, `PermissionsToSecrets`, e `PermissionsToCertificates`.

**Geral**
- A propriedade `ValueFromPipelineByPropertyName` foi removida de todos os cmdlets nos quais foram habilitados o direcionamento por `InputObject`. Os cmdlets afetados são:
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

- Os níveis `ConfirmImpact` foram removidos de todos os cmdlets.  Os cmdlets afetados são:
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

- O `IKeyVaultDataServiceClient` foi atualizado para que todas as operações de Certificado retornem PSTypes em vez de tipos SDK. Isso inclui:
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

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.Network


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- O parâmetro `ProbeEnabled` foi removido

**Add-AzureRmVirtualNetworkPeering**
- O alias do parâmetro `AlloowGatewayTransit` foi removido

**New-AzureRmApplicationGatewayBackendHttpSettings**
- O parâmetro `ProbeEnabled` foi removido

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- O parâmetro `ProbeEnabled` foi removido

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.RedisCache

**New-AzureRmRedisCache**
- Os parâmetros `Subnet` e `VirtualNetwork` foram removidos em favor de `SubnetId`
- O parâmetro `RedisVersion` foi removido
- O parâmetro `MaxMemoryPolicy` foi removido em favor de `RedisConfiguration`

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- O parâmetro `MaxMemoryPolicy` foi removido em favor de `RedisConfiguration`

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.Resources

**Find-AzureRmResource**
- Esse cmdlet foi removido e a funcionalidade foi movida para `Get-AzureRmResource`

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- Esse cmdlet foi removido e a funcionalidade foi movida para `Get-AzureRmResourceGroup`

```powershell-interactive
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- O parâmetro `AtScopeAndBelow` foi removido.

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>Alterações de falha nos cmdlets do AzureRM.Storage

**New-AzureRmStorageAccount**
- O parâmetro `EnableEncryptionService` foi removido

**Set-AzureRmStorageAccount**
- Os parâmetros `EnableEncryptionService` e `DisableEncryptionService` foram removidos

## <a name="removed-modules"></a>Módulos removidos

### `AzureRM.ServerManagement`

O serviço de Ferramentas de Gerenciamento de Servidor se tornou [obsoleto no ano passado](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)e, como resultado, o módulo correspondente para SMT, `AzureRM.ServerManagement`, foi removido do `AzureRM` e parará de enviar no futuro.

### `AzureRM.SiteRecovery`

O módulo `AzureRM.SiteRecovery` está sendo substituído pelo `AzureRM.RecoveryServices.SiteRecovery`, que é um superconjunto funcional do módulo `AzureRM.SiteRecovery` e inclui um novo conjunto de cmdlets equivalentes. A lista completa de mapeamentos de antigos para novos cmdlets pode ser encontrada abaixo:

| Cmdlet preterido                                        | Cmdlet equivalente                                                | Aliases                                  |
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
