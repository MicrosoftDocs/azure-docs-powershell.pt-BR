---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34461611"
---
# <a name="release-notes"></a>Notas de versão

É uma lista das alterações feitas nesta versão do Azure PowerShell.

---
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