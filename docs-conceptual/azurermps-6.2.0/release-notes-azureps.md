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
ms.openlocfilehash: 5bc3c9079cb4019bdb2255ab1f947e8ad35ae4cc
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853450"
---
# <a name="release-notes"></a><span data-ttu-id="d07ad-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="d07ad-103">Release notes</span></span>

<span data-ttu-id="d07ad-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d07ad-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="d07ad-105">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="d07ad-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d07ad-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="d07ad-106">AzureRM.Profile</span></span>
* <span data-ttu-id="d07ad-107">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="d07ad-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="d07ad-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="d07ad-108">AzureRM.Compute</span></span>
* <span data-ttu-id="d07ad-109">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="d07ad-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="d07ad-110">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="d07ad-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="d07ad-111">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="d07ad-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="d07ad-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d07ad-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="d07ad-113">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="d07ad-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="d07ad-114">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="d07ad-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="d07ad-115">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="d07ad-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="d07ad-116">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="d07ad-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="d07ad-117">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="d07ad-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="d07ad-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d07ad-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="d07ad-119">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="d07ad-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="d07ad-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d07ad-120">AzureRM.Network</span></span>
* <span data-ttu-id="d07ad-121">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="d07ad-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="d07ad-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="d07ad-122">AzureRM.Resources</span></span>
* <span data-ttu-id="d07ad-123">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="d07ad-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="d07ad-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="d07ad-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="d07ad-125">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="d07ad-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="d07ad-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d07ad-126">AzureRM.Sql</span></span>
* <span data-ttu-id="d07ad-127">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="d07ad-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="d07ad-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d07ad-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d07ad-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d07ad-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d07ad-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d07ad-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d07ad-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d07ad-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d07ad-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d07ad-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="d07ad-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="d07ad-133">AzureRM.Websites</span></span>
* <span data-ttu-id="d07ad-134">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="d07ad-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="d07ad-135">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="d07ad-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="d07ad-136">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="d07ad-136">AzureRM.Profile</span></span>
* <span data-ttu-id="d07ad-137">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="d07ad-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="d07ad-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d07ad-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="d07ad-139">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="d07ad-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="d07ad-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d07ad-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="d07ad-141">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="d07ad-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="d07ad-142">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d07ad-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="d07ad-143">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="d07ad-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="d07ad-144">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="d07ad-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="d07ad-145">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="d07ad-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="d07ad-146">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="d07ad-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="d07ad-147">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="d07ad-147">Added support for MSI identity</span></span>
* <span data-ttu-id="d07ad-148">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="d07ad-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="d07ad-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="d07ad-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="d07ad-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07ad-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="d07ad-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="d07ad-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="d07ad-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="d07ad-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="d07ad-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="d07ad-153">AzureRM.Batch</span></span>
* <span data-ttu-id="d07ad-154">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="d07ad-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="d07ad-155">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="d07ad-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="d07ad-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="d07ad-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="d07ad-157">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="d07ad-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="d07ad-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d07ad-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="d07ad-159">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="d07ad-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="d07ad-160">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d07ad-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="d07ad-161">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d07ad-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="d07ad-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="d07ad-162">AzureRM.Network</span></span>
* <span data-ttu-id="d07ad-163">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="d07ad-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="d07ad-164">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="d07ad-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="d07ad-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d07ad-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="d07ad-166">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="d07ad-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="d07ad-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d07ad-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d07ad-168">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="d07ad-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="d07ad-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d07ad-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="d07ad-170">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="d07ad-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="d07ad-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d07ad-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="d07ad-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d07ad-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="d07ad-173">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="d07ad-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="d07ad-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="d07ad-174">AzureRM.Sql</span></span>
* <span data-ttu-id="d07ad-175">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="d07ad-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="d07ad-176">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="d07ad-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="d07ad-177">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="d07ad-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="d07ad-178">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="d07ad-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="d07ad-179">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="d07ad-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="d07ad-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d07ad-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="d07ad-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d07ad-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="d07ad-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="d07ad-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="d07ad-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d07ad-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="d07ad-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d07ad-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="d07ad-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d07ad-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="d07ad-186">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="d07ad-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>