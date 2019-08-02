---
ms.openlocfilehash: e72aae940b48543d6a99801032186112748ea48b
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657953"
---
## <a name="250---july-2019"></a><span data-ttu-id="d6fa2-101">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-102">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-103">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d6fa2-103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d6fa2-104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d6fa2-105">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-106">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-107">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-107">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="d6fa2-108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-108">Az.CognitiveServices</span></span>
* <span data-ttu-id="d6fa2-109">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-110">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-111">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d6fa2-112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d6fa2-112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d6fa2-113">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="d6fa2-113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d6fa2-114">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="d6fa2-114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d6fa2-115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6fa2-115">Az.DataFactory</span></span>
* <span data-ttu-id="d6fa2-116">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="d6fa2-116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d6fa2-117">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="d6fa2-117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d6fa2-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-118">Az.EventHub</span></span>
* <span data-ttu-id="d6fa2-119">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d6fa2-119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d6fa2-120">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="d6fa2-120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d6fa2-121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d6fa2-121">Az.KeyVault</span></span>
* <span data-ttu-id="d6fa2-122">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="d6fa2-122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d6fa2-123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d6fa2-123">Az.LogicApp</span></span>
* <span data-ttu-id="d6fa2-124">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="d6fa2-124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d6fa2-125">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="d6fa2-125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d6fa2-126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-126">Az.ManagedServices</span></span>
* <span data-ttu-id="d6fa2-127">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="d6fa2-127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-128">Az.Network</span></span>
* <span data-ttu-id="d6fa2-129">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d6fa2-130">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d6fa2-130">New cmdlets</span></span>
        - <span data-ttu-id="d6fa2-131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6fa2-131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d6fa2-132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6fa2-132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d6fa2-133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d6fa2-134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d6fa2-135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d6fa2-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d6fa2-137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d6fa2-137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d6fa2-138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6fa2-138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d6fa2-139">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="d6fa2-139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d6fa2-140">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="d6fa2-140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d6fa2-141">Parâmetro opcional -PrivateEndpointNetworkPoliciesFlag adicionado para indicar que habilitar ou desabilitar aplica políticas de rede no ponto de extremidade privado nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag to indicate that enable or disable apply network policies on pivate endpoint in this subnet.</span></span>
        - <span data-ttu-id="d6fa2-142">Parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag adicionado para indicar que habilitar ou desabilitar aplica políticas de rede no serviço de link privado nesta sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag to indicate that enable or disable apply network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d6fa2-143">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="d6fa2-143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d6fa2-144">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="d6fa2-144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d6fa2-145">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-145">Updated cmdlets</span></span>
        - <span data-ttu-id="d6fa2-146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d6fa2-147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d6fa2-148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d6fa2-149">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d6fa2-150">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d6fa2-151">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-151">Updated cmdlet:</span></span>
        - <span data-ttu-id="d6fa2-152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d6fa2-153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d6fa2-154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d6fa2-155">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="d6fa2-155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d6fa2-156">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d6fa2-157">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d6fa2-158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-158">Az.OperationalInsights</span></span>
* <span data-ttu-id="d6fa2-159">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-159">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="d6fa2-160">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="d6fa2-160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-161">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-162">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d6fa2-163">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d6fa2-164">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d6fa2-165">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d6fa2-166">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d6fa2-167">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d6fa2-168">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d6fa2-169">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d6fa2-170">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d6fa2-171">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-172">Az.Resources</span></span>
- <span data-ttu-id="d6fa2-173">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d6fa2-174">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d6fa2-174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d6fa2-175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d6fa2-175">Az.ServiceBus</span></span>
* <span data-ttu-id="d6fa2-176">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d6fa2-176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d6fa2-177">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="d6fa2-177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-178">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-179">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d6fa2-179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d6fa2-180">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="d6fa2-180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d6fa2-181">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-182">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-183">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="d6fa2-183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d6fa2-184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d6fa2-184">Az.StorageSync</span></span>
* <span data-ttu-id="d6fa2-185">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d6fa2-186">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="d6fa2-186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-187">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-188">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6fa2-188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d6fa2-189">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d6fa2-189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d6fa2-190">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="d6fa2-190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d6fa2-191">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-192">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-193">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="d6fa2-193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d6fa2-194">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d6fa2-195">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d6fa2-195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d6fa2-196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-196">Az.Advisor</span></span>
* <span data-ttu-id="d6fa2-197">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d6fa2-198">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d6fa2-199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6fa2-199">Az.ApiManagement</span></span>
* <span data-ttu-id="d6fa2-200">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="d6fa2-200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d6fa2-201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d6fa2-202">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="d6fa2-202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d6fa2-203">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d6fa2-204">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="d6fa2-204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d6fa2-205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d6fa2-206">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="d6fa2-206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-207">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-208">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-209">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-210">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d6fa2-211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6fa2-211">Az.DataFactory</span></span>
* <span data-ttu-id="d6fa2-212">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d6fa2-213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d6fa2-213">Az.EventGrid</span></span>
* <span data-ttu-id="d6fa2-214">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d6fa2-215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-215">Az.IotHub</span></span>
* <span data-ttu-id="d6fa2-216">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-217">Az.Network</span></span>
* <span data-ttu-id="d6fa2-218">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="d6fa2-218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d6fa2-219">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d6fa2-220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-220">Az.PolicyInsights</span></span>
* <span data-ttu-id="d6fa2-221">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="d6fa2-221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d6fa2-222">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="d6fa2-222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d6fa2-223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-223">Az.OperationalInsights</span></span>
* <span data-ttu-id="d6fa2-224">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d6fa2-224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-225">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-226">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="d6fa2-226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-227">Az.Resources</span></span>
    - <span data-ttu-id="d6fa2-228">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="d6fa2-228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d6fa2-229">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="d6fa2-229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d6fa2-230">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="d6fa2-230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d6fa2-231">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d6fa2-232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d6fa2-232">Az.ServiceBus</span></span>
* <span data-ttu-id="d6fa2-233">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-234">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-235">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="d6fa2-235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d6fa2-236">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d6fa2-237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d6fa2-237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d6fa2-238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d6fa2-238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d6fa2-239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d6fa2-239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d6fa2-240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d6fa2-240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d6fa2-241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d6fa2-241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d6fa2-242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d6fa2-242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d6fa2-243">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="d6fa2-243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-244">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-245">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d6fa2-246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d6fa2-246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d6fa2-247">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d6fa2-248">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="d6fa2-248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d6fa2-249">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d6fa2-250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d6fa2-251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d6fa2-252">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d6fa2-253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d6fa2-253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d6fa2-254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d6fa2-254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d6fa2-255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d6fa2-255">Az.StorageSync</span></span>
* <span data-ttu-id="d6fa2-256">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d6fa2-257">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-258">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-259">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="d6fa2-259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d6fa2-260">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="d6fa2-260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d6fa2-261">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="d6fa2-261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d6fa2-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d6fa2-262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d6fa2-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d6fa2-263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-264">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-265">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d6fa2-266">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d6fa2-267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d6fa2-267">Az.Dns</span></span>
* <span data-ttu-id="d6fa2-268">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d6fa2-269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d6fa2-269">Az.EventGrid</span></span>
* <span data-ttu-id="d6fa2-270">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d6fa2-271">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-271">New cmdlets:</span></span>
    - <span data-ttu-id="d6fa2-272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d6fa2-272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d6fa2-273">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d6fa2-274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d6fa2-274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d6fa2-275">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d6fa2-276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d6fa2-276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d6fa2-277">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d6fa2-278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d6fa2-278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d6fa2-279">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d6fa2-280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d6fa2-280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d6fa2-281">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d6fa2-282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d6fa2-283">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d6fa2-284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d6fa2-284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d6fa2-285">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="d6fa2-285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="d6fa2-286">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d6fa2-287">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d6fa2-288">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-288">Updated cmdlets:</span></span>
    - <span data-ttu-id="d6fa2-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d6fa2-290">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d6fa2-291">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d6fa2-292">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="d6fa2-292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d6fa2-293">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d6fa2-294">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="d6fa2-294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d6fa2-295">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d6fa2-296">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d6fa2-297">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="d6fa2-297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="d6fa2-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d6fa2-299">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d6fa2-300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d6fa2-300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d6fa2-301">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d6fa2-302">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d6fa2-303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-303">Az.FrontDoor</span></span>
* <span data-ttu-id="d6fa2-304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d6fa2-304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d6fa2-305">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="d6fa2-305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d6fa2-306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d6fa2-306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d6fa2-307">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="d6fa2-307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-308">Az.Network</span></span>
* <span data-ttu-id="d6fa2-309">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d6fa2-309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d6fa2-310">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d6fa2-310">New cmdlets</span></span>
        - <span data-ttu-id="d6fa2-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d6fa2-311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d6fa2-312">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d6fa2-312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d6fa2-313">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d6fa2-313">New cmdlets</span></span> 
        - <span data-ttu-id="d6fa2-314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d6fa2-314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d6fa2-315">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6fa2-315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d6fa2-316">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d6fa2-316">New cmdlets</span></span> 
        - <span data-ttu-id="d6fa2-317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6fa2-317">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="d6fa2-318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6fa2-318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d6fa2-319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d6fa2-319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d6fa2-320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d6fa2-321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d6fa2-322">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6fa2-322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d6fa2-323">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d6fa2-323">New cmdlets</span></span>
        - <span data-ttu-id="d6fa2-324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6fa2-324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d6fa2-325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6fa2-325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d6fa2-326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d6fa2-326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d6fa2-327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d6fa2-328">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d6fa2-329">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d6fa2-330">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d6fa2-331">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d6fa2-332">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d6fa2-333">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d6fa2-333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d6fa2-334">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d6fa2-335">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d6fa2-336">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d6fa2-337">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d6fa2-338">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d6fa2-338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d6fa2-339">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="d6fa2-339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d6fa2-340">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d6fa2-340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d6fa2-341">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d6fa2-342">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d6fa2-343">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="d6fa2-343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d6fa2-344">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d6fa2-344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d6fa2-345">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="d6fa2-345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d6fa2-346">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d6fa2-346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="d6fa2-347">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="d6fa2-348">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d6fa2-349">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d6fa2-350">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d6fa2-351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-351">Az.OperationalInsights</span></span>
* <span data-ttu-id="d6fa2-352">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-353">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-354">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d6fa2-355">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d6fa2-356">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d6fa2-357">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d6fa2-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="d6fa2-359">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-360">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-361">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d6fa2-361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d6fa2-362">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d6fa2-362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d6fa2-363">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d6fa2-364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d6fa2-364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d6fa2-365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d6fa2-365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d6fa2-366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d6fa2-366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d6fa2-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d6fa2-367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d6fa2-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d6fa2-368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-369">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-370">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d6fa2-370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d6fa2-371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-371">New-AzStorageAccount</span></span>
* <span data-ttu-id="d6fa2-372">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="d6fa2-372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d6fa2-373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-374">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-375">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="d6fa2-375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d6fa2-376">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d6fa2-376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d6fa2-377">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d6fa2-378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d6fa2-378">Az.Cdn</span></span>
* <span data-ttu-id="d6fa2-379">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-380">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-381">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d6fa2-382">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d6fa2-382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d6fa2-383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-383">Az.EventHub</span></span>
* <span data-ttu-id="d6fa2-384">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d6fa2-385">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fa2-385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-386">Az.Network</span></span>
* <span data-ttu-id="d6fa2-387">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="d6fa2-387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d6fa2-388">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="d6fa2-388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d6fa2-389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-389">Az.PolicyInsights</span></span>
* <span data-ttu-id="d6fa2-390">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d6fa2-390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-391">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-392">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="d6fa2-392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d6fa2-393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d6fa2-393">Az.ServiceBus</span></span>
* <span data-ttu-id="d6fa2-394">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fa2-394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d6fa2-395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-395">Az.ServiceFabric</span></span>
* <span data-ttu-id="d6fa2-396">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d6fa2-397">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-398">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-399">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d6fa2-400">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d6fa2-401">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d6fa2-401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d6fa2-402">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-403">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-404">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d6fa2-405">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d6fa2-406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6fa2-406">Az.ApiManagement</span></span>
* <span data-ttu-id="d6fa2-407">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d6fa2-408">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d6fa2-409">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d6fa2-410">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d6fa2-411">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d6fa2-412">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="d6fa2-412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d6fa2-413">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d6fa2-414">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d6fa2-415">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6fa2-415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d6fa2-416">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="d6fa2-416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d6fa2-417">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d6fa2-418">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="d6fa2-418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d6fa2-419">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="d6fa2-419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d6fa2-420">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d6fa2-421">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d6fa2-422">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d6fa2-423">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d6fa2-424">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d6fa2-424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d6fa2-425">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-425">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="d6fa2-426">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="d6fa2-426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d6fa2-427">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="d6fa2-427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d6fa2-428">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d6fa2-429">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d6fa2-430">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6fa2-430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="d6fa2-431">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d6fa2-432">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d6fa2-433">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d6fa2-434">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d6fa2-435">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d6fa2-436">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="d6fa2-436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d6fa2-437">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-437">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="d6fa2-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d6fa2-438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d6fa2-439">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d6fa2-440">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d6fa2-441">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d6fa2-442">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="d6fa2-442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d6fa2-443">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d6fa2-444">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d6fa2-445">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d6fa2-446">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-446">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="d6fa2-447">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d6fa2-448">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d6fa2-449">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d6fa2-450">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d6fa2-451">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d6fa2-452">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d6fa2-453">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-453">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="d6fa2-454">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="d6fa2-455">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d6fa2-456">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d6fa2-457">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d6fa2-458">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d6fa2-459">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d6fa2-460">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d6fa2-461">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d6fa2-462">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d6fa2-463">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d6fa2-464">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d6fa2-465">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d6fa2-466">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d6fa2-467">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d6fa2-467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d6fa2-468">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d6fa2-469">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d6fa2-470">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d6fa2-471">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="d6fa2-471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d6fa2-472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d6fa2-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d6fa2-473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d6fa2-474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d6fa2-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d6fa2-475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d6fa2-476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d6fa2-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d6fa2-477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d6fa2-478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d6fa2-479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d6fa2-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d6fa2-481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-481">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="d6fa2-482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d6fa2-483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-484">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-485">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d6fa2-486">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d6fa2-486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d6fa2-487">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d6fa2-487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d6fa2-488">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d6fa2-489">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d6fa2-489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d6fa2-490">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d6fa2-491">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-492">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-493">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d6fa2-494">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-495">Az.DataLakeStore</span></span>
* <span data-ttu-id="d6fa2-496">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d6fa2-497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-497">Az.Monitor</span></span>
* <span data-ttu-id="d6fa2-498">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="d6fa2-498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-499">Az.Network</span></span>
* <span data-ttu-id="d6fa2-500">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d6fa2-501">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-501">Updated cmdlet:</span></span>
        - <span data-ttu-id="d6fa2-502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d6fa2-503">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d6fa2-503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-504">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-505">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="d6fa2-505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-506">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-507">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="d6fa2-507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d6fa2-508">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-509">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-510">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="d6fa2-510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d6fa2-511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-511">Az.CognitiveServices</span></span>
* <span data-ttu-id="d6fa2-512">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d6fa2-513">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-514">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-515">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d6fa2-516">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d6fa2-517">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d6fa2-518">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d6fa2-519">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d6fa2-520">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d6fa2-520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="d6fa2-521">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="d6fa2-521">Breaking changes</span></span>
    - <span data-ttu-id="d6fa2-522">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d6fa2-523">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d6fa2-524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d6fa2-524">Az.DeploymentManager</span></span>
* <span data-ttu-id="d6fa2-525">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d6fa2-526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d6fa2-526">Az.Dns</span></span>
* <span data-ttu-id="d6fa2-527">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="d6fa2-527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d6fa2-528">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d6fa2-529">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d6fa2-530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-530">Az.FrontDoor</span></span>
* <span data-ttu-id="d6fa2-531">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d6fa2-532">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d6fa2-533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d6fa2-533">Az.HDInsight</span></span>
* <span data-ttu-id="d6fa2-534">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d6fa2-535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d6fa2-535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d6fa2-536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d6fa2-536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d6fa2-537">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d6fa2-537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d6fa2-538">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d6fa2-539">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d6fa2-540">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d6fa2-541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-541">Az.Monitor</span></span>
* <span data-ttu-id="d6fa2-542">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="d6fa2-542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="d6fa2-543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d6fa2-543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d6fa2-544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d6fa2-545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d6fa2-545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d6fa2-546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d6fa2-547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d6fa2-547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d6fa2-548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d6fa2-548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d6fa2-549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d6fa2-550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d6fa2-551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d6fa2-552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d6fa2-553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d6fa2-554">[Mais](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="d6fa2-554">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d6fa2-555">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d6fa2-555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-556">Az.Network</span></span>
* <span data-ttu-id="d6fa2-557">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="d6fa2-557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d6fa2-558">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d6fa2-558">New cmdlets</span></span>
        - <span data-ttu-id="d6fa2-559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d6fa2-559">New-AzNatGateway</span></span>
        - <span data-ttu-id="d6fa2-560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d6fa2-560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d6fa2-561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d6fa2-561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d6fa2-562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d6fa2-562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d6fa2-563">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-563">Updated cmdlets</span></span>
        - <span data-ttu-id="d6fa2-564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d6fa2-564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d6fa2-565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d6fa2-565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d6fa2-566">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d6fa2-567">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d6fa2-568">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d6fa2-569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-569">Az.PolicyInsights</span></span>
* <span data-ttu-id="d6fa2-570">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d6fa2-571">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d6fa2-572">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-574">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d6fa2-575">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d6fa2-576">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d6fa2-577">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d6fa2-578">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d6fa2-579">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d6fa2-580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d6fa2-580">Az.Relay</span></span>
* <span data-ttu-id="d6fa2-581">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="d6fa2-581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d6fa2-582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d6fa2-582">Az.ServiceBus</span></span>
* <span data-ttu-id="d6fa2-583">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d6fa2-583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-584">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-585">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="d6fa2-585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d6fa2-586">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d6fa2-587">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d6fa2-588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-588">New-AzStorageAccount</span></span>
* <span data-ttu-id="d6fa2-589">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d6fa2-590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d6fa2-591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d6fa2-592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-593">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-594">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d6fa2-594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d6fa2-595">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d6fa2-596">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d6fa2-597">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d6fa2-597">Highlights since the last major release</span></span>
* <span data-ttu-id="d6fa2-598">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d6fa2-598">General availability of `Az` module</span></span>
* <span data-ttu-id="d6fa2-599">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d6fa2-599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d6fa2-600">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d6fa2-600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d6fa2-601">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d6fa2-602">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d6fa2-602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d6fa2-603">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d6fa2-604">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d6fa2-604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-605">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-606">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="d6fa2-606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d6fa2-607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d6fa2-607">Az.Batch</span></span>
* <span data-ttu-id="d6fa2-608">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d6fa2-609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d6fa2-609">Az.Cdn</span></span>
* <span data-ttu-id="d6fa2-610">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d6fa2-611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-611">Az.CognitiveServices</span></span>
* <span data-ttu-id="d6fa2-612">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-613">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-614">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d6fa2-615">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d6fa2-616">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d6fa2-616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d6fa2-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6fa2-617">Az.DataFactory</span></span>
* <span data-ttu-id="d6fa2-618">Adicionar SsisProperties se NodeCount não for nulo para o tempo de execução de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-619">Az.DataLakeStore</span></span>
* <span data-ttu-id="d6fa2-620">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d6fa2-621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d6fa2-621">Az.EventGrid</span></span>
* <span data-ttu-id="d6fa2-622">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d6fa2-623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-623">Az.EventHub</span></span>
* <span data-ttu-id="d6fa2-624">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d6fa2-624">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="d6fa2-625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d6fa2-625">Az.HDInsight</span></span>
* <span data-ttu-id="d6fa2-626">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d6fa2-627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-627">Az.IotHub</span></span>
* <span data-ttu-id="d6fa2-628">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d6fa2-629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d6fa2-629">Az.KeyVault</span></span>
* <span data-ttu-id="d6fa2-630">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d6fa2-631">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d6fa2-631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d6fa2-632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d6fa2-632">Az.MachineLearning</span></span>
* <span data-ttu-id="d6fa2-633">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d6fa2-634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d6fa2-634">Az.Media</span></span>
* <span data-ttu-id="d6fa2-635">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d6fa2-636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-636">Az.Monitor</span></span>
  * <span data-ttu-id="d6fa2-637">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d6fa2-637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d6fa2-638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d6fa2-638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d6fa2-639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d6fa2-639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d6fa2-640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d6fa2-640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d6fa2-641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d6fa2-641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d6fa2-642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d6fa2-642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d6fa2-643">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="d6fa2-643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-644">Az.Network</span></span>
* <span data-ttu-id="d6fa2-645">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d6fa2-646">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d6fa2-646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d6fa2-647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d6fa2-647">Az.NotificationHubs</span></span>
* <span data-ttu-id="d6fa2-648">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d6fa2-649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-649">Az.OperationalInsights</span></span>
* <span data-ttu-id="d6fa2-650">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d6fa2-651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d6fa2-651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d6fa2-652">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-653">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-654">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d6fa2-655">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d6fa2-656">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d6fa2-656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d6fa2-657">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="d6fa2-657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d6fa2-658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d6fa2-658">Az.RedisCache</span></span>
* <span data-ttu-id="d6fa2-659">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-660">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-661">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d6fa2-661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-662">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-663">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="d6fa2-663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d6fa2-664">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d6fa2-665">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d6fa2-666">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d6fa2-667">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d6fa2-668">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d6fa2-669">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d6fa2-669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-670">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-671">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="d6fa2-671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d6fa2-672">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d6fa2-673">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d6fa2-674">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d6fa2-675">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d6fa2-676">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d6fa2-676">Highlights since the last major release</span></span>
* <span data-ttu-id="d6fa2-677">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d6fa2-677">General availability of `Az` module</span></span>
* <span data-ttu-id="d6fa2-678">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d6fa2-678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d6fa2-679">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d6fa2-679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d6fa2-680">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d6fa2-681">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d6fa2-681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d6fa2-682">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d6fa2-683">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d6fa2-683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-684">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-685">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d6fa2-685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d6fa2-686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-686">Az.AnalysisServices</span></span>
* <span data-ttu-id="d6fa2-687">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="d6fa2-687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d6fa2-688">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="d6fa2-688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-689">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-690">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d6fa2-691">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d6fa2-692">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-693">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-694">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d6fa2-695">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-695">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="d6fa2-696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d6fa2-696">Az.ContainerInstance</span></span>
* <span data-ttu-id="d6fa2-697">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="d6fa2-697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d6fa2-698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6fa2-698">Az.DataFactory</span></span>
* <span data-ttu-id="d6fa2-699">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="d6fa2-699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d6fa2-700">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-701">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-702">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="d6fa2-702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d6fa2-703">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d6fa2-704">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="d6fa2-704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d6fa2-705">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d6fa2-705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d6fa2-706">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="d6fa2-706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d6fa2-707">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d6fa2-707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-708">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-709">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-710">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-711">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d6fa2-712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d6fa2-712">New-AzStorageContext</span></span>
* <span data-ttu-id="d6fa2-713">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d6fa2-713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d6fa2-714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d6fa2-714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d6fa2-715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d6fa2-715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d6fa2-716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d6fa2-717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d6fa2-718">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d6fa2-719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d6fa2-719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d6fa2-720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d6fa2-720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d6fa2-721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d6fa2-721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d6fa2-722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d6fa2-722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d6fa2-723">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d6fa2-724">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d6fa2-724">Highlights since the last major release</span></span>
* <span data-ttu-id="d6fa2-725">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d6fa2-725">General availability of `Az` module</span></span>
* <span data-ttu-id="d6fa2-726">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d6fa2-726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d6fa2-727">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d6fa2-727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d6fa2-728">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d6fa2-729">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d6fa2-729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d6fa2-730">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d6fa2-731">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d6fa2-731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-732">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-733">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d6fa2-734">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="d6fa2-734">Dynamic grouping</span></span>
    * <span data-ttu-id="d6fa2-735">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="d6fa2-735">Pre-Post script</span></span>
    * <span data-ttu-id="d6fa2-736">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="d6fa2-736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-737">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-738">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="d6fa2-738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d6fa2-739">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d6fa2-740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d6fa2-740">Az.KeyVault</span></span>
* <span data-ttu-id="d6fa2-741">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="d6fa2-741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-742">Az.Network</span></span>
* <span data-ttu-id="d6fa2-743">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d6fa2-744">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-745">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-746">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d6fa2-747">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="d6fa2-747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-748">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-749">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d6fa2-750">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="d6fa2-750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-751">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-752">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-753">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-754">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d6fa2-754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d6fa2-755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d6fa2-756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d6fa2-757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d6fa2-758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d6fa2-758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d6fa2-759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d6fa2-759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d6fa2-760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-761">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-762">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="d6fa2-762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="d6fa2-763">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-764">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-765">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="d6fa2-765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d6fa2-766">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-767">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-768">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d6fa2-769">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d6fa2-770">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="d6fa2-770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d6fa2-771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d6fa2-771">Az.Cdn</span></span>
* <span data-ttu-id="d6fa2-772">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-773">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-774">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="d6fa2-774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d6fa2-775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6fa2-775">Az.DataFactory</span></span>
* <span data-ttu-id="d6fa2-776">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="d6fa2-776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d6fa2-777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d6fa2-777">Az.LogicApp</span></span>
* <span data-ttu-id="d6fa2-778">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-779">Az.Network</span></span>
* <span data-ttu-id="d6fa2-780">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-781">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-782">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d6fa2-783">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="d6fa2-783">SDK Update</span></span>
* <span data-ttu-id="d6fa2-784">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d6fa2-784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d6fa2-785">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d6fa2-785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-786">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-787">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="d6fa2-787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d6fa2-788">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d6fa2-788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d6fa2-789">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d6fa2-789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d6fa2-790">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d6fa2-790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d6fa2-791">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d6fa2-791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d6fa2-792">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d6fa2-792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-793">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-794">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d6fa2-795">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-796">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-797">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d6fa2-798">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d6fa2-799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-799">Az.AnalysisServices</span></span>
* <span data-ttu-id="d6fa2-800">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-801">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-802">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d6fa2-803">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d6fa2-804">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d6fa2-805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-805">Az.CognitiveServices</span></span>
* <span data-ttu-id="d6fa2-806">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-807">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-808">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="d6fa2-808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d6fa2-809">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="d6fa2-809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d6fa2-810">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d6fa2-811">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-812">Az.DataLakeStore</span></span>
* <span data-ttu-id="d6fa2-813">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d6fa2-814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-814">Az.EventHub</span></span>
* <span data-ttu-id="d6fa2-815">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="d6fa2-816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d6fa2-816">Az.KeyVault</span></span>
* <span data-ttu-id="d6fa2-817">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d6fa2-817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d6fa2-818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d6fa2-818">Az.LogicApp</span></span>
* <span data-ttu-id="d6fa2-819">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="d6fa2-819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d6fa2-820">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="d6fa2-820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d6fa2-821">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="d6fa2-821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d6fa2-822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d6fa2-822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d6fa2-823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d6fa2-823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d6fa2-824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d6fa2-824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d6fa2-825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d6fa2-825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d6fa2-826">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="d6fa2-826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d6fa2-827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d6fa2-828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d6fa2-829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d6fa2-830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d6fa2-831">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="d6fa2-831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d6fa2-832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-832">Az.Monitor</span></span>
* <span data-ttu-id="d6fa2-833">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-834">Az.Network</span></span>
* <span data-ttu-id="d6fa2-835">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d6fa2-835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d6fa2-836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-836">Az.OperationalInsights</span></span>
* <span data-ttu-id="d6fa2-837">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d6fa2-838">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="d6fa2-839">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="d6fa2-840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-840">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-841">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d6fa2-841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d6fa2-842">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d6fa2-842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d6fa2-843">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d6fa2-843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d6fa2-844">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="d6fa2-844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-845">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-846">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d6fa2-846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d6fa2-847">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="d6fa2-847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-848">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-849">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="d6fa2-849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d6fa2-850">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-851">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-852">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d6fa2-852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d6fa2-853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-853">Az.AnalysisServices</span></span>
<span data-ttu-id="d6fa2-854">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-855">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-856">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="d6fa2-856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d6fa2-857">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d6fa2-857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d6fa2-858">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-859">Az.RecoveryServices</span></span>
<span data-ttu-id="d6fa2-860">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-861">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-862">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-862">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="d6fa2-863">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d6fa2-863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d6fa2-864">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="d6fa2-864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="d6fa2-865">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d6fa2-865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-866">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-867">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d6fa2-868">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="d6fa2-868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d6fa2-869">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="d6fa2-869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d6fa2-870">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-871">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-872">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="d6fa2-872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d6fa2-873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-873">Az.AnalysisServices</span></span>
* <span data-ttu-id="d6fa2-874">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d6fa2-874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-875">Az.RecoveryServices</span></span>
* <span data-ttu-id="d6fa2-876">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d6fa2-876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d6fa2-877">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-878">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-879">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d6fa2-879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d6fa2-880">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d6fa2-881">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="d6fa2-881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d6fa2-882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d6fa2-882">Az.Aks</span></span>
* <span data-ttu-id="d6fa2-883">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d6fa2-884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-884">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-885">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="d6fa2-885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d6fa2-886">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d6fa2-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d6fa2-887">Az.Cdn</span></span>
* <span data-ttu-id="d6fa2-888">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-889">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-890">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d6fa2-891">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d6fa2-891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d6fa2-892">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d6fa2-892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d6fa2-893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d6fa2-893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d6fa2-894">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d6fa2-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d6fa2-895">Az.DataFactory</span></span>
* <span data-ttu-id="d6fa2-896">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="d6fa2-896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="d6fa2-898">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d6fa2-898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d6fa2-899">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d6fa2-899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d6fa2-900">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d6fa2-901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-901">Az.IotHub</span></span>
* <span data-ttu-id="d6fa2-902">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d6fa2-903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d6fa2-903">Az.KeyVault</span></span>
* <span data-ttu-id="d6fa2-904">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-905">Az.Network</span></span>
* <span data-ttu-id="d6fa2-906">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-907">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-908">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d6fa2-909">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d6fa2-910">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="d6fa2-910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d6fa2-911">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d6fa2-911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d6fa2-912">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d6fa2-912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d6fa2-913">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d6fa2-914">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d6fa2-914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d6fa2-915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-915">Az.ServiceFabric</span></span>
* <span data-ttu-id="d6fa2-916">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="d6fa2-916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d6fa2-917">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-917">Fix some error messages.</span></span>
* <span data-ttu-id="d6fa2-918">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d6fa2-919">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d6fa2-920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d6fa2-920">Az.SignalR</span></span>
* <span data-ttu-id="d6fa2-921">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-922">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-923">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d6fa2-924">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d6fa2-924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d6fa2-925">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="d6fa2-925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d6fa2-926">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-927">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-928">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d6fa2-929">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d6fa2-930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d6fa2-930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d6fa2-931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d6fa2-931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d6fa2-932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d6fa2-932">Az.TrafficManager</span></span>
* <span data-ttu-id="d6fa2-933">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-934">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-935">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d6fa2-935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d6fa2-936">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d6fa2-937">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d6fa2-938">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d6fa2-938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d6fa2-939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-939">Az.Accounts</span></span>
* <span data-ttu-id="d6fa2-940">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="d6fa2-940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-941">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-942">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d6fa2-943">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d6fa2-943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d6fa2-944">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-945">Az.DataLakeStore</span></span>
* <span data-ttu-id="d6fa2-946">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d6fa2-947">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="d6fa2-947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d6fa2-948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d6fa2-948">Az.EventGrid</span></span>
* <span data-ttu-id="d6fa2-949">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d6fa2-950">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d6fa2-950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d6fa2-951">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d6fa2-952">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d6fa2-952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d6fa2-953">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d6fa2-954">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d6fa2-955">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d6fa2-956">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d6fa2-956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d6fa2-957">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d6fa2-958">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d6fa2-958">Dead letter endpoint.</span></span>
* <span data-ttu-id="d6fa2-959">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d6fa2-960">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d6fa2-961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-961">Az.IotHub</span></span>
* <span data-ttu-id="d6fa2-962">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="d6fa2-962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d6fa2-963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d6fa2-963">Az.LogicApp</span></span>
* <span data-ttu-id="d6fa2-964">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="d6fa2-964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-965">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-966">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d6fa2-967">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d6fa2-967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d6fa2-968">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6fa2-968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d6fa2-969">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d6fa2-969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d6fa2-970">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d6fa2-971">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d6fa2-971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d6fa2-972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d6fa2-972">Az.SignalR</span></span>
* <span data-ttu-id="d6fa2-973">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-974">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-975">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d6fa2-976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-976">Az.Storage</span></span>
* <span data-ttu-id="d6fa2-977">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="d6fa2-977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d6fa2-978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d6fa2-978">New-AzStorageContext</span></span>
* <span data-ttu-id="d6fa2-979">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d6fa2-980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d6fa2-980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-981">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-982">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="d6fa2-982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d6fa2-983">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d6fa2-984">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d6fa2-984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d6fa2-985">Geral</span><span class="sxs-lookup"><span data-stu-id="d6fa2-985">General</span></span>

- <span data-ttu-id="d6fa2-986">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="d6fa2-986">General Availability of Az Module</span></span>
- <span data-ttu-id="d6fa2-987">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-987">Online help for each module</span></span>
- <span data-ttu-id="d6fa2-988">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="d6fa2-988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d6fa2-989">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="d6fa2-989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d6fa2-990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-990">Az.Accounts</span></span>
- <span data-ttu-id="d6fa2-991">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-991">Changed from Az.Profile</span></span>
- <span data-ttu-id="d6fa2-992">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="d6fa2-992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d6fa2-993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6fa2-993">Az.ApiManagement</span></span>
- <span data-ttu-id="d6fa2-994">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="d6fa2-994">Fixes for #7002</span></span>
- <span data-ttu-id="d6fa2-995">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d6fa2-996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d6fa2-996">Az.Batch</span></span>
- <span data-ttu-id="d6fa2-997">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d6fa2-998">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d6fa2-999">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d6fa2-1000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1000">Az.Billing</span></span>
- <span data-ttu-id="d6fa2-1001">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d6fa2-1002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1002">Az.CognitivServices</span></span>
- <span data-ttu-id="d6fa2-1003">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d6fa2-1004">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d6fa2-1005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1005">Az.ContainerInstance</span></span>
- <span data-ttu-id="d6fa2-1006">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d6fa2-1007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d6fa2-1008">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-1009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1009">Az.DataLakeStore</span></span>
- <span data-ttu-id="d6fa2-1010">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d6fa2-1011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1011">Az.Monitor</span></span>
- <span data-ttu-id="d6fa2-1012">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d6fa2-1013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1013">Az.KeyVault</span></span>
- <span data-ttu-id="d6fa2-1014">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d6fa2-1015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1015">Az.MachineLearning</span></span>
- <span data-ttu-id="d6fa2-1016">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d6fa2-1017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1017">Az.Media</span></span>
- <span data-ttu-id="d6fa2-1018">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d6fa2-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1019">Az.Network</span></span>
<span data-ttu-id="d6fa2-1020">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d6fa2-1021">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1021">New cmdlets added:</span></span>
        - <span data-ttu-id="d6fa2-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d6fa2-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d6fa2-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d6fa2-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d6fa2-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d6fa2-1027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d6fa2-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d6fa2-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d6fa2-1030">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d6fa2-1031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d6fa2-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d6fa2-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d6fa2-1034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d6fa2-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d6fa2-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d6fa2-1037">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d6fa2-1038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d6fa2-1039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d6fa2-1040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d6fa2-1041">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d6fa2-1042">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d6fa2-1043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1043">Az.OperationalInsights</span></span>
- <span data-ttu-id="d6fa2-1044">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d6fa2-1045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1045">Az.Profile</span></span>
- <span data-ttu-id="d6fa2-1046">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-1047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1047">Az.RecoveryServices</span></span>
- <span data-ttu-id="d6fa2-1048">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d6fa2-1049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1049">Az.Resources</span></span>
- <span data-ttu-id="d6fa2-1050">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d6fa2-1051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1051">Az.ServiceFabric</span></span>
- <span data-ttu-id="d6fa2-1052">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d6fa2-1053">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d6fa2-1054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1054">Az.SIgnalR</span></span>
- <span data-ttu-id="d6fa2-1055">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d6fa2-1056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1056">Az.Sql</span></span>
- <span data-ttu-id="d6fa2-1057">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d6fa2-1058">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d6fa2-1059">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d6fa2-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1060">Az.Storage</span></span>
- <span data-ttu-id="d6fa2-1061">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d6fa2-1062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1062">Az.Websites</span></span>
- <span data-ttu-id="d6fa2-1063">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d6fa2-1064">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d6fa2-1065">Geral</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1065">General</span></span>

* <span data-ttu-id="d6fa2-1066">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d6fa2-1067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1067">Az.Compute</span></span>

* <span data-ttu-id="d6fa2-1068">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-1069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1069">Az.DataLakeStore</span></span>

* <span data-ttu-id="d6fa2-1070">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d6fa2-1071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1071">Az.FrontDoor</span></span>

* <span data-ttu-id="d6fa2-1072">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1072">Fixed some broken links</span></span>
    - <span data-ttu-id="d6fa2-1073">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d6fa2-1074">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d6fa2-1075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1075">Az.RecoveryServices</span></span>

* <span data-ttu-id="d6fa2-1076">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d6fa2-1077">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d6fa2-1078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1078">Az.Resources</span></span>

* <span data-ttu-id="d6fa2-1079">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d6fa2-1080">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d6fa2-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1081">Az.Sql</span></span>

* <span data-ttu-id="d6fa2-1082">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d6fa2-1083">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d6fa2-1084">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d6fa2-1085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1085">Az.Storage</span></span>

* <span data-ttu-id="d6fa2-1086">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d6fa2-1087">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d6fa2-1088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d6fa2-1089">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1089">Support Static Website configuration</span></span>
    - <span data-ttu-id="d6fa2-1090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d6fa2-1091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d6fa2-1092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1092">Az.Websites</span></span>

* <span data-ttu-id="d6fa2-1093">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="d6fa2-1094">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d6fa2-1095">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d6fa2-1096">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d6fa2-1097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1097">Az.ApiManagement</span></span>
* <span data-ttu-id="d6fa2-1098">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d6fa2-1099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1099">Az.Automation</span></span>
* <span data-ttu-id="d6fa2-1100">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d6fa2-1101">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d6fa2-1102">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d6fa2-1103">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d6fa2-1104">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d6fa2-1105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1105">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-1106">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d6fa2-1107">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d6fa2-1108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1108">Az.ContainerInstance</span></span>
* <span data-ttu-id="d6fa2-1109">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d6fa2-1110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d6fa2-1111">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d6fa2-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1112">Az.Network</span></span>
* <span data-ttu-id="d6fa2-1113">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d6fa2-1114">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d6fa2-1115">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="d6fa2-1116">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d6fa2-1117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d6fa2-1118">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d6fa2-1119">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d6fa2-1120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d6fa2-1121">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d6fa2-1122">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d6fa2-1123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1123">Az.Relay</span></span>
* <span data-ttu-id="d6fa2-1124">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d6fa2-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1125">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-1126">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d6fa2-1127">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d6fa2-1128">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d6fa2-1129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1129">Az.ServiceFabric</span></span>
* <span data-ttu-id="d6fa2-1130">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d6fa2-1131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1131">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-1132">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d6fa2-1133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d6fa2-1134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d6fa2-1135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d6fa2-1136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d6fa2-1137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d6fa2-1138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d6fa2-1139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d6fa2-1140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d6fa2-1141">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d6fa2-1142">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d6fa2-1143">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d6fa2-1144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d6fa2-1145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d6fa2-1146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d6fa2-1147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d6fa2-1148">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d6fa2-1149">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d6fa2-1150">Geral</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1150">General</span></span>
* <span data-ttu-id="d6fa2-1151">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d6fa2-1152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1152">Az.Profile</span></span>
* <span data-ttu-id="d6fa2-1153">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d6fa2-1154">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d6fa2-1155">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d6fa2-1156">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d6fa2-1157">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d6fa2-1158">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d6fa2-1159">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d6fa2-1160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1160">Az.CognitiveServices</span></span>
* <span data-ttu-id="d6fa2-1161">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-1162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1162">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-1163">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d6fa2-1164">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d6fa2-1165">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-1166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1166">Az.DataLakeStore</span></span>
* <span data-ttu-id="d6fa2-1167">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d6fa2-1168">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d6fa2-1169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1169">Az.Insights</span></span>
* <span data-ttu-id="d6fa2-1170">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d6fa2-1171">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d6fa2-1172">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d6fa2-1173">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-1174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1174">Az.Network</span></span>
* <span data-ttu-id="d6fa2-1175">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d6fa2-1176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d6fa2-1177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d6fa2-1178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d6fa2-1179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d6fa2-1180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d6fa2-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d6fa2-1182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1182">Az.PolicyInsights</span></span>
* <span data-ttu-id="d6fa2-1183">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1184">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-1185">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d6fa2-1186">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d6fa2-1187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1187">Az.ServiceBus</span></span>
* <span data-ttu-id="d6fa2-1188">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d6fa2-1189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1189">Az.ServiceFabric</span></span>
* <span data-ttu-id="d6fa2-1190">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d6fa2-1191">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d6fa2-1192">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d6fa2-1193">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d6fa2-1194">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d6fa2-1195">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d6fa2-1196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1196">Az.Profile</span></span>
* <span data-ttu-id="d6fa2-1197">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d6fa2-1198">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-1199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1199">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-1200">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d6fa2-1201">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d6fa2-1202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1202">Az.DataLakeStore</span></span>
* <span data-ttu-id="d6fa2-1203">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d6fa2-1204">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d6fa2-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d6fa2-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d6fa2-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-1208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1208">Az.Network</span></span>
* <span data-ttu-id="d6fa2-1209">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d6fa2-1210">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-1211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1211">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-1212">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d6fa2-1213">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d6fa2-1214">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d6fa2-1215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1215">Azure.Storage</span></span>
* <span data-ttu-id="d6fa2-1216">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d6fa2-1217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d6fa2-1218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d6fa2-1219">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d6fa2-1220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1220">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="d6fa2-1221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1221">Az.CognitiveServices</span></span>
* <span data-ttu-id="d6fa2-1222">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d6fa2-1223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1223">Az.Compute</span></span>
* <span data-ttu-id="d6fa2-1224">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d6fa2-1225">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d6fa2-1226">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d6fa2-1227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d6fa2-1228">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d6fa2-1229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1229">Az.Network</span></span>
* <span data-ttu-id="d6fa2-1230">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d6fa2-1231">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1231">new cmdlets added</span></span>
    - <span data-ttu-id="d6fa2-1232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d6fa2-1233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d6fa2-1234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d6fa2-1235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d6fa2-1236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d6fa2-1237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d6fa2-1238">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d6fa2-1239">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d6fa2-1240">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d6fa2-1241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1241">Az.RedisCache</span></span>
* <span data-ttu-id="d6fa2-1242">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d6fa2-1243">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d6fa2-1244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1244">Az.Resources</span></span>
* <span data-ttu-id="d6fa2-1245">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d6fa2-1246">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d6fa2-1247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1247">Az.Sql</span></span>
* <span data-ttu-id="d6fa2-1248">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d6fa2-1249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1249">Az.Websites</span></span>
* <span data-ttu-id="d6fa2-1250">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d6fa2-1251">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d6fa2-1252">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d6fa2-1253">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="d6fa2-1253">Initial Release</span></span>