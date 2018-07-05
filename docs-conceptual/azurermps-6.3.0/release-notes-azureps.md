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
# <a name="release-notes"></a><span data-ttu-id="f0649-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="f0649-103">Release notes</span></span>

<span data-ttu-id="f0649-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f0649-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="f0649-105">6.3.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="f0649-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f0649-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="f0649-106">AzureRM.Profile</span></span>
* <span data-ttu-id="f0649-107">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="f0649-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="f0649-108">Criar um contexto para cada assinatura ao executar 'Connect-AzureRmAccount' sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="f0649-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="f0649-109">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f0649-109">Azure.Storage</span></span>
* <span data-ttu-id="f0649-110">Adição de outras informações sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="f0649-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f0649-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f0649-111">AzureRM.Compute</span></span>
* <span data-ttu-id="f0649-112">'Get-AzureRmVmDiskEncryptionStatus' corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="f0649-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="f0649-113">Atualizar a versão da biblioteca de clientes de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="f0649-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="f0649-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f0649-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f0649-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f0649-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f0649-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f0649-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="f0649-117">Correção dos cmdlets a seguir para mostrar corretamente o "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="f0649-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="f0649-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0649-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="f0649-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0649-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="f0649-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0649-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="f0649-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0649-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="f0649-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="f0649-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="f0649-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f0649-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="f0649-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="f0649-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="f0649-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="f0649-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="f0649-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f0649-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="f0649-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f0649-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="f0649-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f0649-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="f0649-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f0649-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="f0649-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f0649-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="f0649-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="f0649-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="f0649-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f0649-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="f0649-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f0649-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="f0649-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f0649-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="f0649-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f0649-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="f0649-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f0649-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="f0649-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="f0649-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="f0649-138">Remoção das condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription a fim de permitir a mudança desses parâmetros para uma cadeia vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="f0649-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="f0649-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f0649-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f0649-140">Correção do problema em que nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="f0649-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="f0649-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="f0649-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="f0649-142">Versão pública de cmdlets do Policy Insights</span><span class="sxs-lookup"><span data-stu-id="f0649-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="f0649-143">Usar a versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="f0649-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="f0649-144">Adição de PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="f0649-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="f0649-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f0649-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="f0649-146">Adição do parâmetro -Vault aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="f0649-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="f0649-147">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="f0649-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f0649-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f0649-148">AzureRM.Sql</span></span>
* <span data-ttu-id="f0649-149">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="f0649-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f0649-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f0649-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f0649-151">Atualização do arquivo de ajuda para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f0649-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f0649-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f0649-152">AzureRM.Websites</span></span>
* <span data-ttu-id="f0649-153">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f0649-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="f0649-154">"New-AzureRmWebAppSlot" foi atualizado para honrar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="f0649-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="f0649-155">6.2.1 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="f0649-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="f0649-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="f0649-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="f0649-157">Atualização do modelo PSWorkspace para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0649-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="f0649-158">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="f0649-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f0649-159">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="f0649-159">AzureRM.Profile</span></span>
* <span data-ttu-id="f0649-160">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="f0649-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="f0649-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="f0649-161">AzureRM.Compute</span></span>
* <span data-ttu-id="f0649-162">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="f0649-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="f0649-163">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="f0649-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="f0649-164">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="f0649-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="f0649-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f0649-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="f0649-166">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="f0649-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="f0649-167">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="f0649-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="f0649-168">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="f0649-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="f0649-169">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="f0649-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="f0649-170">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="f0649-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="f0649-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="f0649-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="f0649-172">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="f0649-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="f0649-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f0649-173">AzureRM.Network</span></span>
* <span data-ttu-id="f0649-174">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="f0649-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="f0649-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="f0649-175">AzureRM.Resources</span></span>
* <span data-ttu-id="f0649-176">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="f0649-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="f0649-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="f0649-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="f0649-178">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="f0649-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="f0649-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f0649-179">AzureRM.Sql</span></span>
* <span data-ttu-id="f0649-180">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="f0649-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="f0649-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f0649-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f0649-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f0649-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f0649-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f0649-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f0649-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f0649-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f0649-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f0649-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="f0649-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="f0649-186">AzureRM.Websites</span></span>
* <span data-ttu-id="f0649-187">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="f0649-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="f0649-188">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="f0649-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="f0649-189">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="f0649-189">AzureRM.Profile</span></span>
* <span data-ttu-id="f0649-190">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="f0649-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="f0649-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f0649-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="f0649-192">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="f0649-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="f0649-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f0649-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="f0649-194">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="f0649-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="f0649-195">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f0649-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="f0649-196">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="f0649-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="f0649-197">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="f0649-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="f0649-198">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="f0649-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="f0649-199">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="f0649-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="f0649-200">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="f0649-200">Added support for MSI identity</span></span>
* <span data-ttu-id="f0649-201">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="f0649-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="f0649-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f0649-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="f0649-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0649-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="f0649-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f0649-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="f0649-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f0649-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="f0649-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="f0649-206">AzureRM.Batch</span></span>
* <span data-ttu-id="f0649-207">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="f0649-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="f0649-208">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="f0649-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="f0649-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f0649-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="f0649-210">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="f0649-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="f0649-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="f0649-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="f0649-212">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f0649-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="f0649-213">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f0649-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="f0649-214">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="f0649-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="f0649-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="f0649-215">AzureRM.Network</span></span>
* <span data-ttu-id="f0649-216">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="f0649-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="f0649-217">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="f0649-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="f0649-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0649-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="f0649-219">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="f0649-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="f0649-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0649-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f0649-221">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="f0649-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="f0649-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0649-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="f0649-223">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="f0649-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="f0649-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f0649-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="f0649-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f0649-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="f0649-226">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="f0649-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="f0649-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="f0649-227">AzureRM.Sql</span></span>
* <span data-ttu-id="f0649-228">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="f0649-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="f0649-229">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="f0649-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="f0649-230">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="f0649-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="f0649-231">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="f0649-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="f0649-232">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="f0649-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="f0649-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f0649-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="f0649-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f0649-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="f0649-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="f0649-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="f0649-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f0649-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="f0649-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f0649-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="f0649-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f0649-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="f0649-239">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="f0649-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>