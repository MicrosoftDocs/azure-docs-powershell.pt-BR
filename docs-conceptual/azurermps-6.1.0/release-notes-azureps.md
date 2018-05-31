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
# <a name="release-notes"></a><span data-ttu-id="4db7a-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="4db7a-103">Release notes</span></span>

<span data-ttu-id="4db7a-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4db7a-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="4db7a-105">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="4db7a-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="4db7a-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="4db7a-106">AzureRM.Profile</span></span>
* <span data-ttu-id="4db7a-107">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="4db7a-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="4db7a-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="4db7a-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="4db7a-109">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="4db7a-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="4db7a-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4db7a-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="4db7a-111">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="4db7a-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="4db7a-112">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4db7a-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="4db7a-113">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="4db7a-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="4db7a-114">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="4db7a-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="4db7a-115">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="4db7a-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="4db7a-116">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="4db7a-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="4db7a-117">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="4db7a-117">Added support for MSI identity</span></span>
* <span data-ttu-id="4db7a-118">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="4db7a-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="4db7a-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="4db7a-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="4db7a-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4db7a-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="4db7a-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="4db7a-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="4db7a-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="4db7a-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="4db7a-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="4db7a-123">AzureRM.Batch</span></span>
* <span data-ttu-id="4db7a-124">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="4db7a-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="4db7a-125">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="4db7a-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="4db7a-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="4db7a-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="4db7a-127">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="4db7a-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="4db7a-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="4db7a-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="4db7a-129">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="4db7a-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="4db7a-130">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4db7a-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="4db7a-131">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4db7a-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="4db7a-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="4db7a-132">AzureRM.Network</span></span>
* <span data-ttu-id="4db7a-133">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="4db7a-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="4db7a-134">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="4db7a-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="4db7a-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4db7a-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="4db7a-136">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="4db7a-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="4db7a-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4db7a-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="4db7a-138">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="4db7a-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="4db7a-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4db7a-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="4db7a-140">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="4db7a-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="4db7a-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="4db7a-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="4db7a-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="4db7a-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="4db7a-143">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="4db7a-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="4db7a-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="4db7a-144">AzureRM.Sql</span></span>
* <span data-ttu-id="4db7a-145">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="4db7a-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="4db7a-146">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="4db7a-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="4db7a-147">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="4db7a-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="4db7a-148">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="4db7a-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="4db7a-149">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="4db7a-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="4db7a-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4db7a-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="4db7a-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4db7a-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="4db7a-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="4db7a-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="4db7a-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4db7a-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="4db7a-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4db7a-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="4db7a-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="4db7a-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="4db7a-156">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="4db7a-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>