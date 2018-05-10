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
ms.date: 2/20/2018
ms.openlocfilehash: 2e80d314991539cb630a0f2a96048bb2e70a05b6
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

---

# <a name="azure-powershell-570"></a>Azure PowerShell 5.7.0

Instalador do Azure PowerShell 5.7.0: [link](https://github.com/Azure/azure-powershell/releases/download/v5.7.0-April2018/azure-powershell.5.7.0.msi)

Módulo de galeria para cmdlets do ARM: [link](https://www.powershellgallery.com/packages/AzureRM/5.7.0)

Para instalar o `AzureRM` da Galeria do PowerShell, execute o seguinte comando:

```powershell
Install-Module -Name AzureRM -Repository PSGallery -Force
```

Para atualizar a partir de uma versão mais antiga do `AzureRM`, execute o seguinte comando:

```powershell
Update-Module -Name AzureRM
```

## <a name="changes-since-last-release"></a>Alterações desde a última versão

#### <a name="general"></a>Geral
* Atualização para a versão mais recente do ClientRuntime do Azure

#### <a name="azurestorage"></a>Azure.Storage
* Correção do problema em que há falha nos cmdlets de carregamento de Blobs e de arquivo em computadores com a política FIPS habilitada
    - Set-AzureStorageBlobContent
    - Set-AzureStorageFileContent

#### <a name="azurermbilling"></a>AzureRM.Billing
* Novo cmdlet Get-AzureRmEnrollmentAccount
  - cmdlet para recuperar contas de registro

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integração ao SDK de Gerenciamento dos Serviços Cognitivos versão 4.0.0.
* Adição da operação Get-AzureRmCognitiveServicesAccountUsage.

#### <a name="azurermcompute"></a>AzureRM.Compute
* `Get-AzureRmVmssDiskEncryptionStatus` oferece suporte ao status de criptografia no nível de disco de dados
* `Get-AzureRmVmssVmDiskEncryptionStatus` oferece suporte ao status de criptografia no nível de disco de dados
* Atualização para zona resiliente
* “New-AzureRmVm” e “New-AzureRmVmss” (conjunto de parâmetro simples) oferece suporte para zonas de disponibilidade.

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Desacoplamento de dependência em SDKs de Commands.Resources.Rest e de ARM/armazenamento.

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Adição de funcionalidades de depuração
* Atualização da versão do SDK de plano de dados do ADLS para 1.1.2
* Export-AzureRmDataLakeStoreItem – preterimento dos parâmetros PerFileThreadCount e ConcurrentFileCount e introdução do parâmetro Concurrency
* Import-AzureRMDataLakeStoreItem – preterimento dos parâmetros PerFileThreadCount e ConcurrentFileCount e introdução do parâmetro Concurrency
* Get-AzureRMDataLakeStoreItemContent – correção do comportamento da parte final para conteúdos maiores que 4 MB
* Set-AzureRMDataLakeStoreItemExpiry – introdução do novo conjunto de parâmetro SetRelativeExpiry para definição de tempo de expiração relativo
* Remove-AzureRmDataLakeStoreItem - preterimento do parâmetro Clean.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Correção de AlternameName em New-AzureRmEventHubGeoDRConfiguration

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Atualização de cmdlets para incluir os cenários de redirecionamento
* Adição de mensagens de preterimento para futuras versões com alteração de falha

#### <a name="azurermnetwork"></a>AzureRM.Network
* Correção de mensagem de erro com cmdlets de rede

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Adição de “propriedades” em CorrelationFilter de regras para oferecer suporte a customproperties
* Atualização da ajuda de New-AzureRmServiceBusGeoDRConfiguration e correção da saída do cmdlet de Regras
* Correção das propriedades do encaminhamento automático nos cmdlets New-AzureRmServiceBusQueue e New-AzureRmServiceBusSubscription

#### <a name="azurermsql"></a>AzureRM.Sql
* Adição de novo cmdlet 'Stop-AzureRmSqlElasticPoolActivity' para oferecer suporte ao cancelamento de operações assíncronas no pool elástico
* Atualização das respostas para cmdlets Get-AzureRmSqlDatabaseActivity e Get-AzureRmSqlElasticPoolActivity para refletir mais informações na resposta

Alterações desde a última versão: https://github.com/Azure/azure-powershell/compare/v5.6.0-March2018...v5.7.0-April2018

## <a name="560---march-2018"></a>5.6.0 - Março de 2018

#### <a name="general"></a>Geral
* Correção do problema com o Grupo de Recursos Padrão no CloudShell
* Correção do problema em que os scripts de inicialização estavam sendo executados incorretamente durante a importação do módulo

#### <a name="azurermprofile"></a>AzureRM.profile
* Habilitação da autenticação MSI em cenários sem suporte
* Adição do suporte para a Identidade de Serviço Gerenciado definido pelo usuário

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Correção do problema com a limpeza de scripts na compilação

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Correção do problema com a limpeza de scripts na compilação

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVM' e 'New-AzureRmVMSS' oferecem suporte a discos de dados.
* 'New-AzureRmVM' e 'New-AzureRmVMSS' oferecem suporte a imagem personalizada por nome ou ID.
* Recurso de análise de log
    - Adição do cmdlet 'Export-AzureRmLogAnalyticRequestRateByInterval'
    - Adição do cmdlet 'Export-AzureRmLogAnalyticThrottledRequests'

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Correção de problema de conjuntos de parâmetro para o registro de contêiner e montagem de volume de arquivo do azure

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* SDK do .NET ADF para a versão 0.6.0-preview que contém as seguintes alterações:
    - Adição da nova atividade AzureDatabricks LinkedService e DatabricksNotebook
    - Adição das propriedades headNodeSize e dataNodeSize em HDInsightOnDemand LinkedService
    - Adição de LinkedService, Dataset, CopySource para SalesforceMarketingCloud
    - Adição do suporte para SecureOutput em todas as atividades
    - Adição da nova propriedade BatchCount à atividade ForEach que controla quantas atividades simultâneas executar
    - Adição de uma nova Atividade de Filtro
    - Adição do suporte para Parâmetros de Serviço Vinculado

#### <a name="azurermdns"></a>AzureRM.Dns
* Adição de Zonas DNS Privado (Visualização Pública)
    - Adição da capacidade de criar zonas DNS que são visíveis apenas para as redes virtuais associadas

#### <a name="azurermnetwork"></a>AzureRM.Network
* Atualização dos tipos de modelo para compatibilidade com os cmdlets do DNS.

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Alterações do Azure ASR para o Azure Site Recovery (os cmdlets atualmente oferecem suporte a operações entre Empresas, Empresa para Azure, HyperV para Azure, VMware para Azure)
    - New-AzureRmRecoveryServicesAsrProtectionContainer
    - New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig
    - Remove-AzureRmRecoveryServicesAsrProtectionContainer
    - Update-AzureRmRecoveryServicesAsrProtectionDirection

#### <a name="azurermstorage"></a>AzureRM.Storage
* Obsolescência dos seguintes parâmetros em cmdlets novos e definição de cmdlets da Conta de Armazenamento: EnableEncryptionService e DisableEncryptionService, uma vez que a criptografia na Rest está habilitada por padrão e não pode ser desabilitada.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Correção da Ajuda para Remove-AzureRmWebAppSlot

## <a name="550---march-2018"></a>5.5.0 – Março de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Correção do problema com a importação de aliases
* Carregar a versão 10.0.3 do Newtonsoft.Json lado a lado à versão 6.0.8

#### <a name="azurestorage"></a>Azure.Storage
* Recurso de suporte a exclusão reversível
    - Enable-AzureStorageDeleteRetentionPolicy
    - Disable-AzureStorageDeleteRetentionPolicy
    - Get-AzureStorageBlob

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Correção do problema com a importação de aliases
* Adicione o suporte de firewall e o recurso de expansão e consulta, bem como o suporte da versão da API 2017-08-01.

#### <a name="azurermautomation"></a>AzureRM.Automation
* Correção do problema com a importação de aliases

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Correção do problema com a importação de aliases

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Atualização de notice.txt e da mensagem de aviso.

#### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVMSS' imprime as cadeias de conexão em modo detalhado.
* 'New-AzureRmVmss' oferece suporte a endereço IP público, regras de balanceamento de carga e regras NAT de entrada.
* Recurso WriteAccelerator
    - Adição do parâmetro de opção WriteAccelerator aos seguintes cmdlets: Set-AzureRmVMOSDisk Set-AzureRmVMDataDisk Add-AzureRmVMDataDisk Add-AzureRmVmssDataDisk
    - Adição do parâmetro de opção OsDiskWriteAccelerator ao seguinte cmdlet: Set-AzureRmVmssStorageProfile.
    - Adição do parâmetro booliano OsDiskWriteAccelerator aos seguintes cmdlets: Update-AzureRmVM     Update-AzureRmVmss

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Correção do problema de criptografia de credencial que não causava erro significativo para algumas operações de criptografia
* Permissão do compartilhamento do tempo de execução de integração em data factory

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Adição dos parâmetros "SetupScriptContainerSasUri" e "Edition" para o cmd "Set-AzureRmDataFactoryV2IntegrationRuntime" para permitir a instalação customizada e a funcionalidade de seleção de edição
* Correção do problema de criptografia de credencial que não causava erro significativo para algumas operações de criptografia.
* Permissão do compartilhamento do tempo de execução de integração em data factory

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Correção do problema com a importação de aliases

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Correção do exemplo de Set-AzureRmKeyVaultAccessPolicy

#### <a name="azurermnetwork"></a>AzureRM.Network
* Correção do problema com a importação de aliases

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Correção do problema com a importação de aliases

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Correção do problema com a importação de aliases

#### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Correção do problema com a importação de aliases

#### <a name="azurermresources"></a>AzureRM.Resources
* Correção do problema com a importação de aliases

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Adição da propriedade EnableBatchedOperations à Fila
* Adição da propriedade DeadLetteringOnFilterEvaluationExceptions a Assinaturas

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Atualização de cmdlet do Service Fabric
  - Atualização de modelos do ARM
  - Operações com falha não passam mais por reversão
  - Add-AzureRmServiceFabricNodeType
    - Padrão de VMs para discos gerenciados
    - Usada sub-rede existente de VMSS
    - Todas as operações são idempotentes
  - Remove-AzureRmServiceFabricNodeType limpa VMSS parcialmente criada e/ou tipos de nó de cluster
  - Correção da saída do objeto PSCluster para tipos de propriedade complexos

#### <a name="azurermsql"></a>AzureRM.Sql
* Correção do problema com a importação de aliases
* A resposta de Get-AzureRmSqlServer, New-AzureRmSqlServer e Remove-AzureRmSqlServer agora inclui a propriedade FullyQualifiedDomainName.

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Correção do problema com a importação de aliases
* New-AzureRMWebApp – adição de parâmetro definido para a criação simplificada de WebApp, com suporte a repositório git local.

## <a name="540---february-2018"></a>5.4.0 – Fevereiro de 2018
#### <a name="azurermautomation"></a>AzureRM.Automation
* Adicionado alias do New-AzureRmAutomationModule para o Import-AzureRmAutomationModule

#### <a name="azurermcompute"></a>AzureRM.Compute
* Correção do problema de ErrorAction de alguns cmdlets Get.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Aplicação do SDK do Azure Container Instance 2018-02-01
    - Suporte ao rótulo de nome DNS

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Correção de todos os cmdlets GET que não estavam funcionando anteriormente.

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Correção do bug na ajuda Get-AzureRmEventHubGeoDRConfiguration

#### <a name="azurermnetwork"></a>AzureRM.Network
* Adição de cmdlet para criar um novo monitor de conexão
    - New-AzureRmNetworkWatcherConnectionMonitor
* Adição de cmdlet para atualizar um monitor de conexão
    - Set-AzureRmNetworkWatcherConnectionMonitor
* Adição de cmdlet para obter o monitor de conexão ou a lista do monitor de conexão
    - Get-AzureRmNetworkWatcherConnectionMonitor
* Adição de cmdlet para consultar um monitor de conexão
    - Get-AzureRmNetworkWatcherConnectionMonitorReport
* Adição de cmdlet para iniciar um monitor de conexão
    - Start-AzureRmNetworkWatcherConnectionMonitor
* Adição de cmdlet para interromper um monitor de conexão
    - Stop-AzureRmNetworkWatcherConnectionMonitor
* Adição de cmdlet para remover um monitor de conexão
    - Remove-AzureRmNetworkWatcherConnectionMonitor
* Atualização da documentação do Set-AzureRmApplicationGatewayBackendAddressPool para remover o exemplo preterido
* Adição do sinalizador EnableHttp2 no Gateway de Aplicativo
    - Atualização do New-AzureRmApplicationGateway: adição do parâmetro opcional -EnableHttp2
* Adição de IpTags ao PublicIpAddress
    - Atualização do cmdlet New-AzureRmPublicIpAddress: adição do IpTags
    - New-AzureRmPublicIpTag para adicionar Iptag
* Adição da propriedade DisableBgpRoutePropagation no RouteTable e no effectiveRoute.

#### <a name="azurermresources"></a>AzureRM.Resources
* Register-AzureRmProviderFeature: adição do exemplo ausente nos documentos
* Register-AzureRmResourceProvider: adição do exemplo ausente nos documentos

#### <a name="azurermstorage"></a>AzureRM.Storage
* Obsolescência dos seguintes parâmetros em cmdlets novos e definição de cmdlets da Conta de Armazenamento: EnableEncryptionService e DisableEncryptionService, uma vez que a criptografia na Rest está habilitada por padrão e não pode ser desabilitada.
    - New-AzureRmStorageAccount
    - Set-AzureRmStorageAccount


## <a name="530---february-2018"></a>5.3.0 - Fevereiro de 2018
### <a name="azurermprofile"></a>AzureRM.profile
* Aviso de reprovação adicionado para PowerShell 3 e 4
* `Add-AzureRmAccount` foi renomeado como `Connect-AzureRmAccount`; foi adicionado um alias para o nome antigo do cmdlet e outros aliases (`Login-AzAccount` e `Login-AzureRmAccount`) foram redirecionados para o novo nome do cmdlet.
* `Remove-AzureRmAccount` foi renomeado como `Disconnect-AzureRmAccount`; foi adicionado um alias para o nome antigo do cmdlet e outros aliases (`Logout-AzAccount` e `Logout-AzureRmAccount`) foram redirecionados para o novo nome do cmdlet.
* Cadeias de caracteres de recurso corrigidas para usar `Connect-AzureRmAccount` em vez de `Login-AzureRmAccount`
* `Add-AzureRmEnvironment` e `Set-AzureRmEnvironment`
  - `-AzureOperationalInsightsEndpoint` e `-AzureOperationalInsightsEndpointResourceId` adicionados como parâmetros para uso com RP de plano de dados OperationalInsights.

### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Uso de `Login-AzureRmAccount` corrigido para usar `Connect-AzureRmAccount`

### <a name="azurermcompute"></a>AzureRM.Compute
* Parâmetro `-AvailabilitySetName` adicionado ao parameterset simplificado de `New-AzureRmVM`.
* Uso de `Login-AzureRmAccount` corrigido para usar `Connect-AzureRmAccount`
* Suporte de identidade atribuída ao usuário para VM e conjunto de dimensionamento de VM
    - Os parâmetros `-IdentityType` e `-IdentityId` são adicionados a `New-AzureRmVMConfig`, `New-AzureRmVmssConfig`, `Update-AzureRmVM` e `Update-AzureRmVmss`
* Parâmetro `-EnableIPForwarding` adicionado a `Add-AzureRmVmssNetworkInterfaceConfig`
* Parâmetro `-Priority` adicionado a `New-AzureRmVmssConfig`

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Uso de `Login-AzureRmAccount` corrigido para usar `Connect-AzureRmAccount`

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Uso de `Login-AzureRmAccount` corrigido para usar `Connect-AzureRmAccount`
* Mensagem de erro corrigida de `Test-AzureRmDataLakeStoreAccount` ao executar este cmdlet sem ter se conectado a `Login-AzureRmAccount`

### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Atualizado para usar a versão da API “2018-01-01”.

### <a name="azurermeventhub"></a>AzureRM.EventHub

* Adicionado abaixo novos comandos para as operações de recuperação de desastre de replicação geográfica.
  - Criar um novo Alias (Configuração de Recuperação de Desastres):
    - `New-AzureRmEventHubGeoDRConfiguration`
  - Recuperar Alias (Configuração de Recuperação de Desastres):
    - `Get-AzureRmEventHubGeoDRConfiguration`
  - Desabilitar a Recuperação de desastre e interrompe a replicação de alterações de namespaces primários para secundários
    - `Set-AzureRmEventHubGeoDRConfigurationBreakPair`
  - Invocar um failover de Recuperação de Desastres e reconfigurar o alias a fim de apontar para o namespace secundário
    - `Set-AzureRmEventHubGeoDRConfigurationFailOver`
  - Excluir um Alias (configuração de Recuperação de Desastre)
    - `Remove-AzureRmEventHubGeoDRConfiguration`
* Novos comandos adicionados abaixo para verificar o nome do namespace e o nome da configuração GeoDr - disponibilidade de alias.
  - Verifique a disponibilidade do nome do Namespace ou do Alias (configuração de Recuperação de Desastre):
    - `Test-AzureRmEventHubName`

### <a name="azurerminsights"></a>AzureRM.Insights
* Uso de `Login-AzureRmAccount` corrigido para usar `Connect-AzureRmAccount`

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Uso de `Login-AzureRmAccount` corrigido para usar `Connect-AzureRmAccount`

### <a name="azurermnetwork"></a>AzureRM.Network
* Corrija a mensagem de substituição 'Tem certeza de que deseja substituir o recurso'

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Suporte adicionado para a consulta da API V2 por meio de `Invoke-AzureRmOperationalInsightsQuery`. Consulte [https://dev.loganalytics.io/](https://dev.loganalytics.io/) para obter mais informações sobre a nova API.

### <a name="azurermresources"></a>AzureRM.Resources
* `Get-AzureRmADServicePrincipal`: `-ServicePrincipalName` removido do conjunto de parâmetros padrão Vazio porque era redundante com o conjunto de parâmetros SPN

### <a name="azurermservicebus"></a>AzureRM.ServiceBus

* Correção de funcionalidade adicionada para `Remove-AzureRmServiceBusRule` e `Get-AzureRmServiceBusKey`
* Adicionado abaixo novos commandlets para as operações de recuperação de desastre de replicação geográfica.
  - Criar um novo Alias (Configuração de Recuperação de Desastres):
    - `New-AzureRmServiceBusDRConfigurations`
  - Recuperar Alias (Configuração de Recuperação de Desastres):
    - `Get-AzureRmServiceBusDRConfigurations`
  - Desabilitar a Recuperação de desastre e interrompe a replicação de alterações de namespaces primários para secundários
    - `Set-AzureRmServiceBusDRConfigurationsBreakPairing`
  - Invocar um failover de Recuperação de Desastres e reconfigurar o alias a fim de apontar para o namespace secundário
    - `Set-AzureRmServiceBusDRConfigurationsFailOver`
  - Excluir um Alias (configuração de Recuperação de Desastre)
    - `Remove-AzureRmServiceBusDRConfigurations`
* Os commandlets `Test-AzureRmServiceBusName` foram atualizados para dar suporte à recuperação de desastre de replicação geográfica - Operações de disponibilidade de verificação do nome do alias.
  - Verifique a disponibilidade do nome do Namespace ou do Alias (configuração de Recuperação de Desastre):
    - `Test-AzureRmServiceBusName`

### <a name="azurermusageaggregates"></a>AzureRM.UsageAggregates
* Uso de `Login-AzureRmAccount` corrigido para usar `Connect-AzureRmAccount`

## <a name="520---january-2018"></a>5.2.0 – Janeiro de 2018
#### <a name="azurermprofile"></a>AzureRM.profile
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Add-AzureRmAccount
  * Adicionado o Logon -MSI para autenticação usando as credenciais da Identidade do serviço gerenciado da VM/serviço atual
  * Autenticação de KeyVault corrigida ao fazer logon com tokens de acesso fornecidos pelo usuário

#### <a name="azurestorage"></a>Azure.Storage
* Adicionar os cmdlets para obter e definir propriedades do serviço de armazenamento
    - Get-AzureStorageServiceProperty
    - Update-AzureStorageServiceProperty

#### <a name="azurermanalysisservices"></a>AzureRM.AnalysisServices
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmApiManagementProperty, Set-AzureRmApiManagementProperty e New-AzureRmApiManagement

#### <a name="azurermapplicationinsights"></a>AzureRM.ApplicationInsights
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermautomation"></a>AzureRM.Automation
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para Set-AzureRmAutomationRunbook

#### <a name="azurermbackup"></a>AzureRM.Backup
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermbatch"></a>AzureRM.Batch
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermcdn"></a>AzureRM.Cdn
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmCdnEndpoint e New-AzureRmCdnProfile

#### <a name="azurermcognitiveservices"></a>AzureRM.CognitiveServices
* Integrar ao SDK de Gerenciamento dos Serviços Cognitivos versão 3.0.0.

#### <a name="azurermcompute"></a>AzureRM.Compute
* Um conjunto de parâmetros simplificado foi adicionado a New-AzureRmVmss, que cria um Conjunto de dimensionamento de máquinas virtuais e todos os recursos necessários usando padrões inteligentes
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmVm e Update-AzureRmVm
* Corrigido o cmdlet Get-AzureRmComputeResourceSku fixo quando a Zona está incluída na restrição.
* Atualizado o esquema de configuração do agente de diagnóstico para suporte do coletor do Azure Monitor.

#### <a name="azurermcontainerinstance"></a>AzureRM.ContainerInstance
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermcontainerregistry"></a>AzureRM.ContainerRegistry
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Habilitado o suporte do Azure Key Vault para todos os serviços vinculados de armazenamento de dados
* Adicionada propriedade de tipo de licença para tempo de execução de integração do Azure SSIS
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmDataFactory

#### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Habilitado o suporte do Azure Key Vault para todos os serviços vinculados de armazenamento de dados
* Adicionada propriedade de tipo de licença para tempo de execução de integração do Azure SSIS
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Adicionar parâmetro "LicenseType" para cmd "Set-AzureRmDataFactoryV2IntegrationRuntime" para habilitar a funcionalidade AHUB

#### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmDataLakeAnalyticsAccount e Set-AzureRmDataLakeAnalyticsAccount

#### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmDataLakeStoreAccount e Set-AzureRmDataLakeStoreAccount

#### <a name="azurermdevtestlabs"></a>AzureRM.DevTestLabs
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermdns"></a>AzureRM.Dns
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermeventgrid"></a>AzureRM.EventGrid
* Adicionado o novo cmdlet a seguir:
  - Update-AzureRmEventGridSubscription
    - Atualize as propriedades de uma assinatura de evento de Grade de Eventos.
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermeventhub"></a>AzureRM.EventHub
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermhdinsight"></a>AzureRM.HDInsight
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurerminsights"></a>AzureRM.Insights
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermiothub"></a>AzureRM.IotHub
* Adicionar suporte a Certificado para cmdlets IoTHub
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Adicionado suporte a -AsJob para cmdlets de longa execução de KeyVault. Permite que os cmdlets selecionados sejam executados em segundo plano e devolvam um trabalho para rastreamento e controle de progresso.
  * O cmdlet afetado é: Remove-AzureRmKeyVault
* Correção do bug em Set-AzureRmKeyVaultAccessPolicy em que o filtro AAD estava definindo o SPN para o UPN fornecido, em vez de definir o UPN
  - Consulte o problema a seguir para obter mais informações: https://github.com/Azure/azure-powershell/issues/5201

#### <a name="azurermlogicapp"></a>AzureRM.LogicApp
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para Update-AzureRmMlCommitmentPlan

#### <a name="azurermmachinelearningcompute"></a>AzureRM.MachineLearningCompute
* Adicionar parâmetro IncludeAllResources ao cmdlet Remove-AzureRmMlOpCluster
  - O uso desse parâmetro de opção removerá todos os recursos que foram criados originalmente com o cluster
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermmedia"></a>AzureRM.Media
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para Set-AzureRmMediaService e New-AzureRmMediaService

#### <a name="azurermnetwork"></a>AzureRM.Network
* Adicionado suporte para -AsJob para cmdlets de Rede de longa execução. Permite que os cmdlets selecionados sejam executados em segundo plano e devolvam um trabalho para rastreamento e controle de progresso.
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmNotificationHubsNamespace e Set-AzureRmNotificationHubsNamespace

#### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmOperationalInsightsSavedSearch, Set-AzureRmOperationalInsightsSavedSearch, New-AzureRmOperationalInsightsWorkspacee Set-AzureRmOperationalInsightsWorkspace

#### <a name="azurermpowerbiembedded"></a>AzureRM.PowerBIEmbedded
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermrecoveryservices"></a>AzureRM.RecoveryServices
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermrecoveryservicesbackup"></a>AzureRM.RecoveryServices.Backup
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Adicionada a opção -UseOriginalStorageAccount para o cmdlet Restore-AzureRmRecoveryServicesBackupItem.
  - Habilitando esses resultados de sinalizador em discos de restauração para suas contas de armazenamento originais, o que permite aos usuários manter a configuração da VM restaurada o mais próximo possível das VMs originais.
  - Também ajuda a melhorar o desempenho da operação de restauração.

#### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Adicionados 3 novos cmdlets para regras de firewall
* Adicionados 3 novos cmdlets para replicação geográfica
* Adicionado suporte para zonas e marcas
* Deixe o ResourceGroup como opcional sempre que possível.

#### <a name="azurermrelay"></a>AzureRM.Relay
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermresources"></a>AzureRM.Resources
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Adicionado suporte para -AsJob para cmdlets de Recursos de longa execução. Permite que os cmdlets selecionados sejam executados em segundo plano e devolvam um trabalho para rastreamento e controle de progresso.
* Adicionado alias de Get-AzureRmProviderOperation para Get-AzureRmResourceProviderAction para manter a conformidade com as convenções de nomenclatura

#### <a name="azurermscheduler"></a>AzureRM.Scheduler
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermservermanagement"></a>AzureRM.ServerManagement
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Obsoleto -Tags a favor de -Tag para New-AzureRmServerManagementNode e New-AzureRmServerManagementGateway

#### <a name="azurermservicebus"></a>AzureRM.ServiceBus
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermsiterecovery"></a>AzureRM.SiteRecovery
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermsql"></a>AzureRM.Sql
* Atualizar a descrição de parâmetros de comandos de Auditoria
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Adicionado o parâmetro -AsJob para cmdlets de longa execução
* Obsoleto parâmetro -DatabaseName de Get-AzureRmSqlServiceObjective

#### <a name="azurermstorage"></a>AzureRM.Storage
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Corrigir um problema de referência nula de execução de cmdlet New-AzureRMStorageAccount com o parâmetro -EnableEncryptionService None
* Adicionado suporte para -AsJob para cmdlets de Armazenamento de longa execução. Permite que os cmdlets selecionados sejam executados em segundo plano e devolvam um trabalho para rastreamento e controle de progresso.
    - Os cmdlets afetados são New-, Remove-, Add- e Update- para a Conta de Armazenamento e a Regra de Conta de Armazenamento em Rede.

#### <a name="azurermstreamanalytics"></a>AzureRM.StreamAnalytics
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermtrafficmanager"></a>AzureRM.TrafficManager
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual

#### <a name="azurermwebsites"></a>AzureRM.Websites
* Adicionado o Completador de local parâmetros de -Location, permitindo o preenchimento da guia por meio de locais válidos
* Adicionado o ResourceGroup Completer aos parâmetros -ResourceGroup, permitindo o preenchimento da guia por meio de grupos de recursos na assinatura atual
* Adicionado suporte para -AsJob para cmdlets de Sites de longa execução. Permite que os cmdlets selecionados sejam executados em segundo plano e devolvam um trabalho para rastreamento e controle de progresso.
     - Os cmdlets afetados são New-, Remove-, Add- e Set- para WebApps, AppServicePlan e Slots

## <a name="2017128-version-511"></a>8/12/2017 Versão 5.1.1
* AnalysisServices
  - Alterar o conjunto validado de locais da pesquisa dinâmica para que todas as nuvens tenham suporte.
* Automação
  - Atualizar para Import-AzureRMAutomationRunbook
    - O suporte agora está sendo fornecido para runbooks Python2
* Lote
  - Correção de bug em que as operações de conta sem um grupo de recursos não conseguiam detectar o grupo de recursos automaticamente
* Computação
  - Get-AzureRmComputeResourceSku mostra informações de zona.
  - Atualização de Disable-AzureRmVmssDiskEncryption para corrigir o problema https://github.com/Azure/azure-powershell/issues/5038
  - Adicionado: suporte AsJob para cmdlets de computação de longa execução. Permite que os cmdlets selecionados sejam executados em segundo plano e devolvam um trabalho para rastreamento e controle de progresso.
    - Os cmdlets afetados incluem: New-, Update-, Set-, Remove-, Start-, Restart-, Stop- para Máquinas Virtuais e Conjuntos de Dimensionamento de Máquinas Virtuais
    - Um conjunto de parâmetros simplificado foi adicionado a New-AzureRmVM, que cria uma Máquina Virtual e todos os recursos necessários usando padrões inteligentes
* ContainerInstance
  - Aplicar o SDK de Instância de Contêiner do Azure 2017-10-01
    - Suporte à execução do contêiner até a conclusão
    - Suporte à montagem de volume do Arquivo do Azure
    - Suporte à abertura de várias portas para IP público
* ContainerRegistry
  - Novos cmdlets para replicação geográfica e webhooks
    - Get/New/Remove-AzureRmContainerRegistryReplication
    - Get/New/Remove/Test/Update-AzureRmContainerRegistryWebhook
* DataFactories
    - A funcionalidade de criptografia de credenciais agora funciona com "Acesso Remoto" habilitado (pela rede) e "Acesso Remoto" desabilitado (computador local).
* DataFactoryV2
  - Dois novos cmdlets foram adicionados: Update-AzureRmDataFactoryV2 e Stop-AzureRmDataFactoryV2PipelineRun
* DataLakeAnalytics
  - Um parâmetro chamado ScriptParameter foi adicionado a Submit-AzureRmDataLakeAnalyticsJob
    - As informações detalhadas sobre ScriptParameter podem ser encontradas usando Get-Help em Submit-AzureRmDataLakeAnalyticsJob
  - Em relação a New-AzureRmDataLakeAnalyticsAccount, o parâmetro MaxDegreeOfParallelism foi alterado para MaxAnalyticsUnits
    - Um alias foi adicionado ao parâmetro MaxAnalyticsUnits: MaxDegreeOfParallelism
  - Em relação a New-AzureRmDataLakeAnalyticsComputePolicy, o parâmetro MaxDegreeOfParallelismPerJob foi alterado para MaxAnalyticsUnitsPerJob
    - Um alias foi adicionado ao parâmetro MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob
  - Em relação a Set-AzureRmDataLakeAnalyticsAccount, o parâmetro MaxDegreeOfParallelism foi alterado para MaxAnalyticsUnits
    - Um alias foi adicionado ao parâmetro MaxAnalyticsUnits: MaxDegreeOfParallelism
  - Em relação a Submit-AzureRmDataLakeAnalyticsJob, o parâmetro DegreeOfParallelism foi alterado para AnalyticsUnits
    - Um alias foi adicionado ao parâmetro AnalyticsUnits: DegreeOfParallelism
  - Em relação a Update-AzureRmDataLakeAnalyticsComputePolicy, o parâmetro MaxDegreeOfParallelismPerJob foi alterado para MaxAnalyticsUnitsPerJob
    - Um alias foi adicionado ao parâmetro MaxAnalyticsUnitsPerJob: MaxDegreeOfParallelismPerJob
* MachineLearningCompute
  - Adicionar Set-AzureRmMlOpCluster
    - Atualizar a contagem de um agente ou a configuração de SSL de um cluster
  - As propriedades do Orchestrator são opcionais
    - O serviço irá criar uma entidade de serviço se este não for fornecido e, portanto, as propriedades do orquestrador agora são opcionais
* PowerBIEmbedded
  - Adicionar suporte aos cmdlets da Capacidade do Power BI Embedded
  - Novo Cmdlet Get-AzureRmPowerBIEmbeddedCapacity - Obtém os detalhes de uma Capacidade do Power BI Embedded.
  - Novo Cmdlet New-AzureRmPowerBIEmbeddedCapacity - Cria uma nova Capacidade do Power BI Embedded
  - Novo Cmdlet Remove-AzureRmPowerBIEmbeddedCapacity - Exclui uma instância da Capacidade do Power BI Embedded
  - Novo Cmdlet Resume-AzureRmPowerBIEmbeddedCapacity - Retoma uma instância da Capacidade do Power BI Embedded
  - Novo Cmdlet Suspend-AzureRmPowerBIEmbeddedCapacity - Suspende uma instância da Capacidade do Power BI Embedded
  - Novo Cmdlet Test-AzureRmPowerBIEmbeddedCapacity - Testa a existência de uma instância da Capacidade do Power BI Embedded
  - Novo Cmdlet Update-AzureRmPowerBIEmbeddedCapacity - Modifica uma instância da Capacidade do Power BI Embedded
* Perfil
  - Atualização de USGovernmentActiveDirectoryEndpoint para https://login.microsoftonline.us/
    - Para obter mais informações sobre os mapeamentos de ponto de extremidade do Azure Governamental, consulte: https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide#endpoint-mapping
    - O suporte -AsJob foi adicionado para cmdlets, permitindo que cmdlets selecionados sejam executados em segundo plano e devolvam um trabalho para rastreamento e controle de progresso
    - O parâmetro -AsJob foi adicionado ao cmdlet Get-AzureRmSubscription
* RecoveryServices.Backup
  - Correção do bug – Get-AzureRmRecoveryServicesBackupItem deve fazer uma comparação no filtro de nome de contêiner que não diferencia maiúsculas de minúsculas.
  - Correção do bug – AzureVmItem agora tem uma propriedade que mostra a última vez que uma operação de backup aconteceu: LastBackupTime.
* Recursos
  - Foi corrigido um problema em que o Get-AzureRMRoleAssignment resultava em atribuições sem nome de roledefiniton para funções personalizadas
    - Os usuários agora podem usar Get-AzureRMRoleAssignment com atribuições com nomes de roledefinition independentemente do tipo de função
  - Correção do problema em que o Set-AzureRMRoleRoleDefinition costumava lançar erro de DF não encontrada quando havia um novo escopo em assignablescopes
    - Os usuários agora podem usar Set-AzureRMRoleRoleDefinition com escopos atribuíveis, incluindo novos escopos independentemente da posição do escopo
  - Permitir que os escopos terminem com "/"
    - Os usuários agora podem usar commandlets de RoleDefinition e RoleAssignment com escopos terminados em "/", consistentes com API e CLI
  - Permitir que usuários criem RoleAssignment usando o sinalizador de delegação
    - Os usuários agora podem usar New-AzureRMRoleAssignment com uma opção de adicionar o sinalizador de delegação
  - Corrigir o get do RoleAssignment para respeitar o parâmetro de escopo
  - Adicionar um alias a ServicePrincipalName no Commandlet New-AzureRmRoleAssignment
    - Os usuários agora podem usar ApplicationId em vez de ServicePrincipalName ao usar o commandlet New-AzureRmRoleAssignment
* SiteRecovery
  - Adicionar avisos de obsolescência para todos os cmdlets neste módulo em preparação para a próxima versão de alteração.
    - Confira o guia de alterações futuras para saber mais sobre como migrar seus cmdlets do AzureRM.
* Sql
  - Adicionada a capacidade de renomeação de banco de dados usando Set-AzureRmSqlDatabase
  - Problema corrigido https://github.com/Azure/azure-powershell/issues/4974
    - O fornecimento de um valor AUDIT_CHANGED_GROUP inválido para cmdlets de auditoria não gera mais um erro e será removido em uma versão futura.
  - Problema corrigido https://github.com/Azure/azure-powershell/issues/5046
    - O parâmetro AuditAction em cmdlets de auditoria não é mais ignorado
  - Corrigido um problema em cmdlets de auditoria quando um StorageKeyType 'Secundário' é fornecido
    - Ao configurar a auditoria de blobs, a chave da conta de armazenamento primária era usada em vez da chave secundária ao fornecer o valor 'Secundário' para o parâmetro StorageKeyType.
  - Alterando o texto da mensagem de confirmação de Set-AzureRmSqlServerTransparentDataEncryptionProtector
* Azure (RDFE)
    - Removidos todos os cmdlets RemoteApp
* Azure.Storage
    - Atualizar para a Biblioteca de Clientes do Armazenamento do Azure 8.6.0 e a Biblioteca de Movimentação de Dados do Armazenamento do Azure 0.6.5

## <a name="20171110-version-501"></a>10/11/2017 Versão 5.0.1
* Problema de carregamento do assembly corrigido, que causou a falha de alguns cmdlets ao executar nos seguintes módulos:
  - AzureRM.ApiManagement
  - AzureRM.Backup
  - AzureRM.Batch
  - AzureRM.Compute
  - AzureRM.DataFactories
  - AzureRM.HDInsight
  - AzureRM.KeyVault
  - AzureRM.RecoveryServices
  - AzureRM.RecoveryServices.Backup
  - AzureRM.RecoveryServices.SiteRecovery
  - AzureRM.RedisCache
  - AzureRM.SiteRecovery
  - AzureRM.Sql
  - AzureRM.Storage
  - AzureRM.StreamAnalytics

## <a name="2017118---version-500"></a>08/11/2017 - Versão 5.0.0
* Observação: esta é uma versão de alteração significativa. Consulte o guia de migração (https://aka.ms/azps-migration-guide) para obter uma lista completa das alterações de falha introduzidas.
* Agora, todos os cmdlets no AzureRM oferecem suporte à ajuda online
  - Execute Get-Help com o parâmetro -Online para abrir a ajuda online em seu navegador de Internet padrão
* AnalysisServices
  * Comando Synchronize-AzureAsInstance corrigido para trabalhar com a nova API REST do AsAzure para a sincronização
* ApiManagement
  * Confira o guia de migração para ver as alterações significativas feitas no ApiManagement desta versão
  * Atualização do cmdlet Get-AzureRmApiManagementUser para corrigir o problema https://github.com/Azure/azure-powershell/issues/4510
  * Atualizado o cmdlet New-AzureRmApiManagementApi para criar a API com o Caminho vazio https://github.com/Azure/azure-powershell/issues/4069
* ApplicationInsights
  * Adicionar comandos para obter/criar/remover recurso do Application Insights
    - Get-AzureRmApplicationInsights
    - New-AzureRmApplicationInsights
    - Remove-AzureRmApplicationInsights
  * Adicionar comandos para obter/atualizar os preços/capacidade diária do recurso do Application Insights
    - Get-AzureRmApplicationInsights -IncludeDailyCap
    - Set-AzureRmApplicationInsightsPricingPlan
    - Set-AzureRmApplicationInsightsDailyCap
  * Adicionar comandos para obter/criar/atualizar/remover exportação contínua do recurso do Application Insights
    - Get-AzureRmApplicationInsightsContinuousExport
    - Set-AzureRmApplicationInsightsContinuousExport
    - New-AzureRmApplicationInsightsContinuousExport
    - Remove-AzureRmApplicationInsightsContinuousExport
  * Adicionar comandos para obter/criar/remover chaves de API do recurso do application insights
    - Get-AzureRmApplicationInsightsApiKey
    - New-AzureRmApplicationInsightsApiKey
    - Remove-AzureRmApplicationInsightsApiKey
* AzureBatch
  * Novos parâmetros adicionados a `New-AzureRmBatchAccount`.
    - `PoolAllocationMode`: o modo de alocação a ser usado para criar pools na conta do Lote. Para criar uma conta do Lote que aloca nós do pool na assinatura do usuário, defina isso para `UserSubscription`.
    - `KeyVaultId`: a ID de recurso do cofre de chaves do Azure associada à conta do Lote.
    - `KeyVaultUrl`: a URL do cofre de chaves do Azure associada à conta do Lote.
  * Parâmetros atualizados para `New-AzureBatchTask`.
    - Opção `RunElevated` removida. O parâmetro `UserIdentity` foi adicionado para substituir `RunElevated` e o comportamento equivalente pode ser obtido construindo `PSUserIdentity` conforme mostrado abaixo:
      - $autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
      - $userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
    - Parâmetro `AuthenticationTokenSettings` adicionado. Esse parâmetro permite solicitar que o serviço de Lote forneça um token de autenticação para a tarefa na execução, evitando a necessidade de passar as chaves de conta do Lote para a tarefa para fazer solicitações ao serviço de Lote.
    - Parâmetro `ContainerSettings` adicionado.
      - Esse parâmetro permite solicitar que o serviço de Lote execute a tarefa dentro de um contêiner.
    - Parâmetro `OutputFiles` adicionado.
      - Esse parâmetro permite que você configure a tarefa para carregar arquivos no Armazenamento do Azure após sua conclusão.
  * Parâmetros atualizados para `New-AzureBatchPool`.
    - Parâmetro `UserAccounts` adicionado.
      - Esse parâmetro define as contas de usuário criadas em cada nó no pool.
    - `TargetLowPriorityComputeNodes` adicionado e `TargetDedicated` renomeado como `TargetDedicatedComputeNodes`.
      - Um alias `TargetDedicated` foi criado para o parâmetro `TargetDedicatedComputeNodes`.
    - Parâmetro `NetworkConfiguration` adicionado.
      - Esse parâmetro permite que você defina as configurações de rede de pools.
  * Parâmetros atualizados para `New-AzureBatchCertificate`.
    - Agora, o parâmetro `Password` é `SecureString`.
  * Parâmetros atualizados para `New-AzureBatchComputeNodeUser`.
    - Agora, o parâmetro `Password` é `SecureString`.
  * Parâmetros atualizados para `Set-AzureBatchComputeNodeUser`.
    - Agora, o parâmetro `Password` é `SecureString`.
  * Parâmetro `Name` renomeado como `Path` em `Get-AzureBatchNodeFile`, `Get-AzureBatchNodeFileContent` e `Remove-AzureBatchNodeFile`.
    - Um alias `Name` foi criado para o parâmetro `Path`.
  * Alterações nos objetos
    - Confira o log de alterações do Lote para obter a lista completa
  * Suporte adicionado para a autenticação baseada no Azure Active Directory.
    - Para usar a autenticação do Azure Active Directory, recupere um objeto `BatchAccountContext` usando o cmdlet `Get-AzureRmBatchAccount` e forneça `BatchAccountContext` ao parâmetro `-BatchContext` de um cmdlet do serviço de Lote. A autenticação do Azure Active Directory é obrigatória para as contas com `PoolAllocationMode = UserSubscription`.
    - Para as contas existentes ou novas contas criadas com `PoolAllocationMode = BatchService`, você pode continuar usando a autenticação da chave compartilhada recuperando um objeto `BatchAccountContext` com o cmdlet `Get-AzureRmBatchAccoutKeys`.
* Computação
  * Comandos de Extensão da Criptografia de Disco do Azure
    - O novo parâmetro para 'Set-AzureRmVmDiskEncryptionExtension': '-EncryptFormatAll' criptografa e formata os discos de dados
    - Os novos parâmetros para 'Set-AzureRmVmDiskEncryptionExtension': '-ExtensionPublisherName' e '-ExtensionType' permitem trocar para outras versões da extensão
    - Os novos parâmetros para 'Disable-AzureRmVmDiskEncryption': '-ExtensionPublisherName' e '-ExtensionType' permitem trocar para outras versões da extensão
    - Os novos parâmetros para 'Get-AzureRmVmDiskEncryptionStatus': '-ExtensionPublisherName' e '-ExtensionType' permitem trocar para outras versões da extensão
* DataLakeAnalytics
  * Confira o guia de migração para ver as alterações significativas feitas no DataLakeAnalytics desta versão
  * Um dos dois OutputTypes de Get-AzureRmDataLakeAnalyticsAccount foi alterado
    - Liste\<DataLakeAnalyticsAccount> para listar\<PSDataLakeAnalyticsAccountBasic>
    - As propriedades de PSDataLakeAnalyticsAccountBasic são um subconjunto exato das propriedades de DataLakeAnalyticsAccount
    - As propriedades adicionais que estão em DataLakeAnalyticsAccount não são retornadas pelo serviço.  Portanto, essa alteração é para refletir isso com precisão. Essas propriedades adicionais ainda estão em PSDataLakeAnalyticsAccountBasic, mas são marcadas como Obsoleto.
  * Um dos dois OutputTypes de Get-AzureRmDataLakeAnalyticsJob foi alterado
    - Liste \<JobInformation> para listar \<PSJobInformationBasic>
    - As propriedades de PSJobInformationBasic são um subconjunto exato das propriedades de JobInformation
    - As propriedades adicionais que estão em JobInformation não são retornadas pelo serviço.  Portanto, essa alteração é para refletir isso com precisão. Essas propriedades adicionais ainda estão em PSJobInformationBasic, mas são marcadas como Obsoleto.
* DataLakeStore
  * Confira o guia de migração para ver as alterações significativas feitas no DataLakeStore desta versão
  * Um dos dois OutputTypes de Get-AzureRmDataLakeStoreAccount foi alterado
    - Liste\<PSDataLakeStoreAccount> para listar\<PSDataLakeStoreAccountBasic>
    - As propriedades de PSDataLakeStoreAccountBasic são um subconjunto exato das propriedades de PSDataLakeStoreAccount
    - As propriedades adicionais que estão em PSDataLakeStoreAccount não são retornadas pelo serviço.  Portanto, essa alteração é para refletir isso com precisão. Essas propriedades adicionais ainda estão em PSDataLakeStoreAccountBasic, mas são marcadas como Obsoleto.
* DNS
  * Suporte para os tipos de registro CAA no DNS do Azure
    - Oferece suporte a todas as operações do tipo de registro CAA
* EventHub
  * Confira o guia de migração para ver as alterações significativas feitas no EventHub desta versão
* Insights
  * Confira o guia de migração para ver as alterações significativas feitas no Insights desta versão
* Rede
  * Confira o guia de migração para ver as alterações significativas feitas no Network desta versão
  * Cmdlet adicionado à lista de provedores de serviço da Internet disponíveis para uma região específica do Azure
    - Get-AzureRmNetworkWatcherReachabilityProvidersList
  * Cmdlet adicionado para obter a pontuação de latência relativa dos provedores de serviço da Internet a partir de um local especificado para as regiões do Azure
    - Get-AzureRmNetworkWatcherReachabilityReport
* Perfil
  - Set-AzureRmDefault
    - Use esse cmdlet para definir um grupo de recursos padrão.  Isso tornará o parâmetro -ResourceGroup opcional para alguns cmdlets e usará o padrão quando um grupo de recursos não for especificado
    - ```Set-AzureRmDefault -ResourceGroupName "ExampleResourceGroup"```
    - Se o grupo de recursos especificado existir na assinatura, esse grupo será definido para o padrão.  Do contrário, o grupo será criado e definido para o padrão.
  - Get-AzureRmDefault
    - Use esse cmdlet para obter o grupo de recursos padrão atual (e outros padrões no futuro).
    - ```Get-AzureRmDefault -ResourceGroup```
  - Clear-AzureRmDefault
    - Use esse cmdlet para remover o grupo de recursos padrão atual
    - ```Clear-AzureRmDefault -ResourceGroup```
  - Add-AzureRmEnvironment e Set-AzureRmEnvironment
    - Adicione o parâmetro BatchAudience, que permite especificar o público de Lote do Azure Active Directory a usar ao adquirir tokens de autenticação para o serviço de Lote.
* RecoveryServices.Backup
  * Cmdlets adicionados para executar a recuperação de arquivos instantânea.
    - Get-AzureRmRecoveryServicesBackupRPMountScript
    - Disable-AzureRmRecoveryServicesBackupRPMountScript
  * Versão do SDK RecoveryServices.Backup atualizada para a mais recente
  * Testes atualizados para a carga de trabalho da VM do Azure para que todas as configurações necessárias para as execuções de teste sejam feitas pelos próprios testes.
  * Corrige https://github.com/Azure/azure-powershell/issues/3164
* RecoveryServices.SiteRecovery
  * Alterações do VMware ASR para o Azure Site Recovery (os cmdlets atualmente oferecem suporte a operações entre Empresas, Empresa para Azure, HyperV para Azure)
    - New-AzureRmRecoveryServicesAsrPolicy
    - New-AzureRmRecoveryServicesAsrProtectedItem
    - Update-AzureRmRecoveryServicesAsrPolicy
    - Update-AzureRmRecoveryServicesAsrProtectionDirection
  * Suporte adicionado ao cofre baseado no AAD
  * Cmdlets adicionados para gerenciar os recursos do VCenter
    - Get-AzureRmRecoveryServicesAsrVCenter
    - New-AzureRmRecoveryServicesAsrVCenter
    - Remove-AzureRmRecoveryServicesAsrVCenter
    - Update-AzureRmRecoveryServicesAsrVCenter
  * Outros cmdlets adicionados
    - Get-AzureRmRecoveryServicesAsrAlertSetting
    - Get-AzureRmRecoveryServicesAsrEvent
    - New-AzureRmRecoveryServicesAsrProtectableItem
    - Set-AzureRmRecoveryServicesAsrAlertSetting
    - Start-AzureRmRecoveryServicesAsrResynchronizeReplicationJob
    - Start-AzureRmRecoveryServicesAsrSwitchProcessServerJob
    - Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob
    - Update-AzureRmRecoveryServicesAsrMobilityService
* ServiceBus
  - Confira o guia de migração para ver as alterações significativas feitas no ServiceBus desta versão
* Sql
  * Adicionar suporte para a lista e cancelar a operação assíncrona updateslo no banco de dados
    - Atualize o cmdlet Get-AzureRmSqlDatabaseActivity existente para retornar ao status da operação updateslo do BD.
    - Adicione um novo cmdlet Stop-AzureRmSqlDatabaseActivity para cancelar a operação assíncrona updateslo no banco de dados.
  * Adicionando suporte para a Redundância de Zona para os bancos de dados e pools elásticos
    - Adicionando o parâmetro da opção ZoneRedundant a New-AzureRmSqlDatabase
    - Adicionando o parâmetro da opção ZoneRedundant a Set-AzureRmSqlDatabase
    - Adicionando o parâmetro da opção ZoneRedundant a New-AzureRmSqlElasticPool
    - Adicionando o parâmetro da opção ZoneRedundant a Set-AzureRmSqlElasticPool
  * Adicionando suporte para os Aliases de DNS do Servidor
    - Adicionando o cmdlet Get-AzureRmSqlServerDnsAlias que obtém os aliases de DNS do servidor por servidor e o nome de alias, ou uma lista de aliases de DNS do servidor para um Azure SQL Server.
    - Adicionando o cmdlet New-AzureRmSqlServerDnsAlias que cria o novo alias de DNS do servidor para um determinado Azure SQL Server
    - Adicionando o cmdlet Set-AzurermSqlServerDnsAlias que permite atualizar um Azure SQL Server para o qual o alias de DNS do servidor está apontando
    - Adicionando o cmdlet Remove-AzureRmSqlServerDnsAlias que remove um alias de DNS do servidor para um Azure SQL Server
* Azure.Storage
  * Atualizar para a Biblioteca de Clientes do Armazenamento do Azure 8.5.0 e a Biblioteca de Movimentação de Dados do Armazenamento do Azure 0.6.3
  * Adicionar Recurso de Suporte do Instantâneo de Compartilhamento de Arquivos
    - Adicionar parâmetro 'SnapshotTime' a Get-AzureStorageShare
    - Adicionar parâmetro 'IncludeAllSnapshot' a Remove-AzureStorageShare
