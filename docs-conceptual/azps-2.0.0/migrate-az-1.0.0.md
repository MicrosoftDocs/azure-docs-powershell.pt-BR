---
title: Alterações significativas no Microsoft Azure PowerShell Az 1.0.0
description: Este guia de migração contém uma lista de alterações significativas criadas para o Azure PowerShell na versão de lançamento 1 do Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: 1cdacbdf4aaf2d7f92cb4773abddaa3b70f5208b
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048794"
---
# <a name="migration-guide-for-az-100"></a>Guia de Migração para 1.0.0

Este documento descreve as alterações entre as versões 6.x do AzureRM e da versão 1.0.0 do Az.

## <a name="table-of-contents"></a>Sumário
- [Alterações da falha gerais](#general-breaking-changes)
  - [Alterações de prefixo de substantivo do cmdlet](#cmdlet-noun-prefix-changes)
  - [Alterações de nome de módulo](#module-name-changes)
  - [Módulos removidos](#removed-modules)
  - [Windows PowerShell 5.1 e .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Remoção temporária de logon de usuário usando PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Logon de código de dispositivo padrão em vez de prompt de navegador da Web](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [Alterações de falhas para módulos](#module-breaking-changes)
  - [Az.ApiManagement (anteriormente AzureRM.ApiManagement)](#azapimanagement-previously-azurermapimanagement)
  - [Az.Billing (anteriormente AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [Az.CognitiveServices (anteriormente AzureRM.CognitiveServices)](#azcognitiveservices-previously-azurermcognitiveservices)
  - [Az.Compute (anteriormente AzureRM.Compute)](#azcompute-previously-azurermcompute)
  - [Az.DataFactory (anteriormente AzureRM.DataFactories e AzureRM.DataFactoryV2)](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [Az.DataLakeAnalytics (anteriormente AzureRM.DataLakeAnalytics)](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [Az.DataLakeStore (anteriormente AzureRM.DataLakeStore)](#azdatalakestore-previously-azurermdatalakestore)
  - [Az.KeyVault (anteriormente AzureRM.KeyVault)](#azkeyvault-previously-azurermkeyvault)
  - [Az.Media (anteriormente AzureRM.Media)](#azmedia-previously-azurermmedia)
  - [Az.Monitor (anteriormente AzureRM.Insights)](#azmonitor-previously-azurerminsights)
  - [Az.Network (anteriormente AzureRM.Network)](#aznetwork-previously-azurermnetwork)
  - [Az.OperationalInsights (anteriormente AzureRM.OperationalInsights)](#azoperationalinsights-previously-azurermoperationalinsights)
  - [Az.RecoveryServices (anteriormente AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [Az.Resources (anteriormente AzureRM.Resources)](#azresources-previously-azurermresources)
  - [Az.ServiceFabric (anteriormente AzureRM.ServiceFabric)](#azservicefabric-previously-azurermservicefabric)
  - [Az.Sql (anteriormente AzureRM.Sql)](#azsql-previously-azurermsql)
  - [Az.Storage (anteriormente Azure.Storage e AzureRM.Storage)](#azstorage-previously-azurestorage-and-azurermstorage)
  - [Az.Websites (anteriormente AzureRM.Websites)](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a>Alterações da falha gerais
### <a name="cmdlet-noun-prefix-changes"></a>Alterações de prefixo de substantivo do cmdlet
No AzureRM, os cmdlets usavam “AzureRM” ou “Azure” como um prefixo de substantivo.  O Az simplifica e normaliza os nomes do cmndlet, para que todos os cmdlets usem “Az” como seu prefixo de substantivo do cmdlet. Por exemplo: 
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

Foram alterados para
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

Para simplificar a transição para esses novos nomes de cmdlet, o Az apresenta dois novos cmdlets, ```Enable-AzureRmAlias``` e ```Disable-AzureRmAlias```.  ```Enable-AzureRmAlias``` cria os aliases de nomes de cmdlet mais antigos no AzureRM para os nomes de cmdlet mais recentes do Az.  O cmdlet permite criar aliases na sessão atual ou em todas as sessões, alterando seu usuário ou o perfil do computador. 

Por exemplo, o script a seguir no AzureRM:
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Pode ser executado com alterações mínimas usando ```Enable-AzureRmAlias```:
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Executar ```Enable-AzureRmAlias -Scope CurrentUser``` habilitará os aliases para todas as sessões do Powershell, para que após executar esse cmdlet, um script como este não precise ser alterado:
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Para obter detalhes completos sobre o uso dos cmdlets do alias, execute ```Get-Help -Online Enable-AzureRmAlias``` no prompt do PowerShell.

```Disable-AzureRmAlias``` remove os aliases de cmdlet do AzureRM criados pelo ```Enable-AzureRmAlias```.  Para obter detalhes completos, execute ```Get-Help -Online Disable-AzureRmAlias``` no prompt do PowerShell.

### <a name="module-name-changes"></a>Alterações de nome de módulo
- Os nomes do módulo foram alterados de `AzureRM.*` para `Az.*`, exceto para os seguintes módulos:
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

As alterações nos nomes dos módulos significam que qualquer script que usa ```#Requires``` ou ```Import-Module``` para carregar módulos específicos precisarão ser alterados para usar o novo módulo.

#### <a name="migrating-requires-statements"></a>Migração de instruções #Requires
Scripts que usam #Requires para declarar uma dependência em módulos AzureRM devem ser atualizados para usar os novos nomes de módulo
```powershell
#Requires -Module AzureRM.Compute
```

Deve ser alterado para
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a>Migração de instruções Import-Module
Scripts que usam ```Import-Module``` para carregar módulos do AzureRM precisarão ser atualizados para refletir os novos nomes de módulo.
```powershell
Import-Module -Name AzureRM.Compute
```

Deve ser alterado para
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migração de invocações de cmdlet totalmente qualificadas
Scripts que usam as invocações de cmdlet qualificadas por módulo, como
```powershell
AzureRM.Compute\Get-AzureRmVM
```

Devem ser alterados para usar os novos nomes de módulo e de cmdlet
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Migração de dependências de manifesto do módulo
Módulos que expressam as dependências em módulos AzureRM por meio de um arquivo de manifesto (.psd1) do módulo precisarão atualizar os nomes do módulo em sua seção “RequiredModules”

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Deve ser alterado para

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Módulos removidos
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Não há mais suporte ativo para as ferramentas para esses serviços.  Os clientes são incentivados a mudar para serviços alternativos, assim que for conveniente.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 e .NET 4.7.2
- Usar o Az com o Windows PowerShell 5.1 requer a instalação do .NET 4.7.2. No entanto, usar o Az com o PowerShell Core não exige o .NET 4.7.2. 

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Remoção temporária de logon de usuário usando PSCredential
- Devido a alterações no fluxo de autenticação para o .NET Standard, estamos temporariamente removendo o logon de usuário por meio do PSCredential. Essa funcionalidade será lançada novamente no lançamento de 15/1/2019 para o Windows PowerShell 5.1. Isso é discutido em detalhes [nesse problema.](https://github.com/Azure/azure-powershell/issues/7430)

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Logon de código de dispositivo padrão em vez de prompt de navegador da Web
- Devido a alterações no fluxo de autenticação para o .NET Standard, estamos usando o logon do dispositivo como o fluxo de logon padrão durante o logon interativo. O logon baseado em navegador da Web será reintroduzido novamente para o Windows PowerShell 5.1 como padrão no lançamento de 15/1/2019. Nesse momento, os usuários poderão escolher logon de dispositivo usando um parâmetro Switch.

## <a name="module-breaking-changes"></a>Alterações de falhas para módulos

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (anteriormente AzureRM.ApiManagement)
- Remoção dos seguintes cmdlets:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Use o cmdlet **Set-AzApiManagement** cmdlet para definir essas propriedades
- As propriedades a seguir foram removidas
  - Removidas as propriedades `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` e `ScmHostnameConfiguration` do tipo `PsApiManagementHostnameConfiguration` de `PsApiManagementContext`. Em vez disso, use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` e `ScmCustomHostnameConfiguration` do tipo `PsApiManagementCustomHostNameConfiguration`.
  - Removida a propriedade `StaticIPs` de PsApiManagementContext. A propriedade foi dividida em `PublicIPAddresses` e `PrivateIPAddresses`.
  - Removida a propriedade necessária `Location` do cmdlet New-AzureApiManagementVirtualNetwork.

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a>Az.Billing (anteriormente AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)
- O parâmetro `InvoiceName` foi removido em favor do cmdlet `Get-AzConsumptionUsageDetail`.  Os scripts precisarão usar outros parâmetros de identidade para a fatura.

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a>Az.CognitiveServices (anteriormente AzureRM.CognitiveServices)
- Removido o conjunto de parâmetros `GetSkusWithAccountParamSetName` do cmdlet `Get-AzCognitiveServicesAccountSkus`.  Você deve obter Skus por Account Type e Location, em vez de usar ResourceGroupName e Account Name.

### <a name="azcompute-previously-azurermcompute"></a>Az.Compute (anteriormente AzureRM.Compute)
- `IdentityIds` foram removidos da propriedade `Identity` nos Scripts dos objetos `PSVirtualMachine` e `PSVirtualMachineScaleSet`, que não devem mais usar o valor desse campo para tomar decisões de processamento.
- O tipo de propriedade `InstanceView` do objeto `PSVirtualMachineScaleSetVM` foi alterado de `VirtualMachineInstanceView` para `VirtualMachineScaleSetVMInstanceView`
- As propriedades `AutoOSUpgradePolicy` e `AutomaticOSUpgrade` foram removidas da propriedade `UpgradePolicy`
- O tipo de propriedade `Sku` do objeto `PSSnapshotUpdate` foi alterado de `DiskSku` para `SnapshotSku`
- `VmScaleSetVMParameterSet` foi removido do cmdlet `Add-AzVMDataDisk`, você não pode mais adicionar um disco de dados individualmente em uma VM ScaleSet.

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a>Az.DataFactory (anteriormente AzureRM.DataFactories e AzureRM.DataFactoryV2)
- O parâmetro `GatewayName` agora é obrigatório no cmdlet `New-AzDataFactoryEncryptValue`
- Removido o cmdlet `New-AzDataFactoryGatewayKey`
- Removido o parâmetro `LinkedServiceName` dos Scripts cmdlet `Get-AzDataFactoryV2ActivityRun`, que não devem mais usar o valor desse campo para tomar decisões de processamento.

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a>Az.DataLakeAnalytics (anteriormente AzureRM.DataLakeAnalytics)
- Removidos os cmdlets preteridos: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, e `Set-AzDataLakeAnalyticsCatalogSecret`

### <a name="azdatalakestore-previously-azurermdatalakestore"></a>Az.DataLakeStore (anteriormente AzureRM.DataLakeStore)
- Os cmdlets a seguir tiveram o parâmetro `Encoding` alterado do tipo `FileSystemCmdletProviderEncoding` para `System.Text.Encoding`. Essa alteração remove os valores de codificação `String` e `Oem`. Todos os outros valores de codificação anteriores permanecem.
  - New-AzureRmDataLakeStoreItem
  - Add-AzureRmDataLakeStoreItemContent
  - Get-AzureRmDataLakeStoreItemContent
- Removido o alias da propriedade preterida `Tags` dos cmdlets `New-AzDataLakeStoreAccount` e `Set-AzDataLakeStoreAccount`

  Uso de scripts
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Deve ser alterado para
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Removidas as propriedades preteridas ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier``` e ```FirewallAllowAzureIps``` do objeto ```PSDataLakeStoreAccountBasic```.  Qualquer script que use o ```PSDatalakeStoreAccount``` retornado de ```Get-AzDataLakeStoreAccount``` não deve fazer referência a essas propriedades.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (anteriormente AzureRM.KeyVault)
- A propriedade `PurgeDisabled` foi removida dos objetos `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes` e os Scripts não devem fazer referência à propriedade ```PurgeDisabled``` para tomar decisões de processamento.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (anteriormente AzureRM.Media)
- Removido o alias da propriedade preterida `Tags` dos Scripts cmdlet `New-AzMediaService` sendo usados
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Deve ser alterado para
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (anteriormente AzureRM.Insights)
- Removidos os nomes no plural dos parâmetros `Categories` e `Timegrains` em favor de nomes de parâmetro no singular dos Scripts cmdlet `Set-AzDiagnosticSetting` sendo usados
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Deve ser alterado para
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a>Az.Network (anteriormente AzureRM.Network)
- Removido o parâmetro preterido `ResourceId` do cmdlet `Get-AzServiceEndpointPolicyDefinition`
- Removida a propriedade preterida `EnableVmProtection` do objeto `PSVirtualNetwork`
- Removido o cmdlet preteridos `Set-AzVirtualNetworkGatewayVpnClientConfig`
  
Os scripts não devem mais tomar decisões de processamento com base nos valores desses campos.

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a>Az.OperationalInsights (anteriormente AzureRM.OperationalInsights)
- O conjunto de parâmetros padrão para `Get-AzOperationalInsightsDataSource` foi removido, e `ByWorkspaceNameByKind` tornou-se o conjunto de parâmetros padrão

  Os scripts que listavam as fontes de dados sendo usadas
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  Devem ser alterados para especificar um Kind
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a>Az.RecoveryServices (anteriormente AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)
- Removido o parâmetro `Encryption` do cmdlet `New/Set-AzRecoveryServicesAsrPolicy`
- O parâmetro `TargetStorageAccountName` agora é obrigatório para restaurações de disco gerenciado no cmdlet `Restore-AzRecoveryServicesBackupItem`
- Removidos os parâmetros `StorageAccountName` e `StorageAccountResourceGroupName` no cmdlet `Restore-AzRecoveryServicesBackupItem`
- Removido o parâmetro `Name` no cmdlet `Get-AzRecoveryServicesBackupContainer`

### <a name="azresources-previously-azurermresources"></a>Az.Resources (anteriormente AzureRM.Resources)
- Removido o parâmetro `Sku` do cmdlet `New/Set-AzPolicyAssignment`
- Removido o parâmetro de `Password` das Senhas cmdlets `New-AzADServicePrincipal` e `New-AzADSpCredential` automaticamente geradas, nos scripts que forneciam a senha:
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Devem ser alterados para recuperar a senha da saída:
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (anteriormente AzureRM.ServiceFabric)
- Os seguintes tipos de retorno de cmdlet foram alterados:
  - A propriedade `SerivceTypeHealthPolicies` do tipo `ApplicationHealthPolicy` foi removida.
  - A propriedade `ApplicationHealthPolicies` do tipo `ClusterUpgradeDeltaHealthPolicy` foi removida.
  - A propriedade `OverrideUserUpgradePolicy` do tipo `ClusterUpgradePolicy` foi removida.
  - Essas alterações afetam os seguintes cmdlets:
    - Add-AzServiceFabricClientCertificate
    - Add-AzServiceFabricClusterCertificate
    - Add-AzServiceFabricNode
    - Add-AzServiceFabricNodeType
    - Get-AzServiceFabricCluster
    - Remove-AzServiceFabricClientCertificate
    - Remove-AzServiceFabricClusterCertificate
    - Remove-AzServiceFabricNode
    - Remove-AzServiceFabricNodeType
    - Remove-AzServiceFabricSetting
    - Set-AzServiceFabricSetting
    - Set-AzServiceFabricUpgradeType
    - Update-AzServiceFabricDurability
    - Update-AzServiceFabricReliability

### <a name="azsql-previously-azurermsql"></a>Az.Sql (anteriormente AzureRM.Sql)
- Removidos os parâmetros `State` e `ResourceId` do cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Removidos os cmdlets preteridos: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`
- Removido o parâmetro preterido `Current` do cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`
- Removido o parâmetro preterido `DatabaseName` do cmdlet `Get-AzSqlServerServiceObjective`
- Removido o parâmetro preterido `PrivilegedLogin` do cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a>Az.Storage (anteriormente Azure.Storage e AzureRM.Storage)
- Para dar suporte à criação de um contexto de armazenamento Oauth com apenas o nome da conta de armazenamento, o conjunto de parâmetros padrão foi alterado para `OAuthParameterSet`
  - Exemplo: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`
- O parâmetro `Location` agora é obrigatório no cmdlet `Get-AzStorageUsage`
- Os métodos da API de armazenamento agora usam o padrão assíncrono baseado em tarefas (TAP), em vez de chamadas à API síncronas.
#### <a name="1-blob-snapshot"></a>1. Instantâneo de Blob
##### <a name="before"></a>Antes:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a>Depois:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a>2. Compartilhar instantâneo
##### <a name="before"></a>Antes:
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a>Depois:
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a>3. Restaurar um blob de exclusão reversível
##### <a name="before"></a>Antes:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a>Depois:
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a>4. Definir camada do Blob
##### <a name="before"></a>Antes:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a>Depois:
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (anteriormente AzureRM.Websites)
- Removidas as propriedades preteridas `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite` dos objetos
