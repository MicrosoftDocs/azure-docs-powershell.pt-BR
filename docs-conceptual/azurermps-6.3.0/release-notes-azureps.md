---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237560"
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

---
## <a name="630---june-2018"></a>6.3.0 - Junho de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave
* Criar um contexto para cada assinatura ao executar 'Connect-AzureRmAccount' sem contexto anterior

#### <a name="azurestorage"></a>Azure.Storage
* Adição de outras informações sobre o parâmetro -Permissions nos arquivos de ajuda.

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'Get-AzureRmVmDiskEncryptionStatus' corrige um problema observado por VMs sem discos de dados 
* Atualizar a versão da biblioteca de clientes de computação para corrigir os cmdlets a seguir
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Correção dos cmdlets a seguir para mostrar corretamente o "ID da operação" e o "status da operação":
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzuerRmVM
    - Set-AzureRmVmss
    - Start-AzureRmVmssRollingOSUpgrade
    - Stop-AzureRmVmssRollingUpgrade
    - Start-AzureRmVmss
    - Restart-AzureRmVmss
    - Stop-AzureRmVmss
    - Remove-AzureRmVmss
    - ConvertTo-AzureRmVMManagedDisk
    - Revoke-AzureRmSnapshotAccess
    - Remove-AzureRmSnapshot
    - Revoke-AzureRmDiskAccess
    - Remove-AzureRmDisk
    - Remove-AzureRmContainerService
    - Remove-AzureRmAvailabilitySet

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Remoção das condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription a fim de permitir a mudança desses parâmetros para uma cadeia vazia, se for necessário.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Correção do problema em que nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Versão pública de cmdlets do Policy Insights
    - Usar a versão da API 2018-04-04
    - Adição de PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Adição do parâmetro -Vault aos cmdlets RecoveryServices.Backup. Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Atualização do arquivo de ajuda para Add-AzureRmTrafficManagerEndpointConfig

#### <a name="azurermwebsites"></a>AzureRM.Websites
* "Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity
* "New-AzureRmWebAppSlot" foi atualizado para honrar AppServicePlan como um parâmetro opcional

## <a name="621---june-2018"></a>6.2.1 - Junho de 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Atualização do modelo PSWorkspace para permitir que a Rede use o tipo como um parâmetro

## <a name="620---june-2018"></a>6.2.0 - Junho de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo

#### <a name="azurermcompute"></a>AzureRM.Compute
* Recurso de atualização de VM VMSS
    - Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados
    - Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:
    - A operação para Configurar o repositório de fábrica foi adicionada
    - O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret
    - Vários tipos de modelo atualizados de SecretBase para Object
    - Foram adicionados gatilho de eventos de blob

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Atualizar documentação com a saída de exemplo

### <a name="azurermnetwork"></a>AzureRM.Network
* Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede

#### <a name="azurermresources"></a>AzureRM.Resources
* Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação

### <a name="azurermsql"></a>AzureRM.Sql
* Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermwebsites"></a>AzureRM.Websites
* 'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.

## <a name="610---may-2018"></a>6.1.0 - maio de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Habilite as operações de associação/desassociação do Gateway no sistema autônomo.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions
* Suporte adicionado para Back-end do ServiceFabric
* Suporte adicionado para Agente do Application Insights
* Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api
* Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA
* Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy
* Suporte adicionado para a identidade MSI
* Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão
   - Import-AzureRmApiManagementHostnameCertificate
   - New-AzureRmApiManagementHostnameConfiguration
   - Set-AzureRmApiManagementHostnames
   - Update-AzureRmApiManagementDeployment

#### <a name="azurermbatch"></a>AzureRM.Batch
* Versão do novo cmdlet Get-AzureBatchPoolNodeCounts
* Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload

#### <a name="azurermconsumption"></a>AzureRM.Consumption
* Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties
* Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry 
* Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry 

#### <a name="azurermnetwork"></a>AzureRM.Network
* Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview
* Cmdlet adicionado para criar a configuração de protocolo
    - New-AzureRmNetworkWatcherProtocolConfiguration
* Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.
    - Add-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.
    - Remove-AzureRmExpressRouteCircuitConnectionConfig
* Cmdlet adicionado para recuperar uma conexão de circuito
    - Get-AzureRmExpressRouteCircuitConnectionConfig

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)

#### <a name="azurermsql"></a>AzureRM.Sql
* Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups
* Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política. Envie a solicitação com a nova política de retenção flexível”.
* Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.
* Os cmdlets atualizados, incluindo: 
    - New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase
    - New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool
    - New-AzureRmSqlDatabaseCopy
    - New-AzureRmSqlDatabaseSecondary
    - Restore-AzureRmSqlDatabase

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.