---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
ms.locfileid: "33911996"
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

---

## <a name="600---may-2018"></a>6.0.0 - maio de 2018

### <a name="general"></a>Geral
* Definir dependência mínima de módulos do PowerShell 5.0

### <a name="azurestorage"></a>Azure.Storage
* Suporte como nome do contêiner de blob de armazenamento
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Corrija o problema que a saída de algumas falhas de cmdlets de Armazenamento não contém informações de falhas de detalhes

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Apresenta várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermautomation"></a>AzureRM.Automation
* Remover o alias “Marcas” preterido dos cmdlets
    - 'Set-AzureRmAutomationRunbook'

### <a name="azurermbatch"></a>AzureRM.Batch
* Documentação de New-AzureBatchPool atualizada para remover o exemplo preterido

### <a name="azurermcdn"></a>AzureRM.Cdn
* Apresenta várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermcompute"></a>AzureRM.Compute
* Saída detalhada de 'New-AzureRmVm' e 'New-AzureRmVmss' dos parâmetros de suporte
* 'New-AzureRmVm' e 'New-AzureRmVmss' (conjunto de parâmetros simples) suportam a atribuição de identidades definidas pelo usuário e/ou definidas pelo sistema para as VMs.
* Recurso de reimplantação de VMSS e PerformMaintenance
    -  Adicionar um novo parâmetro de opção -Reimplantação e -PerformMaintenance a 'Set-AzureRmVmss' e 'Set-AzureRmVmssVM'
* Adicionar o parâmetro de opção DisableVMAgent ao cmdlet 'Set-AzureRmVMOperatingSystem'
* “New-AzureRmVm” e “New-AzureRmVmss” (conjunto de parâmetro simples) oferece suporte a uma imagem “Win10”.
* O cmdlet 'Repair-AzureRmVmssServiceFabricUpdateDomain' é adicionado.
* Apresenta várias alterações de falha
    - Consulte o guia de migração para obter mais detalhes
* 'Set-AzureRmVmDiskEncryptionExtension' torna os parâmetros do AAD opcionais

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Remover o alias “Marcas” preterido dos cmdlets
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Versão atualizada do SDK do .Net ADF para versão prévia 0.7.0 que contém as seguintes alterações:
    - Parâmetros de execução adicional e a propriedade de gerenciadores de conexão na atividade de ExecuteSSISPackage
    - PostgreSql atualizado, serviço vinculado do MySql para usar a cadeia de conexão completa em vez de servidor, banco de dados, esquema, nome de usuário e senha
    - Removido o esquema do serviço vinculado do DB2
    - Propriedade de esquema removido do serviço vinculado de Teradata
    - Adição do LinkedService, Dataset e CopySource para Responsys

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Remover o alias “Marcas” preterido dos cmdlets
    - 'Novo AzureRmDataLakeAnalyticsAccount'
    - 'Set-AzureRmDataLakeAnalyticsAccount'

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Adicionar o novo recurso de alteração de Acl recursiva para Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Adicionar um novo cmdlet para recuperar o resumo do conteúdo em um diretório
* Adicionar um novo cmdlet para recuperar o uso do disco e despejo de Acl
* Corrigir tipo de retorno do bool Set-AzureRmDataLakeStoreItemAcl para IEnumerable<DataLakeStoreItemAce>
* Corrigir tipo de retorno do bool Set-AzureRmDataLakeStoreItemAclEntry para IEnumerable<DataLakeStoreItemAce>
* Alterações de falha no Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem e Remove-AzureRmDataLakeStoreItem

### <a name="azurermdns"></a>AzureRM.Dns
* Apresenta várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermeventhub"></a>AzureRM.EventHub
* Ajuda atualizada para os cmdlets com exemplos ausentes

### <a name="azurerminsights"></a>AzureRM.Insights
* Apresentou várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermiothub"></a>AzureRM.IotHub
* Habilitar marcas e Sku básico para o IotHub

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Alterações de falha para dar suporte a cenários de redirecionamento
* Adicionados novos cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval e Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Remover o alias “Marcas” preterido dos cmdlets
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Remover o alias “Marcas” preterido dos cmdlets
    - 'Set-AzureRmMediaService'

### <a name="azurermnetwork"></a>AzureRM.Network
* Adicionar suporte ao recurso do plano de proteção contra DDoS
* Apresentou várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Apresenta várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Apresenta várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermprofile"></a>AzureRM.profile
* Habilitar salvamento automático de contexto por padrão
* Adicionar propriedades USGovernmentOperationalInsightsEndpoint e USGovernmentOperationalInsightsEndpointResourceId ao ambiente do Azure para o Governos dos Estados Unidos.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Cabeçalho de Autenticação nos cenários do SiteRecovery

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Apresentou várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermresources"></a>AzureRM.Resources
* Remover parâmetro obsoleto -AtScopeAndBelow da chamada Get-AzureRmRoledefinition
* Incluir atribuições para USers/Groups/ServicePrincipals excluído no resultado Get-AzureRmRoleAssignment
* Adicionar completadores Guia para Escopo e ResourceType
* Adicionar cmdlet de conveniência para criar ServicePrincipals
* Mesclar a funcionalidade Get- e Find- em Get-AzureRmResource
* Adicionar Cmdlets do AD:
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Atualizar sku de versão de imagem padrão do Linux
  - Atualização de sku padrão NewAzureServiceFabricCluster.cs do UbuntuServer1604

### <a name="azurermstorage"></a>AzureRM.Storage
* Apresentou várias alterações de falha
    - Consulte o guia de migração para obter mais informações

### <a name="azurermwebsites"></a>AzureRM.Websites
* Atualizar para a versão mais recente do SDK de sites
* Propriedades adicionadas de -AssignIdentity e -Httpsonly para Set-AzureRmWebApp e Set-AzureRmWebAppSlot
* Adicionados dois novos cmdlets: Get-AzureRmWebAppSnapshots e Restore-AzureRmWebAppSnapshot
