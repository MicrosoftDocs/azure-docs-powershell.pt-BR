---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: f90c77d8c9cd78315264fb0a0a58e047aefc5041
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821863"
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

---
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