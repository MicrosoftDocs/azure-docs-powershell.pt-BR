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
ms.openlocfilehash: 3961f5c37869d0dc877b85bad535f399181040db
ms.sourcegitcommit: fd11600079ee3844986552bccc4e274a231332b6
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/02/2018
ms.locfileid: "39368170"
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

---
## <a name="660---july-2018"></a>6.6.0 – Julho de 2018
#### <a name="general"></a>Geral
* Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.

#### <a name="azurermprofile"></a>AzureRM.profile
* Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino. O padrão é sempre true, recursos individuais e substituição do padrão.
* Tipos de ps1xml adicionados a Common.Storage

#### <a name="azurestorage"></a>Azure.Storage
* Suporte à obtenção do contexto de armazenamento de DefaulfProfile
* Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets.

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6370
    - Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6515
    - Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação
* Problema corrigido https://github.com/Azure/azure-powershell/issues/6560
    - Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId

#### <a name="azurermcompute"></a>AzureRM.Compute
* Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.
* Corrigir o cmdlet Invoke-AzureRmVMRunCommand
* Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.  (O parâmetro ResouceGroupName agora é opcional.)
* Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.
* Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.
* Atualizar exemplo de New-AzureRmDisk
* Adicionar exemplo de 'New-AzureRmVM'
* Atualizar descrição de Set-AzureRmVMOSDisk
* Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo. 

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Atualizado a versão do SDK do .NET do ADF para 1.1.0.
* Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.
     - Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.
     - Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Tubulação atualizada para InputObject e ResourceId em Remover cmdlets

#### <a name="azurerminsights"></a>AzureRM.Insights
* Formatação corrigida do OutputType nos arquivos de ajuda
* Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.

#### <a name="azurermresources"></a>AzureRM.Resources
* Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'
    - https://github.com/Azure/azure-powershell/issues/6765
* Corrigir o cenário de tubulação com 'Set-AzureRmResource'

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Tubulação atualizada para InputObject e ResourceId em Remover cmdlets
* alguns problemas corrigidos
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a>AzureRM.Sql
* Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:
    - Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy
* Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:
    - Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings
    - Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline
    - Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan
* Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule
* Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog

#### <a name="azurermstorage"></a>AzureRM.Storage
* Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets
* Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela
    - Get-AzureRmStorageAccount
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermtags"></a>AzureRM.Tags
* Remover instrução incorreta de ajuda de cmdlet de marca
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a>6.5.0 - julho de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'

#### <a name="azurestorage"></a>Azure.Storage
* Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação
- Set-AzureStorageBlobContent
- Set-AzureStorageFileContent

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Adicione a propriedade necessária ResourceGroupName ao AS.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'

#### <a name="azurermcompute"></a>AzureRM.Compute
* Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet
* Adicionar exemplo do 'Add-AzureRmVmssExtension'
* Adicionar exemplos do 'Remove-AzureRmVmssExtension'
* Atualizar ajuda do 'Set-AzureRmVMAccessExtension'
* Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp

#### <a name="azurermnetwork"></a>AzureRM.Network
* Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering
* Atualizados os cmdlets abaixo para o Gateway de Aplicativo
    - New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas
    - New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2
    - Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2
* Cmdlets de RouteTable regenerados com a versão mais recente do gerador

#### <a name="azurermrelay"></a>AzureRM.Relay
* Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo

#### <a name="azurermresources"></a>AzureRM.Resources
* Atualize os cmdlets Roleassignment e roledefinition:
    - Remova chamadas extras roledefinition feitas como parte da paginação.
* Corrigir cmdlet Get-AzureRmRoleAssignment
    - Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups
* Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Adicionado o parâmetro top e skip aos cmdlets de lista
* Adicionados os cmdlets de migração de NameSpace Standard a Premium:
    - Start-AzureRmServiceBusMigration
    - Get-AzureRmServiceBusMigration
    - Complete-AzureRmServiceBusMigration
    - Stop-AzureRmServiceBusMigration
    - Remove-AzureRmServiceBusMigration
* Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Exemplo de atualização para 'New-AzureRmServiceFabricCluster'

#### <a name="azurermsql"></a>AzureRM.Sql
* Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada
    - Add-AzureRmSqlServerTransparentDataEncryptionCertificate
    - Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate

#### <a name="azurermwebsites"></a>AzureRM.Websites
* `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.
* Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados
* `Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida

## <a name="640---july-2018"></a>6.4.0 - julho de 2018
#### <a name="general"></a>Geral
* Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos

#### <a name="azurermprofile"></a>AzureRM.profile
* Atributo Ps1Xml adicionado aos tipos de saída básicos

#### <a name="azurermcompute"></a>AzureRM.Compute
* Recurso de Marca do IP para VMSS
    - O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado
    - O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig
* Recurso de Reversão Automática do SO para VMSS
    - Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss
* Recurso do Histórico de Atualizações do SO para Vmss
    - O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Adicione suporte para as ACLs de Catálogo com os comandos a seguir:
    - Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry
    - Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties
* Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas
* Corrigir local de teste dos cmdlets DataLake

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup
* Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub. Conjunto de Parâmetros Padrão fornecido.
* Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag

#### <a name="azurermnetwork"></a>AzureRM.Network
* Expor novas Skus para Zone-Redundant VirtualNetworkGateways
* Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM
    - Get-AzureRmExpressRouteCrossConnection adicionado
    - Set-AzureRmExpressRouteCrossConnection adicionado
    - Add-AzureRmExpressRouteCrossConnectionPeering adicionado
    - Get-AzureRmExpressRouteCrossConnectionPeering adicionado
    - Remove-AzureRmExpressRouteCrossConnectionPeering adicionado
    - Get-AzureRMExpressRouteCrossConnectionArpTable adicionado
    - Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado
    - Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado. Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura. Se houver tal cofre, o cmdlet produzirá detalhes dele.

#### <a name="azurermresources"></a>AzureRM.Resources
* Atualize os cmdlets Get-AzureRmPolicyAssignment:
    - Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento
    - Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento
    - Adicionar argumentos -Effective e -All para controlar  parâmetro
* Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition
    - Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento
    - Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura
* Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition
    - Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento
    - Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura
* Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”
* Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”
    - https://github.com/Azure/azure-powershell/issues/6505
* Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.

#### <a name="azurermsql"></a>AzureRM.Sql
* Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint
* Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets

## <a name="630---june-2018"></a>6.3.0 - junho de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave
* Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior

#### <a name="azurestorage"></a>Azure.Storage
* Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.

#### <a name="azurermcompute"></a>AzureRM.Compute
* “Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados 
* Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir
    - Grant-AzureRmDiskAccess
    - Grant-AzureRmSnapshotAccess
    - Save-AzureRmVMImage
* Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":
    - Start-AzureRmVM
    - Stop-AzureRmVM
    - Restart-AzureRmVM
    - Set-AzureRmVM
    - Remove-AzureRmVM
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
* Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag

#### <a name="azurermpolicyinsights"></a>AzureRM.PolicyInsights
* Versão pública dos cmdlets de Informações sobre a Política
    - Usar versão da API 2018-04-04
    - Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup. Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.

#### <a name="azurermsql"></a>AzureRM.Sql
* Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig

#### <a name="azurermwebsites"></a>AzureRM.Websites
* "Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity
* "New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional

## <a name="621---june-2018"></a>6.2.1 - junho de 2018
### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro

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