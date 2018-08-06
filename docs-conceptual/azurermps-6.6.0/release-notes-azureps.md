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
# <a name="release-notes"></a><span data-ttu-id="a0c4c-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="a0c4c-103">Release notes</span></span>

<span data-ttu-id="a0c4c-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="a0c4c-105">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="a0c4c-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a0c4c-106">Geral</span><span class="sxs-lookup"><span data-stu-id="a0c4c-106">General</span></span>
* <span data-ttu-id="a0c4c-107">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a0c4c-108">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="a0c4c-108">AzureRM.Profile</span></span>
* <span data-ttu-id="a0c4c-109">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span> <span data-ttu-id="a0c4c-110">O padrão é sempre true, recursos individuais e substituição do padrão.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-110">Default is always true, individual resources and overridet the default.</span></span>
* <span data-ttu-id="a0c4c-111">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="a0c4c-111">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a0c4c-112">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a0c4c-112">Azure.Storage</span></span>
* <span data-ttu-id="a0c4c-113">Suporte à obtenção do contexto de armazenamento de DefaulfProfile</span><span class="sxs-lookup"><span data-stu-id="a0c4c-113">Support get Storage Context from DefaulfProfile</span></span>
* <span data-ttu-id="a0c4c-114">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-114">Add Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a0c4c-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a0c4c-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a0c4c-116">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="a0c4c-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="a0c4c-117">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="a0c4c-117">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="a0c4c-118">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="a0c4c-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="a0c4c-119">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="a0c4c-119">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="a0c4c-120">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="a0c4c-120">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="a0c4c-121">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="a0c4c-121">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0c4c-122">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0c4c-122">AzureRM.Compute</span></span>
* <span data-ttu-id="a0c4c-123">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-123">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="a0c4c-124">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="a0c4c-124">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="a0c4c-125">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-125">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="a0c4c-126">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="a0c4c-126">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="a0c4c-127">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-127">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="a0c4c-128">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-128">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="a0c4c-129">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a0c4c-129">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="a0c4c-130">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-130">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="a0c4c-131">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="a0c4c-131">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="a0c4c-132">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-132">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a0c4c-133">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a0c4c-133">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a0c4c-134">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-134">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="a0c4c-135">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-135">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="a0c4c-136">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-136">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="a0c4c-137">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-137">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a0c4c-138">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a0c4c-138">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a0c4c-139">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="a0c4c-139">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a0c4c-140">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a0c4c-140">AzureRM.EventHub</span></span>
* <span data-ttu-id="a0c4c-141">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="a0c4c-141">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="a0c4c-142">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="a0c4c-142">AzureRM.Insights</span></span>
* <span data-ttu-id="a0c4c-143">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="a0c4c-143">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="a0c4c-144">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="a0c4c-144">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0c4c-145">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0c4c-145">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0c4c-146">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0c4c-146">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0c4c-147">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0c4c-147">AzureRM.Network</span></span>
* <span data-ttu-id="a0c4c-148">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-148">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0c4c-149">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0c4c-149">AzureRM.Resources</span></span>
* <span data-ttu-id="a0c4c-150">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-150">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="a0c4c-151">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-151">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0c4c-152">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0c4c-152">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0c4c-153">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="a0c4c-153">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="a0c4c-154">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="a0c4c-154">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="a0c4c-155">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0c4c-155">AzureRM.Sql</span></span>
* <span data-ttu-id="a0c4c-156">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-156">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="a0c4c-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0c4c-157">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="a0c4c-158">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-158">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="a0c4c-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="a0c4c-159">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="a0c4c-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="a0c4c-160">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="a0c4c-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="a0c4c-161">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="a0c4c-162">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0c4c-162">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="a0c4c-163">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="a0c4c-163">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="a0c4c-164">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="a0c4c-164">AzureRM.Storage</span></span>
* <span data-ttu-id="a0c4c-165">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="a0c4c-165">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="a0c4c-166">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="a0c4c-166">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="a0c4c-167">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0c4c-167">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a0c4c-168">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0c4c-168">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="a0c4c-169">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a0c4c-169">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="a0c4c-170">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="a0c4c-170">AzureRM.Tags</span></span>
* <span data-ttu-id="a0c4c-171">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="a0c4c-171">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="a0c4c-172">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="a0c4c-172">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0c4c-173">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="a0c4c-173">AzureRM.Profile</span></span>
* <span data-ttu-id="a0c4c-174">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-174">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a0c4c-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a0c4c-175">Azure.Storage</span></span>
* <span data-ttu-id="a0c4c-176">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="a0c4c-176">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="a0c4c-177">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a0c4c-177">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="a0c4c-178">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a0c4c-178">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a0c4c-179">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a0c4c-179">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a0c4c-180">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-180">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="a0c4c-181">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="a0c4c-181">AzureRM.Automation</span></span>
* <span data-ttu-id="a0c4c-182">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-182">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0c4c-183">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0c4c-183">AzureRM.Compute</span></span>
* <span data-ttu-id="a0c4c-184">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a0c4c-184">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="a0c4c-185">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-185">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a0c4c-186">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-186">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="a0c4c-187">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-187">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="a0c4c-188">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-188">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a0c4c-189">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a0c4c-189">AzureRM.EventHub</span></span>
* <span data-ttu-id="a0c4c-190">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="a0c4c-190">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0c4c-191">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0c4c-191">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0c4c-192">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0c4c-192">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="a0c4c-193">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a0c4c-193">AzureRM.LogicApp</span></span>
* <span data-ttu-id="a0c4c-194">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a0c4c-194">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0c4c-195">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0c4c-195">AzureRM.Network</span></span>
* <span data-ttu-id="a0c4c-196">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a0c4c-196">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="a0c4c-197">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="a0c4c-197">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="a0c4c-198">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="a0c4c-198">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="a0c4c-199">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="a0c4c-199">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="a0c4c-200">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="a0c4c-200">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="a0c4c-201">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="a0c4c-201">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="a0c4c-202">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="a0c4c-202">AzureRM.Relay</span></span>
* <span data-ttu-id="a0c4c-203">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="a0c4c-203">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0c4c-204">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0c4c-204">AzureRM.Resources</span></span>
* <span data-ttu-id="a0c4c-205">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-205">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="a0c4c-206">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-206">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="a0c4c-207">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a0c4c-207">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="a0c4c-208">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="a0c4c-208">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="a0c4c-209">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="a0c4c-209">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="a0c4c-210">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0c4c-210">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0c4c-211">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="a0c4c-211">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="a0c4c-212">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-212">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="a0c4c-213">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0c4c-213">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0c4c-214">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0c4c-214">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0c4c-215">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0c4c-215">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0c4c-216">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0c4c-216">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="a0c4c-217">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="a0c4c-217">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="a0c4c-218">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="a0c4c-218">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a0c4c-219">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a0c4c-219">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a0c4c-220">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-220">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0c4c-221">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0c4c-221">AzureRM.Sql</span></span>
* <span data-ttu-id="a0c4c-222">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="a0c4c-222">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="a0c4c-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c4c-223">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="a0c4c-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c4c-224">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0c4c-225">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0c4c-225">AzureRM.Websites</span></span>
* <span data-ttu-id="a0c4c-226">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-226">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="a0c4c-227">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="a0c4c-227">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="a0c4c-228">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="a0c4c-228">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="a0c4c-229">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="a0c4c-229">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a0c4c-230">Geral</span><span class="sxs-lookup"><span data-stu-id="a0c4c-230">General</span></span>
* <span data-ttu-id="a0c4c-231">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="a0c4c-231">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="a0c4c-232">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="a0c4c-232">AzureRM.Profile</span></span>
* <span data-ttu-id="a0c4c-233">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="a0c4c-233">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0c4c-234">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0c4c-234">AzureRM.Compute</span></span>
* <span data-ttu-id="a0c4c-235">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="a0c4c-235">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="a0c4c-236">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-236">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="a0c4c-237">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="a0c4c-237">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="a0c4c-238">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="a0c4c-238">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="a0c4c-239">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-239">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="a0c4c-240">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-240">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="a0c4c-241">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-241">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="a0c4c-242">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a0c4c-242">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="a0c4c-243">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-243">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="a0c4c-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0c4c-244">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a0c4c-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0c4c-245">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="a0c4c-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0c4c-246">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a0c4c-247">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a0c4c-247">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a0c4c-248">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="a0c4c-248">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="a0c4c-249">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="a0c4c-249">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a0c4c-250">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="a0c4c-250">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="a0c4c-251">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="a0c4c-251">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="a0c4c-252">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="a0c4c-252">AzureRM.EventHub</span></span>
* <span data-ttu-id="a0c4c-253">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a0c4c-253">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="a0c4c-254">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-254">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="a0c4c-255">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-255">Provided Default Parameter set.</span></span>
* <span data-ttu-id="a0c4c-256">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-256">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0c4c-257">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0c4c-257">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0c4c-258">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="a0c4c-258">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="a0c4c-259">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0c4c-259">AzureRM.Network</span></span>
* <span data-ttu-id="a0c4c-260">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="a0c4c-260">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="a0c4c-261">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="a0c4c-261">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="a0c4c-262">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-262">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a0c4c-263">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-263">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="a0c4c-264">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-264">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a0c4c-265">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-265">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a0c4c-266">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-266">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="a0c4c-267">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-267">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a0c4c-268">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a0c4c-269">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="a0c4c-269">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a0c4c-270">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a0c4c-270">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a0c4c-271">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-271">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="a0c4c-272">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-272">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="a0c4c-273">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-273">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0c4c-274">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0c4c-274">AzureRM.Resources</span></span>
* <span data-ttu-id="a0c4c-275">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-275">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="a0c4c-276">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a0c4c-276">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="a0c4c-277">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a0c4c-277">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="a0c4c-278">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0c4c-278">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="a0c4c-279">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a0c4c-279">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="a0c4c-280">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a0c4c-280">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a0c4c-281">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="a0c4c-281">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a0c4c-282">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="a0c4c-282">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="a0c4c-283">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="a0c4c-283">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="a0c4c-284">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="a0c4c-284">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="a0c4c-285">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="a0c4c-285">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="a0c4c-286">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="a0c4c-286">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="a0c4c-287">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="a0c4c-287">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="a0c4c-288">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a0c4c-288">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="a0c4c-289">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-289">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0c4c-290">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0c4c-290">AzureRM.Sql</span></span>
* <span data-ttu-id="a0c4c-291">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="a0c4c-291">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="a0c4c-292">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="a0c4c-292">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="a0c4c-293">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="a0c4c-293">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0c4c-294">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="a0c4c-294">AzureRM.Profile</span></span>
* <span data-ttu-id="a0c4c-295">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="a0c4c-295">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="a0c4c-296">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="a0c4c-296">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="a0c4c-297">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a0c4c-297">Azure.Storage</span></span>
* <span data-ttu-id="a0c4c-298">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-298">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0c4c-299">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0c4c-299">AzureRM.Compute</span></span>
* <span data-ttu-id="a0c4c-300">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="a0c4c-300">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="a0c4c-301">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="a0c4c-301">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="a0c4c-302">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a0c4c-302">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a0c4c-303">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a0c4c-303">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a0c4c-304">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="a0c4c-304">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="a0c4c-305">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="a0c4c-305">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="a0c4c-306">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0c4c-306">Start-AzureRmVM</span></span>
    - <span data-ttu-id="a0c4c-307">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0c4c-307">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="a0c4c-308">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0c4c-308">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="a0c4c-309">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0c4c-309">Set-AzureRmVM</span></span>
    - <span data-ttu-id="a0c4c-310">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a0c4c-310">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="a0c4c-311">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-311">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="a0c4c-312">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="a0c4c-312">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="a0c4c-313">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="a0c4c-313">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="a0c4c-314">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-314">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="a0c4c-315">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-315">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="a0c4c-316">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-316">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="a0c4c-317">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a0c4c-317">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="a0c4c-318">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a0c4c-318">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="a0c4c-319">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a0c4c-319">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="a0c4c-320">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="a0c4c-320">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="a0c4c-321">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a0c4c-321">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="a0c4c-322">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="a0c4c-322">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="a0c4c-323">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a0c4c-323">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="a0c4c-324">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a0c4c-324">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="a0c4c-325">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a0c4c-325">AzureRM.EventGrid</span></span>
* <span data-ttu-id="a0c4c-326">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-326">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="a0c4c-327">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0c4c-327">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0c4c-328">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="a0c4c-328">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="a0c4c-329">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a0c4c-329">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="a0c4c-330">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="a0c4c-330">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="a0c4c-331">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="a0c4c-331">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="a0c4c-332">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="a0c4c-332">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="a0c4c-333">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a0c4c-333">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a0c4c-334">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-334">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="a0c4c-335">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-335">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0c4c-336">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0c4c-336">AzureRM.Sql</span></span>
* <span data-ttu-id="a0c4c-337">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="a0c4c-337">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a0c4c-338">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a0c4c-338">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a0c4c-339">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="a0c4c-339">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0c4c-340">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0c4c-340">AzureRM.Websites</span></span>
* <span data-ttu-id="a0c4c-341">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a0c4c-341">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="a0c4c-342">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="a0c4c-342">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="a0c4c-343">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="a0c4c-343">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="a0c4c-344">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a0c4c-344">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="a0c4c-345">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0c4c-345">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="a0c4c-346">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="a0c4c-346">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0c4c-347">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="a0c4c-347">AzureRM.Profile</span></span>
* <span data-ttu-id="a0c4c-348">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="a0c4c-348">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="a0c4c-349">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="a0c4c-349">AzureRM.Compute</span></span>
* <span data-ttu-id="a0c4c-350">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="a0c4c-350">VMSS VM Update feature</span></span>
    - <span data-ttu-id="a0c4c-351">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="a0c4c-351">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="a0c4c-352">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-352">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="a0c4c-353">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a0c4c-353">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="a0c4c-354">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-354">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="a0c4c-355">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="a0c4c-355">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="a0c4c-356">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="a0c4c-356">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="a0c4c-357">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="a0c4c-357">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="a0c4c-358">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="a0c4c-358">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="a0c4c-359">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a0c4c-359">AzureRM.KeyVault</span></span>
* <span data-ttu-id="a0c4c-360">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="a0c4c-360">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="a0c4c-361">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0c4c-361">AzureRM.Network</span></span>
* <span data-ttu-id="a0c4c-362">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="a0c4c-362">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="a0c4c-363">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="a0c4c-363">AzureRM.Resources</span></span>
* <span data-ttu-id="a0c4c-364">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="a0c4c-364">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="a0c4c-365">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="a0c4c-365">AzureRM.Scheduler</span></span>
* <span data-ttu-id="a0c4c-366">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="a0c4c-366">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="a0c4c-367">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0c4c-367">AzureRM.Sql</span></span>
* <span data-ttu-id="a0c4c-368">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="a0c4c-368">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="a0c4c-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0c4c-369">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a0c4c-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a0c4c-370">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a0c4c-371">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a0c4c-371">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a0c4c-372">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a0c4c-372">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a0c4c-373">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0c4c-373">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="a0c4c-374">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="a0c4c-374">AzureRM.Websites</span></span>
* <span data-ttu-id="a0c4c-375">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-375">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="a0c4c-376">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="a0c4c-376">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="a0c4c-377">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="a0c4c-377">AzureRM.Profile</span></span>
* <span data-ttu-id="a0c4c-378">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="a0c4c-378">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="a0c4c-379">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a0c4c-379">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="a0c4c-380">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-380">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="a0c4c-381">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a0c4c-381">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="a0c4c-382">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="a0c4c-382">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="a0c4c-383">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a0c4c-383">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="a0c4c-384">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="a0c4c-384">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="a0c4c-385">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="a0c4c-385">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="a0c4c-386">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="a0c4c-386">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="a0c4c-387">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="a0c4c-387">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="a0c4c-388">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="a0c4c-388">Added support for MSI identity</span></span>
* <span data-ttu-id="a0c4c-389">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="a0c4c-389">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="a0c4c-390">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a0c4c-390">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="a0c4c-391">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c4c-391">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="a0c4c-392">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a0c4c-392">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="a0c4c-393">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="a0c4c-393">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="a0c4c-394">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="a0c4c-394">AzureRM.Batch</span></span>
* <span data-ttu-id="a0c4c-395">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="a0c4c-395">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="a0c4c-396">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="a0c4c-396">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="a0c4c-397">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="a0c4c-397">AzureRM.Consumption</span></span>
* <span data-ttu-id="a0c4c-398">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="a0c4c-398">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="a0c4c-399">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a0c4c-399">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="a0c4c-400">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="a0c4c-400">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="a0c4c-401">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0c4c-401">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="a0c4c-402">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a0c4c-402">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="a0c4c-403">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="a0c4c-403">AzureRM.Network</span></span>
* <span data-ttu-id="a0c4c-404">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="a0c4c-404">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="a0c4c-405">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="a0c4c-405">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="a0c4c-406">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c4c-406">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="a0c4c-407">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-407">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="a0c4c-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a0c4c-408">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a0c4c-409">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-409">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="a0c4c-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a0c4c-410">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="a0c4c-411">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="a0c4c-411">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="a0c4c-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="a0c4c-412">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="a0c4c-413">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a0c4c-413">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="a0c4c-414">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="a0c4c-414">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="a0c4c-415">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="a0c4c-415">AzureRM.Sql</span></span>
* <span data-ttu-id="a0c4c-416">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="a0c4c-416">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="a0c4c-417">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-417">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="a0c4c-418">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-418">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="a0c4c-419">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-419">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="a0c4c-420">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="a0c4c-420">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="a0c4c-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0c4c-421">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="a0c4c-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a0c4c-422">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="a0c4c-423">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a0c4c-423">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="a0c4c-424">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a0c4c-424">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="a0c4c-425">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0c4c-425">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="a0c4c-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a0c4c-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="a0c4c-427">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="a0c4c-427">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>