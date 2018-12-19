---
title: Log de Alterações do Azure PowerShell | Microsoft Docs
description: É um histórico das alterações feitas na versão mais recente do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/13/2018
ms.locfileid: "53218214"
---
# <a name="release-notes"></a><span data-ttu-id="33511-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="33511-103">Release notes</span></span>

<span data-ttu-id="33511-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33511-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="33511-105">6.13.0 - novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-106">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-107">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="33511-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="33511-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33511-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="33511-109">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="33511-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="33511-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="33511-110">AzureRM.Automation</span></span>
* <span data-ttu-id="33511-111">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="33511-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="33511-112">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="33511-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="33511-113">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="33511-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="33511-114">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="33511-115">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="33511-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-116">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-117">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="33511-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="33511-118">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="33511-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="33511-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="33511-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="33511-120">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="33511-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="33511-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="33511-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="33511-122">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="33511-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-123">AzureRM.Network</span></span>
* <span data-ttu-id="33511-124">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="33511-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="33511-125">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="33511-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="33511-126">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="33511-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="33511-127">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="33511-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="33511-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="33511-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="33511-129">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="33511-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="33511-130">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="33511-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="33511-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="33511-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="33511-132">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="33511-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="33511-133">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="33511-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="33511-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="33511-134">AzureRM.Relay</span></span>
* <span data-ttu-id="33511-135">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="33511-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-136">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-137">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="33511-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="33511-138">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="33511-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="33511-139">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="33511-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="33511-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="33511-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="33511-141">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="33511-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="33511-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-142">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-143">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="33511-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="33511-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="33511-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="33511-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="33511-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="33511-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="33511-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="33511-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="33511-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="33511-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="33511-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="33511-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="33511-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="33511-152">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="33511-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="33511-153">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="33511-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="33511-154">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="33511-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="33511-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="33511-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="33511-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="33511-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="33511-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="33511-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="33511-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="33511-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="33511-159">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="33511-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="33511-160">6.12.0 - novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-161">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-161">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-162">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="33511-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="33511-163">Renomear o parâmetro TenantId no cmdlet Connect-AzureRmAccount do locatário e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="33511-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="33511-164">Descrição de TenantId atualizada para Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="33511-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="33511-165">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="33511-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="33511-166">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="33511-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="33511-167">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="33511-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="33511-168">Corrigir o problema em que 'Disconnect-AzureRmAccount' seria lançado se não conectado</span><span class="sxs-lookup"><span data-stu-id="33511-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="33511-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="33511-169">AzureRM.Automation</span></span>
* <span data-ttu-id="33511-170">Nome do arquivo DLL de cmdlet renomeado para Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="33511-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="33511-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="33511-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="33511-172">Adicionar operação Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="33511-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-173">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-174">Adicionar cmdlets Add-AzureRmVmssVMDataDisk e Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="33511-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="33511-175">Get-AzureRmVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="33511-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="33511-176">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzureRmVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="33511-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="33511-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33511-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="33511-178">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="33511-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="33511-179">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="33511-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="33511-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="33511-180">AzureRM.Insights</span></span>
* <span data-ttu-id="33511-181">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="33511-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="33511-182">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="33511-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="33511-183">Correção do problema #7513 [Insights] Set-AzureRMDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="33511-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="33511-184">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="33511-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-185">AzureRM.Network</span></span>
* <span data-ttu-id="33511-186">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="33511-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="33511-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="33511-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="33511-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="33511-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="33511-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="33511-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="33511-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="33511-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="33511-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="33511-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="33511-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="33511-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="33511-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="33511-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="33511-194">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="33511-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="33511-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="33511-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="33511-196">Adicionado suporte para compartilhamentos de arquivos do Azure nos serviços de recuperação.</span><span class="sxs-lookup"><span data-stu-id="33511-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-197">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-198">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="33511-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="33511-199">Permitir a listagem de recursos usando o parâmetro '-ResourceId' para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="33511-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-201">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="33511-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="33511-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="33511-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="33511-203">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="33511-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="33511-204">Corrigir 'Add-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="33511-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="33511-205">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="33511-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="33511-206">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="33511-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="33511-207">Corrigir 'Update-AzureRmServiceFabricDurability' para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="33511-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="33511-208">6.11.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-209">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-209">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-210">Corrigir o problema com Get-AzureRmSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="33511-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="33511-211">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="33511-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="33511-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="33511-212">AzureRM.Backup</span></span>
* <span data-ttu-id="33511-213">Cmdlets do Backup do Azure preteridos.</span><span class="sxs-lookup"><span data-stu-id="33511-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-214">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-215">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para 'New-AzureRmVm'</span><span class="sxs-lookup"><span data-stu-id="33511-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="33511-216">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="33511-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="33511-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33511-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="33511-218">Adicionar suporte às Regras de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="33511-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="33511-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="33511-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="33511-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adiciona uma regra de rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="33511-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="33511-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifica a regra de rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="33511-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="33511-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Exclui uma regra de rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="33511-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-223">AzureRM.Network</span></span>
* <span data-ttu-id="33511-224">Atualize o cmdlet Test-AzureRmNetworkWatcherConnectivity, passe o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="33511-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="33511-225">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="33511-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-226">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-227">Corrija o problema onde Get-AzureRMRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="33511-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="33511-228">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="33511-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="33511-229">6.10.0 – outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="33511-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-230">Azure.Storage</span></span>
* <span data-ttu-id="33511-231">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="33511-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="33511-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="33511-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="33511-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="33511-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="33511-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="33511-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="33511-235">Suporte para Get-AzureRmCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="33511-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-236">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-237">Correção de Get-AzureRmVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="33511-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="33511-238">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="33511-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="33511-239">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="33511-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="33511-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="33511-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="33511-241">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="33511-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-242">AzureRM.Network</span></span>
* <span data-ttu-id="33511-243">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="33511-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="33511-244">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="33511-244">new cmdlets added</span></span>
    - <span data-ttu-id="33511-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33511-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="33511-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33511-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="33511-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33511-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="33511-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="33511-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="33511-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="33511-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="33511-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="33511-251">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="33511-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="33511-252">Adicionados os cmdlets New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="33511-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="33511-253">Adicionados os cmdlets Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="33511-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="33511-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="33511-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="33511-255">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="33511-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="33511-256">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="33511-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-257">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-258">Adição do parâmetro -Mode ausente a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="33511-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="33511-259">Correção do bug do cmdlet Get-AzureRmProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="33511-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="33511-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-260">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-261">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="33511-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="33511-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-262">AzureRM.Storage</span></span>
* <span data-ttu-id="33511-263">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="33511-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="33511-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="33511-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="33511-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="33511-265">AzureRM.Websites</span></span>
* <span data-ttu-id="33511-266">Novo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="33511-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="33511-267">Novos cmdlets New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="33511-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="33511-268">6.9.0 - setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="33511-269">Geral</span><span class="sxs-lookup"><span data-stu-id="33511-269">General</span></span>
* <span data-ttu-id="33511-270">O AzureRM.SignalR foi adicionado ao módulo de rollup do AzureRM</span><span class="sxs-lookup"><span data-stu-id="33511-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="33511-271">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-271">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-272">Pequenas alterações no código comum de armazenamento</span><span class="sxs-lookup"><span data-stu-id="33511-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="33511-273">Arquivos de ajuda atualizados para incluir tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="33511-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="33511-274">Alterado: ServicePrincipal como não obrigatório no conjunto de parâmetros ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33511-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="33511-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-275">Azure.Storage</span></span>
* <span data-ttu-id="33511-276">Suporte à criação do Contexto de Armazenamento com OAuth.</span><span class="sxs-lookup"><span data-stu-id="33511-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="33511-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="33511-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="33511-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="33511-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="33511-279">Standard_Microsoft adicionado à SKU de preços da CDN.</span><span class="sxs-lookup"><span data-stu-id="33511-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="33511-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-280">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-281">Mover dependências em Keyvault e Armazenamento para as dependências em comum</span><span class="sxs-lookup"><span data-stu-id="33511-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="33511-282">Adicionar suporte aos cmdlets do AEM para mais tamanhos de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="33511-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="33511-283">Adicionar o parâmetro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="33511-284">Adicionar parâmetro ResourceId ao cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="33511-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="33511-285">Adicionar cmdlet Invoke-AzureRmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="33511-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="33511-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="33511-286">AzureRM.Dns</span></span>
* <span data-ttu-id="33511-287">Suporte adicionado ao registro de alias durante criação de registros DNS</span><span class="sxs-lookup"><span data-stu-id="33511-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="33511-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="33511-288">AzureRM.Insights</span></span>
* <span data-ttu-id="33511-289">Problemas 6833 e 7102 corrigidos (área Configurações de Diagnóstico)</span><span class="sxs-lookup"><span data-stu-id="33511-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="33511-290">Problemas com o nome padrão, ou seja, “service”, durante a criação e a listagem/obtenção das configurações de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="33511-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="33511-291">Problemas na criação das configurações de diagnóstico com categorias</span><span class="sxs-lookup"><span data-stu-id="33511-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="33511-292">Mensagem de reprovação adicionada para parâmetros do intervalo de agregação de métrica</span><span class="sxs-lookup"><span data-stu-id="33511-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="33511-293">Os parâmetros do intervalo de agregação ainda são aceitos (é uma alteração contínua), mas eles são ignorados no back-end, já que só PT1M é válido</span><span class="sxs-lookup"><span data-stu-id="33511-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-294">AzureRM.Network</span></span>
* <span data-ttu-id="33511-295">Alterações nos cmdlets LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33511-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="33511-296">LoadBalancerInboundNatPoolConfig: parâmetros IdleTimeoutInMinutes, EnableFloatingIp e EnableTcpReset adicionados</span><span class="sxs-lookup"><span data-stu-id="33511-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="33511-297">LoadBalancerInboundNatRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="33511-298">LoadBalancerRuleConfig: parâmetro EnableTcpReset adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="33511-299">LoadBalancerProbeConfig: suporte adicionado para o valor "Https" do parâmetro Protocol</span><span class="sxs-lookup"><span data-stu-id="33511-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="33511-300">Adicionados novos comandos para o novo sub-recurso OutboundRule do LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="33511-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="33511-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33511-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="33511-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33511-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="33511-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33511-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="33511-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33511-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="33511-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="33511-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="33511-306">Nova propriedade HostedWorkloads adicionada para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="33511-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="33511-307">Adicionados novos cmdlets para o recurso: Firewall do Azure por meio do ARM</span><span class="sxs-lookup"><span data-stu-id="33511-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="33511-308">Get-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="33511-309">Set-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="33511-310">New-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="33511-311">Remove-AzureRmFirewall adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="33511-312">New-AzureRmFirewallApplicationRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="33511-313">New-AzureRmFirewallApplicationRule adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="33511-314">New-AzureRmFirewallNatRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="33511-315">New-AzureRmFirewallNatRule adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="33511-316">New-AzureRmFirewallNetworkRuleCollection adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="33511-317">New-AzureRmFirewallNetworkRule adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="33511-318">Suporte adicionado para o certificado de Raiz Confiável e a configuração de Dimensionamento automático no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="33511-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="33511-319">Novos Cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="33511-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="33511-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="33511-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="33511-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="33511-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="33511-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="33511-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="33511-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="33511-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="33511-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="33511-329">Cmdlets atualizados com o parâmetro opcional -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="33511-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="33511-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="33511-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="33511-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="33511-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="33511-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="33511-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="33511-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="33511-334">Cmdlets atualizados com o parâmetro opcional -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="33511-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="33511-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="33511-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="33511-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="33511-337">Adicionar cmdlet para o Ponto de Extremidade da interface Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="33511-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="33511-338">Suporte adicionado para vários prefixos de endereço em uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="33511-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="33511-339">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="33511-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="33511-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33511-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="33511-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33511-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="33511-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33511-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="33511-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="33511-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="33511-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="33511-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="33511-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="33511-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="33511-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="33511-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="33511-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="33511-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="33511-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="33511-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="33511-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="33511-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="33511-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="33511-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="33511-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="33511-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="33511-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="33511-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="33511-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="33511-359">Adicionando cmdlets para delegação da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="33511-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="33511-360">New-AzureRmDelegation: Cria uma nova delegação que pode ser adicionada a uma sub-rede</span><span class="sxs-lookup"><span data-stu-id="33511-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="33511-361">Remove-AzureRmDelegation: Usa uma sub-rede e remove o nome de delegação fornecido dessa sub-rede</span><span class="sxs-lookup"><span data-stu-id="33511-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="33511-362">Add-AzureRmDelegation: Usa uma sub-rede e adiciona o nome do serviço fornecido como uma delegação a essa sub-rede</span><span class="sxs-lookup"><span data-stu-id="33511-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="33511-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="33511-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="33511-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="33511-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="33511-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="33511-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="33511-366">Suporte ao disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="33511-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="33511-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="33511-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="33511-368">Dependência do Insights atualizada.</span><span class="sxs-lookup"><span data-stu-id="33511-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-369">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-370">Atualizar New-AzureRmResourceGroupDeployment com o novo parâmetro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="33511-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="33511-371">Adicionar suporte a OnErrorDeployment com o novo parâmetro</span><span class="sxs-lookup"><span data-stu-id="33511-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="33511-372">Suporte à identidade gerenciada nas atribuições de política.</span><span class="sxs-lookup"><span data-stu-id="33511-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="33511-373">Os parâmetros com valores padrão não são mais necessários ao atribuir uma política com “New-AzureRmPolicyAssignment”</span><span class="sxs-lookup"><span data-stu-id="33511-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="33511-374">Adicionar novo cmdlet Get-AzureRmPolicyAlias para recuperar os aliases de política</span><span class="sxs-lookup"><span data-stu-id="33511-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-376">Problema corrigido 7161</span><span class="sxs-lookup"><span data-stu-id="33511-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="33511-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="33511-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="33511-378">Atualizar nomes de SKU para Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="33511-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="33511-379">Adicionar campo de versão ao objeto PSSignalRResource e a cadeia de conexão ao objeto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="33511-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="33511-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-380">AzureRM.Storage</span></span>
* <span data-ttu-id="33511-381">Suporte à Política de Imutabilidade no AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="33511-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="33511-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="33511-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="33511-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="33511-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="33511-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="33511-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="33511-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="33511-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="33511-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="33511-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="33511-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="33511-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="33511-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="33511-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33511-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="33511-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33511-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="33511-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33511-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="33511-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="33511-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="33511-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="33511-393">AzureRM.Websites</span></span>
* <span data-ttu-id="33511-394">Adicionados dois novos cmdlets: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="33511-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="33511-395">O argumento New-AzureRmAppServicePlan-HyperV é adicionado para criar um plano do serviço de aplicativo com o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="33511-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="33511-396">New-AzureRmWebApp/New-AzureRmWebAppSlot/ Set-AzureRmWebApp/Set-AzureRmWebAppSlot: Novos parâmetros (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) adicionados para criar e gerenciar o aplicativo de contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="33511-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="33511-397">6.8.1 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="33511-398">Geral</span><span class="sxs-lookup"><span data-stu-id="33511-398">General</span></span>
* <span data-ttu-id="33511-399">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="33511-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="33511-400">Assemblies de tempo de execução comum atualizados</span><span class="sxs-lookup"><span data-stu-id="33511-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="33511-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33511-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="33511-402">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="33511-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="33511-403">Problema corrigido https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="33511-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="33511-404">Os cmdlets Importar-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos</span><span class="sxs-lookup"><span data-stu-id="33511-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="33511-405">Problema corrigido https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="33511-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="33511-406">O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="33511-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="33511-407">Corrigida pela atualização para o nuget 4.0.4-nuget de prévia</span><span class="sxs-lookup"><span data-stu-id="33511-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="33511-408">Problema corrigido https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="33511-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="33511-409">Corrigido o filtro Odata para pesquisar por nome no produto</span><span class="sxs-lookup"><span data-stu-id="33511-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="33511-410">Problema corrigido https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="33511-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="33511-411">Corrigido o filtro Odata para pesquisar por nome na API</span><span class="sxs-lookup"><span data-stu-id="33511-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="33511-412">Adicionado suporte para o agente de AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="33511-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="33511-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-413">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-414">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="33511-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="33511-415">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="33511-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="33511-416">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="33511-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="33511-417">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="33511-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-418">AzureRM.Network</span></span>
* <span data-ttu-id="33511-419">Alterada a representação de saída de cmdlet para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="33511-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="33511-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="33511-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="33511-421">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="33511-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="33511-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-422">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-423">Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="33511-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-425">Problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="33511-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="33511-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="33511-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="33511-427">Suporte adicionado para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="33511-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="33511-428">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="33511-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="33511-429">Suporte adicionado para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="33511-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="33511-430">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="33511-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="33511-431">Suporte adicionado para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="33511-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="33511-432">Suporte adicionado para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="33511-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="33511-433">Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="33511-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="33511-434">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="33511-435">Geral</span><span class="sxs-lookup"><span data-stu-id="33511-435">General</span></span>
* <span data-ttu-id="33511-436">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="33511-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="33511-437">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-437">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-438">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="33511-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-439">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-440">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="33511-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="33511-441">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="33511-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="33511-442">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="33511-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="33511-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="33511-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="33511-444">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="33511-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-445">AzureRM.Network</span></span>
* <span data-ttu-id="33511-446">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="33511-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="33511-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="33511-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="33511-448">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="33511-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-449">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-450">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="33511-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-452">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="33511-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="33511-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="33511-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="33511-454">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="33511-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="33511-455">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="33511-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="33511-456">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="33511-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="33511-457">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="33511-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="33511-458">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="33511-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="33511-459">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="33511-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="33511-460">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="33511-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="33511-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="33511-461">AzureRM.Websites</span></span>
* <span data-ttu-id="33511-462">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="33511-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="33511-463">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-464">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-464">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-465">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="33511-466">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="33511-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="33511-467">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="33511-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="33511-468">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="33511-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="33511-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-469">Azure.Storage</span></span>
* <span data-ttu-id="33511-470">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="33511-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="33511-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="33511-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="33511-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="33511-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="33511-473">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="33511-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="33511-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="33511-475">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="33511-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33511-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="33511-477">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="33511-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="33511-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="33511-479">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="33511-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="33511-480">AzureRM.Automation</span></span>
* <span data-ttu-id="33511-481">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="33511-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="33511-482">AzureRM.Backup</span></span>
* <span data-ttu-id="33511-483">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="33511-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="33511-484">AzureRM.Batch</span></span>
* <span data-ttu-id="33511-485">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="33511-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="33511-486">AzureRM.Billing</span></span>
* <span data-ttu-id="33511-487">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="33511-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="33511-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="33511-489">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="33511-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="33511-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="33511-491">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-492">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-493">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="33511-494">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="33511-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="33511-495">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="33511-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="33511-496">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="33511-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="33511-497">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="33511-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="33511-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="33511-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="33511-499">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="33511-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="33511-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="33511-501">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="33511-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="33511-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="33511-503">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="33511-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="33511-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="33511-505">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="33511-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="33511-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="33511-507">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="33511-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="33511-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="33511-509">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="33511-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33511-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="33511-511">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="33511-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="33511-512">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="33511-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="33511-513">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="33511-514">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33511-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="33511-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="33511-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="33511-516">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="33511-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="33511-517">AzureRM.Dns</span></span>
* <span data-ttu-id="33511-518">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="33511-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="33511-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="33511-520">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="33511-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="33511-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="33511-522">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="33511-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="33511-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="33511-524">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="33511-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="33511-525">AzureRM.Insights</span></span>
* <span data-ttu-id="33511-526">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="33511-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="33511-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="33511-528">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="33511-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="33511-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="33511-530">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="33511-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="33511-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="33511-532">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="33511-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="33511-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="33511-534">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="33511-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="33511-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="33511-536">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="33511-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="33511-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="33511-538">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="33511-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="33511-539">AzureRM.Media</span></span>
* <span data-ttu-id="33511-540">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-541">AzureRM.Network</span></span>
* <span data-ttu-id="33511-542">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33511-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="33511-543">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="33511-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="33511-544">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33511-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="33511-545">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="33511-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="33511-546">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="33511-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="33511-547">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="33511-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="33511-548">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="33511-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="33511-549">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="33511-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="33511-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="33511-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="33511-551">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="33511-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="33511-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="33511-553">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="33511-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="33511-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="33511-555">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="33511-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="33511-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="33511-557">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="33511-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="33511-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="33511-559">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="33511-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="33511-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="33511-561">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="33511-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="33511-562">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="33511-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="33511-563">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="33511-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="33511-564">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="33511-565">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="33511-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="33511-566">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="33511-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="33511-567">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="33511-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="33511-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="33511-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="33511-569">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="33511-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="33511-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="33511-571">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="33511-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="33511-572">AzureRM.Relay</span></span>
* <span data-ttu-id="33511-573">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-574">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-575">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="33511-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="33511-576">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="33511-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="33511-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="33511-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="33511-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="33511-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="33511-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="33511-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="33511-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="33511-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="33511-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="33511-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="33511-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="33511-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="33511-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="33511-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="33511-584">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="33511-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="33511-585">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="33511-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="33511-586">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="33511-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="33511-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="33511-588">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-590">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="33511-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="33511-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="33511-592">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="33511-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-593">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-594">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="33511-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-595">AzureRM.Storage</span></span>
* <span data-ttu-id="33511-596">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="33511-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="33511-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="33511-598">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="33511-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="33511-599">AzureRM.Tags</span></span>
* <span data-ttu-id="33511-600">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="33511-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="33511-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="33511-602">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="33511-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="33511-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="33511-604">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="33511-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="33511-605">AzureRM.Websites</span></span>
* <span data-ttu-id="33511-606">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="33511-607">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="33511-608">Geral</span><span class="sxs-lookup"><span data-stu-id="33511-608">General</span></span>
* <span data-ttu-id="33511-609">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="33511-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="33511-610">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-610">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-611">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="33511-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="33511-612">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="33511-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-613">Azure.Storage</span></span>
* <span data-ttu-id="33511-614">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33511-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="33511-615">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="33511-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="33511-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33511-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="33511-617">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="33511-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="33511-618">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="33511-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="33511-619">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="33511-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="33511-620">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="33511-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="33511-621">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="33511-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="33511-622">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="33511-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-623">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-624">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="33511-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="33511-625">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="33511-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="33511-626">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="33511-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="33511-627">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="33511-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="33511-628">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="33511-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="33511-629">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="33511-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="33511-630">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="33511-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="33511-631">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="33511-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="33511-632">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="33511-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="33511-633">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="33511-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="33511-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="33511-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="33511-635">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="33511-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="33511-636">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="33511-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="33511-637">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="33511-638">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="33511-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="33511-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33511-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="33511-640">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="33511-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="33511-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="33511-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="33511-642">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="33511-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="33511-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="33511-643">AzureRM.Insights</span></span>
* <span data-ttu-id="33511-644">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="33511-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="33511-645">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="33511-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="33511-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="33511-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="33511-647">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33511-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-648">AzureRM.Network</span></span>
* <span data-ttu-id="33511-649">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="33511-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-650">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-651">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="33511-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="33511-652">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="33511-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-654">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="33511-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="33511-655">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="33511-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="33511-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-656">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-657">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="33511-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="33511-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="33511-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="33511-659">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="33511-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="33511-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="33511-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="33511-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="33511-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="33511-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="33511-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="33511-663">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="33511-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="33511-664">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="33511-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="33511-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-665">AzureRM.Storage</span></span>
* <span data-ttu-id="33511-666">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="33511-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="33511-667">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="33511-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="33511-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33511-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="33511-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33511-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="33511-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33511-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="33511-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="33511-671">AzureRM.Tags</span></span>
* <span data-ttu-id="33511-672">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="33511-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="33511-673">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-674">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-674">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-675">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="33511-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="33511-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-676">Azure.Storage</span></span>
* <span data-ttu-id="33511-677">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="33511-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="33511-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="33511-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="33511-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="33511-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="33511-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="33511-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="33511-681">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="33511-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="33511-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="33511-682">AzureRM.Automation</span></span>
* <span data-ttu-id="33511-683">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="33511-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-684">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-685">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="33511-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="33511-686">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="33511-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="33511-687">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="33511-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="33511-688">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="33511-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="33511-689">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="33511-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="33511-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="33511-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="33511-691">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="33511-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="33511-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="33511-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="33511-693">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="33511-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="33511-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="33511-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="33511-695">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="33511-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-696">AzureRM.Network</span></span>
* <span data-ttu-id="33511-697">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="33511-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="33511-698">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="33511-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="33511-699">New-AzureRmApplicationGateway: Adicionados o sinalizador de EnableFIPS e suporte a zonas</span><span class="sxs-lookup"><span data-stu-id="33511-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="33511-700">New-AzureRmApplicationGatewaySku: Adicionadas novas SKUs Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="33511-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="33511-701">Set-AzureRmApplicationGatewaySku: Adicionadas novas SKUs Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="33511-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="33511-702">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="33511-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="33511-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="33511-703">AzureRM.Relay</span></span>
* <span data-ttu-id="33511-704">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="33511-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-705">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-706">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="33511-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="33511-707">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="33511-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="33511-708">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="33511-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="33511-709">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="33511-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="33511-710">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="33511-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-712">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="33511-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="33511-713">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="33511-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="33511-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="33511-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="33511-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="33511-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="33511-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="33511-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="33511-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="33511-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="33511-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="33511-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="33511-719">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="33511-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="33511-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="33511-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="33511-721">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="33511-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="33511-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-722">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-723">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="33511-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="33511-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="33511-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="33511-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="33511-726">AzureRM.Websites</span></span>
* <span data-ttu-id="33511-727">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="33511-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="33511-728">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="33511-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="33511-729">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="33511-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="33511-730">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="33511-731">Geral</span><span class="sxs-lookup"><span data-stu-id="33511-731">General</span></span>
* <span data-ttu-id="33511-732">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="33511-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="33511-733">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-733">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-734">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="33511-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-735">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-736">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="33511-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="33511-737">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="33511-738">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="33511-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="33511-739">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="33511-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="33511-740">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33511-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="33511-741">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="33511-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="33511-742">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33511-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="33511-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="33511-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="33511-744">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="33511-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="33511-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33511-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="33511-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33511-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="33511-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33511-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="33511-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33511-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="33511-749">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="33511-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="33511-750">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="33511-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="33511-751">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="33511-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="33511-752">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="33511-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="33511-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="33511-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="33511-754">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="33511-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="33511-755">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="33511-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="33511-756">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="33511-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="33511-757">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="33511-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="33511-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="33511-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="33511-759">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="33511-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-760">AzureRM.Network</span></span>
* <span data-ttu-id="33511-761">Expor novas Skus para VirtualNetworkGateways com Redundância de Zona</span><span class="sxs-lookup"><span data-stu-id="33511-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="33511-762">Adicionados novos comandos para o recurso: APIs de parceiro do ExpressRoute por meio do ARM</span><span class="sxs-lookup"><span data-stu-id="33511-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="33511-763">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="33511-764">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="33511-765">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="33511-766">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="33511-767">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="33511-768">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="33511-769">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="33511-770">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="33511-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="33511-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="33511-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="33511-772">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="33511-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="33511-773">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="33511-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="33511-774">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="33511-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-775">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-776">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="33511-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="33511-777">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="33511-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="33511-778">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="33511-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="33511-779">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="33511-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="33511-780">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="33511-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="33511-781">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="33511-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="33511-782">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="33511-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="33511-783">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="33511-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="33511-784">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="33511-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="33511-785">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="33511-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="33511-786">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="33511-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="33511-787">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="33511-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="33511-788">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="33511-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="33511-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="33511-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="33511-790">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="33511-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="33511-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-791">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-792">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="33511-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="33511-793">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="33511-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="33511-794">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-795">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-795">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-796">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="33511-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="33511-797">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="33511-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="33511-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="33511-798">Azure.Storage</span></span>
* <span data-ttu-id="33511-799">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="33511-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-800">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-801">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="33511-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="33511-802">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="33511-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="33511-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="33511-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="33511-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="33511-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="33511-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="33511-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="33511-806">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="33511-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="33511-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33511-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="33511-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33511-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="33511-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33511-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="33511-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33511-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="33511-811">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33511-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="33511-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33511-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="33511-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="33511-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="33511-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="33511-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="33511-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33511-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="33511-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33511-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="33511-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33511-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="33511-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="33511-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="33511-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="33511-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="33511-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="33511-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="33511-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="33511-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="33511-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="33511-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="33511-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="33511-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="33511-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="33511-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="33511-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="33511-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="33511-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="33511-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="33511-827">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="33511-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="33511-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="33511-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="33511-829">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="33511-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="33511-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="33511-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="33511-831">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="33511-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="33511-832">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="33511-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="33511-833">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="33511-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="33511-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="33511-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="33511-835">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="33511-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="33511-836">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="33511-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="33511-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-837">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-838">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="33511-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="33511-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="33511-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="33511-840">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="33511-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="33511-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="33511-841">AzureRM.Websites</span></span>
* <span data-ttu-id="33511-842">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="33511-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="33511-843">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="33511-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="33511-844">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="33511-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="33511-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="33511-846">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="33511-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="33511-847">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-848">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-848">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-849">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="33511-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="33511-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="33511-850">AzureRM.Compute</span></span>
* <span data-ttu-id="33511-851">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="33511-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="33511-852">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="33511-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="33511-853">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="33511-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="33511-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="33511-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="33511-855">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="33511-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="33511-856">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="33511-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="33511-857">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="33511-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="33511-858">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="33511-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="33511-859">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="33511-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="33511-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="33511-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="33511-861">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="33511-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="33511-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-862">AzureRM.Network</span></span>
* <span data-ttu-id="33511-863">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="33511-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="33511-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="33511-864">AzureRM.Resources</span></span>
* <span data-ttu-id="33511-865">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="33511-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="33511-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="33511-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="33511-867">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="33511-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="33511-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-868">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-869">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="33511-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="33511-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="33511-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33511-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="33511-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="33511-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="33511-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="33511-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="33511-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="33511-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="33511-875">AzureRM.Websites</span></span>
* <span data-ttu-id="33511-876">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="33511-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="33511-877">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="33511-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="33511-878">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="33511-878">AzureRM.Profile</span></span>
* <span data-ttu-id="33511-879">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="33511-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="33511-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="33511-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="33511-881">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="33511-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="33511-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="33511-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="33511-883">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="33511-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="33511-884">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="33511-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="33511-885">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="33511-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="33511-886">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="33511-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="33511-887">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="33511-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="33511-888">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="33511-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="33511-889">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="33511-889">Added support for MSI identity</span></span>
* <span data-ttu-id="33511-890">Suporte adicionado para aceitar políticas por meio da Observação do Url: Os cmdlets a seguir serão preteridos na versão futura</span><span class="sxs-lookup"><span data-stu-id="33511-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="33511-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="33511-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="33511-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="33511-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="33511-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="33511-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="33511-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="33511-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="33511-895">AzureRM.Batch</span></span>
* <span data-ttu-id="33511-896">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="33511-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="33511-897">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="33511-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="33511-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="33511-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="33511-899">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="33511-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="33511-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="33511-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="33511-901">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="33511-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="33511-902">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33511-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="33511-903">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="33511-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="33511-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="33511-904">AzureRM.Network</span></span>
* <span data-ttu-id="33511-905">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="33511-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="33511-906">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="33511-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="33511-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="33511-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="33511-908">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="33511-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="33511-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="33511-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="33511-910">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="33511-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="33511-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="33511-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="33511-912">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="33511-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="33511-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="33511-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="33511-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="33511-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="33511-915">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="33511-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="33511-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="33511-916">AzureRM.Sql</span></span>
* <span data-ttu-id="33511-917">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="33511-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="33511-918">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="33511-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="33511-919">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="33511-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="33511-920">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="33511-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="33511-921">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="33511-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="33511-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="33511-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="33511-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="33511-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="33511-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="33511-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="33511-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="33511-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="33511-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="33511-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="33511-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="33511-928">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="33511-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
