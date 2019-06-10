---
title: Todas as alterações do AzureRM para o Azure PowerShell Az 1.0.0
description: Este guia de migração contém uma lista de alterações significativas criadas para o Azure PowerShell na versão de lançamento 1 do Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: de07565efa98409c6b00cf5fda3417c618d6586b
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498215"
---
# <a name="breaking-changes-for-az-100"></a>Alterações da falha para Az 1.0.0

Este documento fornece informações detalhadas sobre as alterações entre o AzureRM 6.x e o novo módulo Az, versão 1.x e posterior. O sumário ajudará a orientá-lo por um caminho de migração completa, incluindo alterações específicas do módulo que possam afetar seus scripts.

Para obter orientações gerais sobre como iniciar uma migração do AzureRM para o Az, confira [Iniciar uma migração do AzureRM para o Az](migrate-from-azurerm-to-az.md).

> [!IMPORTANT]
> Houve alterações da falha entre o Az 1.0.0 e o Az 2.0.0. Depois de seguir este guia para a atualização do AzureRM para o Az, confira as [alterações da falha do Az 2.0.0](migrate-az-2.0.0.md) para descobrir se você precisa fazer alterações adicionais.

## <a name="table-of-contents"></a>Sumário

- [Alterações da falha gerais](#general-breaking-changes)
  - [Alterações de prefixo de substantivo do cmdlet](#cmdlet-noun-prefix-changes)
  - [Alterações de nome de módulo](#module-name-changes)
  - [Módulos removidos](#removed-modules)
  - [Windows PowerShell 5.1 e .NET 4.7.2](#windows-powershell-51-and-net-472)
  - [Remoção temporária de logon de usuário usando PSCredential](#temporary-removal-of-user-login-using-pscredential)
  - [Logon de código de dispositivo padrão em vez de prompt do navegador da Web](#default-device-code-login-instead-of-web-browser-prompt)
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

Esta seção fornece detalhes sobre as alterações gerais da falha que fazem parte do novo design do módulo Az.

### <a name="cmdlet-noun-prefix-changes"></a>Alterações de prefixo de substantivo do cmdlet

No módulo AzureRM, os cmdlets usavam `AzureRM` ou `Azure` como prefixo de substantivo.  O Az simplifica e normaliza os nomes dos cmdlets, de modo que todos os cmdlets usem 'Az' como seu prefixo de substantivo do cmdlet. Por exemplo:

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

Foi alterado para:

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

Para simplificar a transição para esses novos nomes de cmdlets, o Az introduz dois novos cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) e [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).  `Enable-AzureRmAlias` cria aliases para os nomes de cmdlets mais antigos no AzureRM que são mapeados para os nomes de cmdlets mais recentes do Az. O uso do argumento `-Scope` com `Enable-AzureRmAlias` permite que você escolha em que local os aliases serão habilitados.

Por exemplo, o script a seguir no AzureRM:

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Pode ser executado com alterações mínimas usando `Enable-AzureRmAlias`:

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

A execução de `Enable-AzureRmAlias -Scope CurrentUser` habilitará os aliases para todas as sessões do PowerShell, para que, após a execução desse cmdlet, um script como este não precise ser alterado:

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

Para obter detalhes completos sobre o uso dos cmdlets de alias, confira a [referência de Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

Quando você estiver pronto para desabilitar os aliases, `Disable-AzureRmAlias` removerá os aliases criados. Para obter detalhes completos, confira a [referência de Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Ao desabilitar os aliases, verifique se eles estão desabilitados para _todos_ os escopos que tinham aliases habilitados.

### <a name="module-name-changes"></a>Alterações de nome de módulo

Os nomes do módulo foram alterados de `AzureRM.*` para `Az.*`, exceto para os seguintes módulos:

| Módulo AzureRM | Módulo Az |
|----------------|-----------|
| Azure.Storage | Az.Storage |
| Azure.AnalysisServices | Az.AnalysisServices |
| AzureRM.profile | Az.Accounts |
| AzureRM.Insights | Az.Monitor |
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |
| AzureRM.Tags | Az.Resources |
| AzureRM.MachineLearningCompute | Az.MachineLearning |
| AzureRM.UsageAggregates | Az.Billing |
| AzureRM.Consumption | Az.Billing |

As alterações nos nomes dos módulos significam que qualquer script que usa `#Requires` ou `Import-Module` para carregar módulos específicos precisarão ser alterados para usar o novo módulo. Para os módulos em que o sufixo do cmdlet não foi alterado, isso significa que, embora o nome do módulo tenha sido alterado, isso _não_ ocorreu com o sufixo que indica o espaço da operação.

#### <a name="migrating-requires-and-import-module-statements"></a>Como migrar as instruções #Requires e Import-Module

Os scripts que usam `#Requires` ou `Import-Module` para declarar uma dependência de módulos AzureRM precisam ser atualizados para usar os novos nomes de módulos. Por exemplo:

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

Deve ser alterado para:

```azurepowershell-interactive
#Requires -Module Az.Compute
```

Para `Import-Module`:

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

Deve ser alterado para:

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a>Migração de invocações de cmdlet totalmente qualificadas

Os scripts que usam as invocações de cmdlet qualificadas por módulo, como:

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

Precisam ser alterados para usar os novos nomes de módulos e cmdlets:

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a>Como migrar dependências de manifesto de módulo

Os módulos que expressam dependências de módulos AzureRM por meio de um arquivo de manifesto (.psd1) de módulo precisarão atualizar os nomes de módulos em sua seção `RequiredModules`:

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

Precisa ser alterado para:

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a>Módulos removidos

Os seguintes módulos foram removidos:

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

Não há mais suporte ativo para as ferramentas desses serviços.  Os clientes são incentivados a mudar para serviços alternativos, assim que for conveniente.

### <a name="windows-powershell-51-and-net-472"></a>Windows PowerShell 5.1 e .NET 4.7.2

O uso do Az com o PowerShell 5.1 para Windows exige a instalação do .NET Framework 4.7.2. O uso do PowerShell Core 6.x ou posterior não exige o .NET Framework.

### <a name="temporary-removal-of-user-login-using-pscredential"></a>Remoção temporária de logon de usuário usando PSCredential

Devido a alterações no fluxo de autenticação para o .NET Standard, estamos temporariamente removendo o logon de usuário por meio do PSCredential. Essa funcionalidade será introduzida novamente na versão de 15/1/2019 do PowerShell 5.1 para Windows. Isso é abordado detalhadamente [neste problema do GitHub.](https://github.com/Azure/azure-powershell/issues/7430)

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a>Logon de código de dispositivo padrão em vez de prompt do navegador da Web

Devido a alterações no fluxo de autenticação para o .NET Standard, estamos usando o logon do dispositivo como o fluxo de logon padrão durante o logon interativo. O logon baseado em navegador da Web será reintroduzido no PowerShell 5.1 para Windows como o padrão na versão de 15/1/2019. Nesse momento, os usuários poderão escolher logon de dispositivo usando um parâmetro Switch.

## <a name="module-breaking-changes"></a>Alterações de falhas para módulos

Esta seção fornece detalhes sobre alterações específicas da falha para cmdlets e módulos individuais.

### <a name="azapimanagement-previously-azurermapimanagement"></a>Az.ApiManagement (anteriormente AzureRM.ApiManagement)

- Remoção dos seguintes cmdlets:
  - New-AzureRmApiManagementHostnameConfiguration
  - Set-AzureRmApiManagementHostnames
  - Update-AzureRmApiManagementDeployment
  - Import-AzureRmApiManagementHostnameCertificate
  - Use o cmdlet **Set-AzApiManagement** para definir essas propriedades
- Remoção das seguintes propriedades:
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
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  Deve ser alterado para
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- Removidas as propriedades preteridas `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier` e `FirewallAllowAzureIps` do objeto `PSDataLakeStoreAccountBasic`.  Qualquer script que use o `PSDatalakeStoreAccount` retornado de `Get-AzDataLakeStoreAccount` não deve fazer referência a essas propriedades.

### <a name="azkeyvault-previously-azurermkeyvault"></a>Az.KeyVault (anteriormente AzureRM.KeyVault)

- A propriedade `PurgeDisabled` foi removida dos objetos `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes` e os Scripts não devem fazer referência à propriedade ```PurgeDisabled``` para tomar decisões de processamento.

### <a name="azmedia-previously-azurermmedia"></a>Az.Media (anteriormente AzureRM.Media)

- Removido o alias da propriedade preterida `Tags` dos Scripts cmdlet `New-AzMediaService` sendo usados
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  Deve ser alterado para
  ```azurepowershell-interactive
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a>Az.Monitor (anteriormente AzureRM.Insights)

- Removidos os nomes no plural dos parâmetros `Categories` e `Timegrains` em favor de nomes de parâmetro no singular dos Scripts cmdlet `Set-AzDiagnosticSetting` sendo usados
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  Deve ser alterado para
  ```azurepowershell-interactive
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
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  Devem ser alterados para especificar um Kind
  ```azurepowershell-interactive
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

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  Devem ser alterados para recuperar a senha da saída:

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a>Az.ServiceFabric (anteriormente AzureRM.ServiceFabric)

- Os seguintes tipos de retorno de cmdlet foram alterados:
  - A propriedade `ServiceTypeHealthPolicies` do tipo `ApplicationHealthPolicy` foi removida.
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
- Os métodos da API de armazenamento agora usam o padrão assíncrono baseado em tarefas (TAP), em vez de chamadas à API síncronas. Os seguintes exemplos demonstram os novos comandos assíncronos:

#### <a name="blob-snapshot"></a>Instantâneo de Blob

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

Az:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a>Compartilhar instantâneo

AzureRM:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

Az:

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a>Cancelar a exclusão de blob com exclusão reversível

AzureRM:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

Az:

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a>Definir camada do Blob

AzureRM:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

Az:

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a>Az.Websites (anteriormente AzureRM.Websites)

- Removidas as propriedades preteridas `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite` dos objetos
