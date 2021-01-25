---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 8cf52259008b2551b780d4cf6f09b4876673723c
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573451"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="5c3ac-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c3ac-103">Azure PowerShell release notes</span></span>

## <a name="540---january-2021"></a><span data-ttu-id="5c3ac-104">5.4.0 – janeiro de 2021</span><span class="sxs-lookup"><span data-stu-id="5c3ac-104">5.4.0 - January 2021</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-105">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-106">ID de solicitação do cliente correta mostrada na mensagem de depuração [nº 13745]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-106">Shown correct client request id on debug message [#13745]</span></span>
* <span data-ttu-id="5c3ac-107">Tipo de exceção comum do Azure PowerShell adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-107">Added common Azure PowerShell exception type</span></span>
* <span data-ttu-id="5c3ac-108">API 2019-06-01 de armazenamento com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3ac-108">Supported storage API 2019-06-01</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-109">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-109">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-110">O problema em que a descrição não era populada para agendamentos de gerenciamento de atualizações foi corrigido</span><span class="sxs-lookup"><span data-stu-id="5c3ac-110">Fixed issue where description was not populated for update management schedules</span></span>

#### <a name="azcosmosdb"></a><span data-ttu-id="5c3ac-111">Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5c3ac-111">Az.CosmosDB</span></span>
* <span data-ttu-id="5c3ac-112">Disponibilidade geral do módulo 'Az.CosmosDB'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-112">General availability of 'Az.CosmosDB' module</span></span>
* <span data-ttu-id="5c3ac-113">Restrição do cmdlet New-AzCosmosDBAccount para fazer chamadas de atualização para Contas de Banco de Dados existentes.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-113">Restricting New-AzCosmosDBAccount cmdlet to make update calls to existing Database Accounts.</span></span>
* <span data-ttu-id="5c3ac-114">Introdução do AnalyticalStorageTTL em SqlContainer.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-114">Introducing AnalyticalStorageTTL in SqlContainer.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-115">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-115">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-116">Regressão relativa à geração de token SAS corrigida</span><span class="sxs-lookup"><span data-stu-id="5c3ac-116">Fixed a regression regarding SAS token generation</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-117">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-117">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-118">Problema no módulo Gerenciamento de Segredos corrigido</span><span class="sxs-lookup"><span data-stu-id="5c3ac-118">Fixed an issue in Secret Management module</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c3ac-119">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-119">Az.LogicApp</span></span>
* <span data-ttu-id="5c3ac-120">Problema em que 'Get-AzLogicAppTriggerHistory' e 'Get-AzLogicAppRunAction' só recuperavam a primeira página de resultados corrigido [Nº 9141]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-120">Fixed issue that 'Get-AzLogicAppTriggerHistory' and 'Get-AzLogicAppRunAction' only retrieving the first page of results [#9141]</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-121">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-121">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-122">Cmdlets adicionados para regras de coleta de dados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-122">Added cmdlets for data collection rules:</span></span> 
    - <span data-ttu-id="5c3ac-123">'Get-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-123">'Get-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="5c3ac-124">'New-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-124">'New-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="5c3ac-125">'Set-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-125">'Set-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="5c3ac-126">'Update-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-126">'Update-AzDataCollectionRule'</span></span>
    - <span data-ttu-id="5c3ac-127">'Remove-AzDataCollectionRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-127">'Remove-AzDataCollectionRule'</span></span>
* <span data-ttu-id="5c3ac-128">Cmdlets adicionados para associações de regras de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-128">Added cmdlets for data collection rules associations</span></span>
    - <span data-ttu-id="5c3ac-129">'Get-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-129">'Get-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="5c3ac-130">'New-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-130">'New-AzDataCollectionRuleAssociation'</span></span>
    - <span data-ttu-id="5c3ac-131">'Remove-AzDataCollectionRuleAssociation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-131">'Remove-AzDataCollectionRuleAssociation'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-132">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-132">Az.Network</span></span>
* <span data-ttu-id="5c3ac-133">Novos cmdlets adicionados para CRUD de VpnGatewayNATRule.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-133">Added new cmdlets for CRUD of VpnGatewayNATRule.</span></span>
    - <span data-ttu-id="5c3ac-134">'New-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-134">'New-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="5c3ac-135">'Update-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-135">'Update-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="5c3ac-136">'Get-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-136">'Get-AzAzVpnGatewayNatRule'</span></span>
    - <span data-ttu-id="5c3ac-137">'Remove-AzAzVpnGatewayNatRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-137">'Remove-AzAzVpnGatewayNatRule'</span></span>    
* <span data-ttu-id="5c3ac-138">Cmdlets atualizados para definir NATRule no recurso VpnGateway e associá-lo ao recurso VpnSiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-138">Updated cmdlets to set NATRule on VpnGateway resource and associate it with VpnSiteLinkConnection resource.</span></span>
    - <span data-ttu-id="5c3ac-139">'New-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-139">'New-AzVpnGateway'</span></span>
    - <span data-ttu-id="5c3ac-140">'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-140">'Update-AzVpnGateway'</span></span> 
    - <span data-ttu-id="5c3ac-141">'New-AzVpnSiteLinkConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-141">'New-AzVpnSiteLinkConnection'</span></span>
* <span data-ttu-id="5c3ac-142">Cmdlets atualizados para habilitar a configuração de ConnectionMode em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-142">Updated cmdlets to enable setting of ConnectionMode on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="5c3ac-143">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-143">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="5c3ac-144">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-144">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="5c3ac-145">Cmdlet 'New-AzFirewallPolicyApplicationRule' atualizado:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-145">Updated 'New-AzFirewallPolicyApplicationRule' cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-146">Parâmetro TargetUrl adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-146">Added parameter TargetUrl</span></span>
    - <span data-ttu-id="5c3ac-147">Parâmetro TerminateTLS adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-147">Added parameter TerminateTLS</span></span>
* <span data-ttu-id="5c3ac-148">Novos cmdlets adicionados para recursos Premium do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-148">Added new cmdlets for Azure Firewall Premium Features</span></span>
    - <span data-ttu-id="5c3ac-149">'New-AzFirewallPolicyIntrusionDetection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-149">'New-AzFirewallPolicyIntrusionDetection'</span></span>
    - <span data-ttu-id="5c3ac-150">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-150">'New-AzFirewallPolicyIntrusionDetectionBypassTraffic'</span></span>
    - <span data-ttu-id="5c3ac-151">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-151">'New-AzFirewallPolicyIntrusionDetectionSignatureOverride'</span></span>
* <span data-ttu-id="5c3ac-152">Cmdlet New-AzFirewallPolicy atualizado:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-152">Updated New-AzFirewallPolicy cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-153">Parâmetro -SkuTier adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-153">Added parameter -SkuTier</span></span>
    - <span data-ttu-id="5c3ac-154">Parâmetro -Identity adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-154">Added parameter -Identity</span></span>
    - <span data-ttu-id="5c3ac-155">Parâmetro -UserAssignedIdentityId adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-155">Added parameter -UserAssignedIdentityId</span></span>
    - <span data-ttu-id="5c3ac-156">Parâmetro -IntrusionDetection adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-156">Added parameter -IntrusionDetection</span></span>
    - <span data-ttu-id="5c3ac-157">Parâmetro -TransportSecurityName adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-157">Added parameter -TransportSecurityName</span></span>
    - <span data-ttu-id="5c3ac-158">Parâmetro -TransportSecurityKeyVaultSecretId adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-158">Added parameter -TransportSecurityKeyVaultSecretId</span></span>
* <span data-ttu-id="5c3ac-159">Novo cmdlet para buscar Associações de Segurança IKE para Conexões de Gateway de Rede Virtual adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-159">Added new cmdlet to fetch IKE Security Associations for Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="5c3ac-160">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-160">'Get-AzVirtualNetworkGatewayConnectionIkeSa'</span></span>
* <span data-ttu-id="5c3ac-161">Suporte a várias autenticações para p2sVpnGateway adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-161">Added multiple Authentication support for p2sVpnGateway</span></span>
    - <span data-ttu-id="5c3ac-162">New-AzVpnServerConfiguration e Update-AzVpnServerConfiguration adicionados para permitir que vários parâmetros de autenticação sejam definidos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-162">Updated New-AzVpnServerConfiguration and Update-AzVpnServerConfiguration to allow multiple authentication parameters to be set.</span></span>
* <span data-ttu-id="5c3ac-163">Cmdlet 'New-AzVpnGateway' e 'New-AzP2sVpnGateway' atualizado:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-163">Updated 'New-AzVpnGateway' and 'New-AzP2sVpnGateway' cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-164">Parâmetro EnableRoutingPreferenceInternetFlag adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-164">Added parameter EnableRoutingPreferenceInternetFlag</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-165">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-165">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-166">Recurso Restauração entre Regiões adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-166">Added Cross Region Restore feature.</span></span>  
* <span data-ttu-id="5c3ac-167">Obtenção de configuração de carga de trabalho bloqueada quando o item de destino é um grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-167">Blocked getting workload config when target item is an availability group.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-168">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-168">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-169">Suporte adicionado para o parâmetro -QueryString em cmdlets New-AZ\*Deployments</span><span class="sxs-lookup"><span data-stu-id="5c3ac-169">Added support for -QueryString parameter in New-Az\*Deployments cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-170">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-171">Cmdlet 'Start-AzSqlInstanceDatabaseLogReplay' tornado síncrono, sinalizador -AsJob adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-171">Made 'Start-AzSqlInstanceDatabaseLogReplay' cmdlet synchronous, added -AsJob flag</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-172">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-173">ContinuationToken corrigido para nunca nulo na listagem de blobs com -IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="5c3ac-173">Fix ContinuationToken never null when list blob with -IncludeVersion</span></span>
    - <span data-ttu-id="5c3ac-174">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-174">'Get-AzStorageBlob'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-175">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-176">Suporte adicionado para certificados Gerenciados do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-176">Added support for App Service Managed certificates</span></span>
    - <span data-ttu-id="5c3ac-177">'New-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-177">'New-AzWebAppCertificate'</span></span>
    - <span data-ttu-id="5c3ac-178">'Remove-AzWebAppCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-178">'Remove-AzWebAppCertificate'</span></span>
* <span data-ttu-id="5c3ac-179">Problema que fazia com que a Senha do Docker fosse removida de appSettings em 'Set-AzWebApp' e 'Set-AzWebAppSlot' corrigido</span><span class="sxs-lookup"><span data-stu-id="5c3ac-179">Fixed issue that causes Docker Password to be removed from appsettings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="5c3ac-180">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-180">Thanks to our community contributors</span></span>
* <span data-ttu-id="5c3ac-181">Ivan Akcheurov (@ivanakcheurov), por atualizar Set-AzSecurityWorkspaceSetting.md (Nº 13877)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-181">Ivan Akcheurov (@ivanakcheurov), Update Set-AzSecurityWorkspaceSetting.md (#13877)</span></span>
* <span data-ttu-id="5c3ac-182">@javiermarasco, atualização de exemplo (Nº 13837)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-182">@javiermarasco, Update example (#13837)</span></span>
* <span data-ttu-id="5c3ac-183">@jhaprakash26, Atualização de Set-AzVirtualNetwork.md (Nº 13857)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-183">@jhaprakash26, Update Set-AzVirtualNetwork.md (#13857)</span></span>
* <span data-ttu-id="5c3ac-184">Michael Holmes (@MichaelHolmesWP), por atualizar New-AzStorageTableStoredAccessPolicy.md (#13871)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-184">Michael Holmes (@MichaelHolmesWP), Update New-AzStorageTableStoredAccessPolicy.md (#13871)</span></span>
* <span data-ttu-id="5c3ac-185">Michael James (@mikejwhat), por permitir que Get-AzLogicAppTriggerHistory e Get-AzLogicAppRunAction retornem mais de 30 resultados (Nº 13846)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-185">Michael James (@mikejwhat), Allow Get-AzLogicAppTriggerHistory and Get-AzLogicAppRunAction to return more than 30 results (#13846)</span></span>
* <span data-ttu-id="5c3ac-186">@Willem-J-an, correção de bug que fazia a senha do Docker ser removida de appsettings em Set-AzWebApp(Slot) (Nº 13866)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-186">@Willem-J-an, Fix bug causing Docker Password to be removed from appsettings in Set-AzWebApp(Slot) (#13866)</span></span>

## <a name="530---december-2020"></a><span data-ttu-id="5c3ac-187">5.3.0 – Dezembro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-187">5.3.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-188">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-189">Foi corrigido o problema em que o proxy http não é respeitado no Windows PowerShell [n. 13647]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-189">Fixed the issue that Http proxy is not respected in Windows PowerShell [#13647]</span></span>
* <span data-ttu-id="5c3ac-190">Foi aprimorado o log de depuração de operações de execução prolongada em módulos gerados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-190">Improved debug log of long running operations in generated modules</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-191">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-191">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-192">Foi corrigido o problema em que os parâmetros de 'Start-AzAutomationRunbook' não podem converter a cadeia de caracteres encapsulada de PSObject em cadeia de caracteres JSON [#13240]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-192">Fixed issue that parameters of 'Start-AzAutomationRunbook' cannot convert PSObject wrapped string to JSON string [#13240]</span></span>
* <span data-ttu-id="5c3ac-193">Foi corrigido o preenchedor de localização para o cmdlet New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="5c3ac-193">Fixed location completer for New-AzAutomationUpdateManagementAzureQuery cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-194">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-194">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-195">Novo parâmetro 'VM' no novo conjunto de parâmetros 'VMParameterSet' adicionado aos cmdlets 'Get-AzVMDscExtensionStatus' e 'Get-AzVMDscExtension'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-195">New parameter 'VM' in new parameter set 'VMParameterSet' added to 'Get-AzVMDscExtensionStatus' and 'Get-AzVMDscExtension' cmdlets.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="5c3ac-196">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-196">Az.Databricks</span></span>
* <span data-ttu-id="5c3ac-197">Foi corrigido um problema que fazia com que 'New-AzDatabricksVNetPeering' fosse retornado antes de ser totalmente provisionado (https://github.com/Azure/autorest.powershell/issues/610) )</span><span class="sxs-lookup"><span data-stu-id="5c3ac-197">Fixed an issue that may cause 'New-AzDatabricksVNetPeering' to return before it is fully provisioned (https://github.com/Azure/autorest.powershell/issues/610)</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-198">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-198">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-199">Foi corrigido o problema do comando ' Invoke-AzDataFactoryV2Pipeline' para SupportsShouldProcess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-199">Fixed the command 'Invoke-AzDataFactoryV2Pipeline' for SupportsShouldProcess issue</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="5c3ac-200">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="5c3ac-200">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="5c3ac-201">Foi adicionada a propriedade StartVMOnConnect ao pool de host.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-201">Added StartVMOnConnect property to hostpool.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-202">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-203">Propriedades adicionadas: FQDN e EffectiveDiskEncryptionKeyUrl na classe AzureHDInsightHostInfo.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-203">Added properties: Fqdn and EffectiveDiskEncryptionKeyUrl in the class AzureHDInsightHostInfo.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-204">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-204">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-205">Foi adicionado um novo parâmetro '-AsPlainText' a 'Get-AzKeyVaultSecret' para retornar diretamente o segredo em texto sem formatação [n. 13630]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-205">Added a new parameter '-AsPlainText' to 'Get-AzKeyVaultSecret' to directly return the secret in plain text [#13630]</span></span>
* <span data-ttu-id="5c3ac-206">Foi adicionado suporte à restauração seletiva de uma chave de um backup completo de HSM gerenciado [n. 13526]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-206">Supported selective restore a key from a managed HSM full backup [#13526]</span></span>
* <span data-ttu-id="5c3ac-207">Foram corrigidos alguns problemas secundários [n. 13583] [n. 13584]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-207">Fixed some minor issues [#13583] [#13584]</span></span>
* <span data-ttu-id="5c3ac-208">Foram adicionados objetos de retorno ausentes de 'Get-Secret' no módulo SecretManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-208">Added missing return objects of 'Get-Secret' in SecretManagement module</span></span>
* <span data-ttu-id="5c3ac-209">Foi corrigido um problema que pode fazer com que o cofre seja criado sem a política de acesso padrão [n. 13687]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-209">Fixed an issue that may cause vault to be created without default access policy [#13687]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="5c3ac-210">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="5c3ac-210">Az.Kusto</span></span>
* <span data-ttu-id="5c3ac-211">Versão da API atualizada para a versão de 18/09/2020.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-211">Updated API version to 2020-09-18.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-212">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-212">Az.Network</span></span>
* <span data-ttu-id="5c3ac-213">Foi corrigido problema no cmdlet de remoção e emparelhamento e conexão para o cenário ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-213">Fixed issue in remove peering and connection cmdlet for ExpressRouteCircuit scenario</span></span>
    - <span data-ttu-id="5c3ac-214">'Remove-AzExpressRouteCircuitPeeringConfig' e 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-214">'Remove-AzExpressRouteCircuitPeeringConfig' and 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-215">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-215">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-216">Foi adicionado suporte para retorno de resultados paginados para Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="5c3ac-216">Added support for returning paginated results for Get-AzPolicyState</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-217">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-217">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-218">Foi habilitado o recurso de exclusão temporária para SQL.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-218">Enabled softdelete feature for SQL.</span></span>
* <span data-ttu-id="5c3ac-219">Foi corrigida a restauração do SQL AG e removida a verificação do nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-219">Fixed SQL AG restore and removed the container name check.</span></span>
* <span data-ttu-id="5c3ac-220">Foi alterado o formato de nome de contêiner para o item de backup de Arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-220">Changed container name format for Azure Files backup item.</span></span>
* <span data-ttu-id="5c3ac-221">Foi adicionado suporte de recurso CMK para ações do cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-221">Added CMK feature support for Recovery services vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-222">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-223">Foi corrigido um problema de exceção de NullRef em 'New-AzureManagedApplication' e 'Set-AzureManagedApplication'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-223">Fixed a NullRef exception issue in 'New-AzureManagedApplication' and 'Set-AzureManagedApplication'.</span></span>
* <span data-ttu-id="5c3ac-224">Foi atualizado o SDK do Azure Resource Manager para uso da versão mais recente em GA da API do DeploymentScripts: 01/10/2020.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-224">Updated Azure Resource Manager SDK to use latest DeploymentScripts GA api-version: 2020-10-01.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-225">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-225">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-226">Correção do 'Add-AzServiceFabricNodeType'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-226">Fixed 'Add-AzServiceFabricNodeType'.</span></span> <span data-ttu-id="5c3ac-227">Foi adicionado um tipo de nó ao cluster do Service Fabric antes da criação de um conjunto de dimensionamento de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-227">Added node type to service fabric cluster before creating virtual machine scale set.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-228">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-229">Foi corrigida a descrição do parâmetro fixo para o comando 'InstanceFailoverGroup'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-229">Fixed parameter description for 'InstanceFailoverGroup' command.</span></span>
* <span data-ttu-id="5c3ac-230">Foi atualizada a lógica em que schemaName, tableName e columnName estão sendo extraídos da ID dos comandos da Classificação de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-230">Updated the logic in which schemaName, tableName and columnName are being extracted from the id of SQL Data Classification commands.</span></span>
* <span data-ttu-id="5c3ac-231">Foram corrigidos os campos Status e StatusMessage em 'Get-AzSqlDatabaseImportExportStatus' para estar em conformidade com a documentação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-231">Fixed Status and StatusMessage fields in 'Get-AzSqlDatabaseImportExportStatus' to conform to documentation</span></span>
* <span data-ttu-id="5c3ac-232">Foram adicionados cmdlets de auditoria do DevOps (operações de suporte da Microsoft): Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-232">Added Microsoft support operations (DevOps) auditing cmdlets: Get-AzSqlServerMSSupportAudit, Set-AzSqlServerMSSupportAudit, Remove-AzSqlServerMSSupportAudit</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-233">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-233">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-234">Foi adicionado suporte à criação/atualização/obtenção/listagem de EncryptionScope de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-234">Supported create/update/get/list EncryptionScope of a Storage account</span></span>
    - <span data-ttu-id="5c3ac-235">'New-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-235">'New-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="5c3ac-236">'Update-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-236">'Update-AzStorageEncryptionScope'</span></span>
    - <span data-ttu-id="5c3ac-237">'Get-AzStorageEncryptionScope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-237">'Get-AzStorageEncryptionScope'</span></span>
* <span data-ttu-id="5c3ac-238">Foi adicionado suporte para a criação de contêineres e o upload de blobs com a configuração Escopo de Criptografia</span><span class="sxs-lookup"><span data-stu-id="5c3ac-238">Supported create container and upload blob with Encryption Scope setting</span></span>
    - <span data-ttu-id="5c3ac-239">'New-AzRmStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-239">'New-AzRmStorageContainer'</span></span>
    - <span data-ttu-id="5c3ac-240">'New-AzStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-240">'New-AzStorageContainer'</span></span>
    - <span data-ttu-id="5c3ac-241">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-241">'Set-AzStorageBlobContent'</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="5c3ac-242">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-242">Thanks to our community contributors</span></span>
* <span data-ttu-id="5c3ac-243">Andreas Wolter (@AndreasWolter), idioma de marketing removido, melhor filtro de exemplo (n. 13671)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-243">Andreas Wolter (@AndreasWolter), removed marketing language, better example filter (#13671)</span></span>
* <span data-ttu-id="5c3ac-244">Tidjani Belmansour (@BelRarr), Get-AzBillingInvoice.md atualizado (n. 13634)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-244">Tidjani Belmansour (@BelRarr), Update Get-AzBillingInvoice.md (#13634)</span></span>
* <span data-ttu-id="5c3ac-245">David Klempfner (@DavidKlempfner)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-245">David Klempfner (@DavidKlempfner)</span></span>
  * <span data-ttu-id="5c3ac-246">Foi corrigido um erro de ortografia (n. 13677)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-246">Fixed spelling mistake (#13677)</span></span>
  * <span data-ttu-id="5c3ac-247">Atualização do PSMetricNoDetails.cs (#13676)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-247">Update PSMetricNoDetails.cs (#13676)</span></span>
* <span data-ttu-id="5c3ac-248">@kilobyte97, correção de bug para a exclusão da configuração pelo cmdlet remove (n. 13655)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-248">@kilobyte97, bugfix for remove cmdlet to delete config (#13655)</span></span>
* <span data-ttu-id="5c3ac-249">@kongou-ae, atualização do Set-AzFirewall.md (n. 13727)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-249">@kongou-ae, Update Set-AzFirewall.md (#13727)</span></span>
* <span data-ttu-id="5c3ac-250">@MasterKuat, correção da troca entre título e código na documentação (n. 13666)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-250">@MasterKuat, Fix swap between title and code in documentation (#13666)</span></span>
* <span data-ttu-id="5c3ac-251">NickT (@nukeulis), atualização do Set-AzContext.md (n. 13702)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-251">NickT (@nukeulis), Update Set-AzContext.md (#13702)</span></span>
* <span data-ttu-id="5c3ac-252">@PaulHCode, atualização do Start-AzJitNetworkAccessPolicy.md – correção do exemplo para exibir o cmdlet adequado que está sendo demonstrado (n. 13713)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-252">@PaulHCode, Update Start-AzJitNetworkAccessPolicy.md - Fix the Example to display the proper cmdlet being demonstrated (#13713)</span></span>
* <span data-ttu-id="5c3ac-253">Ryan Borstelmann (@ryanborMSFT), ID da assinatura removida (n. 13715)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-253">Ryan Borstelmann (@ryanborMSFT), Removed Subscription ID (#13715)</span></span>
* <span data-ttu-id="5c3ac-254">Shashikant Shakya (@shshakya), atualização do Set-AzSqlDatabase.md (n. 13674)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-254">Shashikant Shakya (@shshakya), Update Set-AzSqlDatabase.md (#13674)</span></span>
* <span data-ttu-id="5c3ac-255">Sebastian Olsen (@Spacebjorn), atualização do Get-AzRecoveryServicesBackupItem.md (n. 13719)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-255">Sebastian Olsen (@Spacebjorn), Update Get-AzRecoveryServicesBackupItem.md (#13719)</span></span>

## <a name="520---december-2020"></a><span data-ttu-id="5c3ac-256">5.2.0 – Dezembro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-256">5.2.0 - December 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-257">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-257">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-258">Gerenciado para analisar o tempo de ExpiresOn do token bruto se não for possível obter da biblioteca subjacente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-258">Managed to parse ExpiresOn time from raw token if could not get from underlying library</span></span>
* <span data-ttu-id="5c3ac-259">Mensagem de aviso aprimorada se a autenticação interativa não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="5c3ac-259">Improved warning message if Interactive authentication is unavailable</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-260">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-260">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-261">[Alteração da falha] 'New-AzApiManagementProduct', por padrão, não tem limite de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-261">[Breaking change] 'New-AzApiManagementProduct' by default has no subscription limit.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-262">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-263">Get-AzVm editado para filtrar por '-Name' antes de verificar a limitação devido a muitos recursos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-263">Edited Get-AzVm to filter by '-Name' prior to checking for throttling due to too many resources.</span></span> 
* <span data-ttu-id="5c3ac-264">Novo cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-264">New cmdlet 'Start-AzVmssRollingExtensionUpgrade'.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5c3ac-265">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c3ac-265">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5c3ac-266">Parâmetro 'Name' com suporte e valor da entrada de pipeline para 'Get-AzContainerRegistryUsage' [nº 13605]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-266">Supported parameter 'Name' for and value from pipeline input for 'Get-AzContainerRegistryUsage' [#13605]</span></span>
* <span data-ttu-id="5c3ac-267">Exceções refinadas para 'Connect-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-267">Polished exceptions for 'Connect-AzContainerRegistry'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-268">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-268">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-269">SDK do .NET do ADF atualizado para a versão 4.13.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-269">Updated ADF .Net SDK version to 4.13.0</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5c3ac-270">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5c3ac-270">Az.HealthcareApis</span></span>
* <span data-ttu-id="5c3ac-271">Suporte adicionado para chaves gerenciadas pelo cliente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-271">Added support for customer managed keys</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-272">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-272">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-273">Problema de token SAS corrigido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-273">Fixed an issue of SAS token.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-274">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-274">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-275">'Todos' com suporte como uma opção quando são definidas políticas de acesso do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="5c3ac-275">Supported 'all' as an option when setting key vault access policies</span></span>
* <span data-ttu-id="5c3ac-276">Nova versão com suporte do módulo do SecretManagement [nº 13366]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-276">Supported new version of SecretManagement module [#13366]</span></span>
* <span data-ttu-id="5c3ac-277">ByteArray, String, PSCredential e Hashtable com suporte para 'SecretValue' em SecretManagementModule [nº 12190]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-277">Supported ByteArray, String, PSCredential and Hashtable for 'SecretValue' in SecretManagementModule [#12190]</span></span>
* <span data-ttu-id="5c3ac-278">[Alteração da falha] Superfície de API de cmdlets recriada com relação ao HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-278">[Breaking change] redesigned the API surface of cmdlets related to managed HSM.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-279">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-279">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-280">Parâmetro 'Rule' de 'New-AzAutoscaleProfile' alterado para aceitar lista vazia.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-280">Changed parameter 'Rule' of 'New-AzAutoscaleProfile' to accept empty list.</span></span> <span data-ttu-id="5c3ac-281">[Nº 12903]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-281">[#12903]</span></span>
* <span data-ttu-id="5c3ac-282">Adição de novos cmdlets para dar suporte à criação de configurações de diagnóstico mais flexíveis:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-282">Added new cmdlets to support creating diagnostic settings more flexible:</span></span>
    * <span data-ttu-id="5c3ac-283">'Get-AzDiagnosticSettingCategory'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-283">'Get-AzDiagnosticSettingCategory'</span></span>
    * <span data-ttu-id="5c3ac-284">'New-AzDiagnosticSetting'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-284">'New-AzDiagnosticSetting'</span></span>
    * <span data-ttu-id="5c3ac-285">'New-AzDiagnosticDetailSetting'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-285">'New-AzDiagnosticDetailSetting'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-287">O texto de ajuda e o nome do conjunto de parâmetros foram alterados para o cmdlet 'Restore-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-287">Made help text and parameter set name changes to 'Restore-AzRecoveryServicesBackupItem' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-288">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-289">Suporte ao parâmetro '-Tag' adicionado para 'Set-AzTemplateSpec' e 'New-AzTemplateSpec'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-289">Added '-Tag' parameter support to 'Set-AzTemplateSpec' and 'New-AzTemplateSpec'</span></span>
* <span data-ttu-id="5c3ac-290">Suporte à exibição de marcas adicionado para o formatador padrão para Especificações de Modelo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-290">Added Tag display support to default formatter for Template Specs</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-291">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-291">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-292">Exemplo adicionado para 'Set-AzServiceFabricSetting' com o parâmetro SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="5c3ac-292">Added example to 'Set-AzServiceFabricSetting' with SettingsSectionDescription param</span></span>
* <span data-ttu-id="5c3ac-293">Cmdlets relacionados a aplicativos atualizados para alertar que o suporte é apenas para recursos implantados do ARM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-293">Updated application related cmdlets to call out that support is only for ARM deployed resources</span></span>
* <span data-ttu-id="5c3ac-294">Cmdlets de certificado de cluster de 'Add-AzureRmServiceFabricClusterCertificate' e 'Remove-AzureRmServiceFabricClusterCertificate' marcados para substituição</span><span class="sxs-lookup"><span data-stu-id="5c3ac-294">Marked for deprecation cluster cert cmdlets 'Add-AzureRmServiceFabricClusterCertificate' and 'Remove-AzureRmServiceFabricClusterCertificate'</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-295">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-296">SecondaryType adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-296">Added SecondaryType to the following:</span></span> 
    - <span data-ttu-id="5c3ac-297">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-297">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="5c3ac-298">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-298">'Set-AzSqlDatabase'</span></span>
    - <span data-ttu-id="5c3ac-299">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-299">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="5c3ac-300">HighAvailabilityReplicaCount adicionado ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-300">Added HighAvailabilityReplicaCount to the following:</span></span> 
    - <span data-ttu-id="5c3ac-301">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-301">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="5c3ac-302">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-302">'Set-AzSqlDatabase'</span></span>
* <span data-ttu-id="5c3ac-303">ReadReplicaCount tornado um alias de HighAvailabilityReplicaCount no seguinte:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-303">Made ReadReplicaCount an alias of HighAvailabilityReplicaCount in the following:</span></span> 
    - <span data-ttu-id="5c3ac-304">'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-304">'New-AzSqlDatabase'</span></span>
    - <span data-ttu-id="5c3ac-305">'Set-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-305">'Set-AzSqlDatabase'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-306">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-306">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-307">Upload de arquivos do Azure de até 4 TiB com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3ac-307">Supported upload Azure File size up to 4 TiB</span></span>
    - <span data-ttu-id="5c3ac-308">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-308">'Set-AzStorageFileContent'</span></span>
* <span data-ttu-id="5c3ac-309">Azure.Storage.Blobs atualizado para 12.7.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-309">Upgraded Azure.Storage.Blobs to 12.7.0</span></span>
* <span data-ttu-id="5c3ac-310">Azure.Storage.Files.Shares atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-310">Upgraded Azure.Storage.Files.Shares to 12.5.0</span></span>
* <span data-ttu-id="5c3ac-311">Azure.Storage.Files.DataLake atualizado para 12.5.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-311">Upgraded Azure.Storage.Files.DataLake to 12.5.0</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c3ac-312">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c3ac-312">Az.StorageSync</span></span>
* <span data-ttu-id="5c3ac-313">Recurso de política de camadas de sincronização adicionado com política de download e modo de cache local</span><span class="sxs-lookup"><span data-stu-id="5c3ac-313">Added Sync tiering policy feature with download policy and local cache mode</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-314">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-314">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-315">Impedir regras de restrição de acesso duplicadas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-315">Prevent duplicate access restriction rules</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="5c3ac-316">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-316">Thanks to our community contributors</span></span>
* <span data-ttu-id="5c3ac-317">Andrew Dawson (@dawsonar802), por atualizar Get-AzKeyVaultCertificate.md – obter certificado e salvá-lo como seção pfx para trabalhar com o PowerShell Core (nº 13557)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-317">Andrew Dawson (@dawsonar802), Update Get-AzKeyVaultCertificate.md - Get cert and save it as pfx section to work with PowerShell Core (#13557)</span></span>
* <span data-ttu-id="5c3ac-318">@iviark, por atualizações de APIs de saúde BYOK do Powershell (nº 13518)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-318">@iviark, Healthcare APIs Powershell BYOK Updates (#13518)</span></span>
* <span data-ttu-id="5c3ac-319">John Duckmanton (@johnduckmanton), por corrigir a ortografia de TagPatchOperation (nº 13508)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-319">John Duckmanton (@johnduckmanton), Correct spelling of TagPatchOperation (#13508)</span></span>
* <span data-ttu-id="5c3ac-320">Michael James (@mikejwhat)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-320">Michael James (@mikejwhat)</span></span>
  * <span data-ttu-id="5c3ac-321">Ajuda organizada do Get-AzLogicAppRunHistory (nº 13513)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-321">Get-AzLogicAppRunHistory Help Tidy (#13513)</span></span>
* <span data-ttu-id="5c3ac-322">Richard de Zwart (@mountain65)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-322">Richard de Zwart (@mountain65)</span></span>
  * <span data-ttu-id="5c3ac-323">Atualizar Update-AzAppConfigurationStore.md (nº 13485)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-323">Update Update-AzAppConfigurationStore.md (#13485)</span></span>
  * <span data-ttu-id="5c3ac-324">Atualizar New-AzCosmosDBAccount.md (nº 13490)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-324">Update New-AzCosmosDBAccount.md (#13490)</span></span>
* <span data-ttu-id="5c3ac-325">@SteppingRazor, New-AzApiManagementProduct: alterar o valor padrão do parâmetro SubscriptionsLimit para nenhum (nº 13457)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-325">@SteppingRazor, New-AzApiManagementProduct: Change SubscriptionsLimit parameter default value to None (#13457)</span></span>
* <span data-ttu-id="5c3ac-326">Steve Burkett (@SteveBurkettNZ), por corrigir erros de digitação para o parâmetro WorkspaceResourceId no exemplo (nº 13589)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-326">Steve Burkett (@SteveBurkettNZ), Fix Typo for WorkspaceResourceId parameter in example (#13589)</span></span>

## <a name="510---november-2020"></a><span data-ttu-id="5c3ac-327">5.1.0 – Novembro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-327">5.1.0 - November 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-328">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-328">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-329">Correção de um problema em que a TenantId podia não ser respeitada se 'Connect-AzAccount -DeviceCode' [nº 13477] fosse usado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-329">Fixed an issue that TenantId may be not respected if using 'Connect-AzAccount -DeviceCode'[#13477]</span></span>
* <span data-ttu-id="5c3ac-330">Adição do novo cmdlet 'Get-AzAccessToken'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-330">Added new cmdlet 'Get-AzAccessToken'</span></span>
* <span data-ttu-id="5c3ac-331">Correção de um problema que ocorria quando o caminho do perfil do usuário estava inacessível</span><span class="sxs-lookup"><span data-stu-id="5c3ac-331">Fixed an issue that error happens if user profile path is inaccessible</span></span>
* <span data-ttu-id="5c3ac-332">Correção de um problema que causava o erro Write-Object durante Connect-AzAccount [nº 13419]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-332">Fixed an issue causing Write-Object error during Connect-AzAccount [#13419]</span></span>
* <span data-ttu-id="5c3ac-333">Adição do parâmetro 'ContainerRegistryEndpointSuffix' a: 'Add-AzEnvironment', 'Set-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-333">Added parameter 'ContainerRegistryEndpointSuffix' to: 'Add-AzEnvironment', 'Set-AzEnvironment'</span></span> 
* <span data-ttu-id="5c3ac-334">Suporte à interrupção de logon com o clique em <kbd>CTRL</kbd>+<kbd>C</kbd></span><span class="sxs-lookup"><span data-stu-id="5c3ac-334">Supported interrupting login by hitting <kbd>CTRL</kbd>+<kbd>C</kbd></span></span>
* <span data-ttu-id="5c3ac-335">Correção de um problema que fazia com que 'Connect-AzAccount -KeyVaultAccessToken' não funcionasse [nº 13127]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-335">Fixed an issue causing 'Connect-AzAccount -KeyVaultAccessToken' not working [#13127]</span></span>
* <span data-ttu-id="5c3ac-336">Correção da referência nula e da não diferenciação de maiúsculas e minúsculas no método em 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-336">Fixed null reference and method case insensitive in 'Invoke-AzRestMethod'</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-337">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-337">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-338">Correção do problema em que o usuário não podia usar a entidade de serviço para criar um cluster do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-338">Fixed the issue that user cannot use service principal to create a new Kubernetes cluster.</span></span> <span data-ttu-id="5c3ac-339">[nº 13012]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-339">[#13012]</span></span>

#### <a name="azappconfiguration"></a><span data-ttu-id="5c3ac-340">Az.AppConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-340">Az.AppConfiguration</span></span>
* <span data-ttu-id="5c3ac-341">Disponibilidade geral do módulo 'Az.AppConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-341">General availability of 'Az.AppConfiguration' module</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-342">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-342">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-343">Aprimoramento da mensagem de erro do comando 'New-AzDataFactoryV2LinkedServiceEncryptedCredential'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-343">Improved error message of 'New-AzDataFactoryV2LinkedServiceEncryptedCredential' command</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-344">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-345">Atualização do SDK do plano de dados do ADLS para 1.2.4-alpha.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-345">Updated ADLS dataplane SDK to 1.2.4-alpha.</span></span> <span data-ttu-id="5c3ac-346">Alterações: https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span><span class="sxs-lookup"><span data-stu-id="5c3ac-346">Changes:https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-124-alpha</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="5c3ac-347">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="5c3ac-347">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="5c3ac-348">Adição de novos cmdlets do Pacote MSIX e atualização de cmdlets de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-348">Added new MSIX Package cmdlets and updated Applications cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-349">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-349">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-350">Correção de comandos do cluster EventHub sem marcas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-350">Fixed Cluster commands for EventHub cluster without tags</span></span>
* <span data-ttu-id="5c3ac-351">Atualização do texto da Ajuda de PartnerNamespace dos comandos AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-351">Updated help text for PartnerNamespace of AzEventHubGeoDRConfiguration commands</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-352">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-353">Adição dos parâmetros 'ResourceProviderConnection' e 'PrivateLink' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de link privado e saída de retransmissão</span><span class="sxs-lookup"><span data-stu-id="5c3ac-353">Add parameters 'ResourceProviderConnection' and 'PrivateLink' to cmdlet 'New-AzHDInsightCluster' to support relay outbound and private link feature</span></span>
* <span data-ttu-id="5c3ac-354">Adição do parâmetro 'AmbariDatabase' ao cmdlet 'New-AzHDInsightCluster' para dar suporte ao recurso de banco de dados personalizado do Ambari</span><span class="sxs-lookup"><span data-stu-id="5c3ac-354">Add parameter 'AmbariDatabase' to cmdlet 'New-AzHDInsightCluster' to support custom Ambari database feature</span></span>
* <span data-ttu-id="5c3ac-355">Adição do valor de aceitação de 'AmbariDatabase' ao parâmetro 'MetastoreType' do cmdlet 'Add-AzHDInsightMetastore'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-355">Add accept value 'AmbariDatabase' to the parameter 'MetastoreType' of the cmdlet 'Add-AzHDInsightMetastore'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-356">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-356">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-357">Permissão de marcas no cmdlet create do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-357">Allowed tags in IoT Hub create cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-358">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-358">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-359">Suporte à atualização de marcas do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="5c3ac-359">Supported updating key vault tag</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c3ac-360">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-360">Az.LogicApp</span></span>
* <span data-ttu-id="5c3ac-361">Correção de Get-AzLogicAppRunHistory, que só recuperava a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-361">Fixed for Get-AzLogicAppRunHistory only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-362">Az.Network</span></span>
* <span data-ttu-id="5c3ac-363">Atualização do cmdlet indicado abaixo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-363">Updated below cmdlet</span></span> 
    - <span data-ttu-id="5c3ac-364">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-364">'New-AzLoadBalancerFrontendIpConfigCommand', 'Set-AzLoadBalancerFrontendIpConfigCommand', 'Add-AzLoadBalancerFrontendIpConfigCommand':</span></span>
        - <span data-ttu-id="5c3ac-365">Adição da propriedade PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5c3ac-365">Added PublicIpAddressPrefix property</span></span>
        - <span data-ttu-id="5c3ac-366">Adição da propriedade PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-366">Added PublicIpAddressPrefixId property</span></span>
* <span data-ttu-id="5c3ac-367">Adição de novas propriedades aos cmdlets a seguir para permitir o balanceamento de carga global</span><span class="sxs-lookup"><span data-stu-id="5c3ac-367">Added new properties to the following cmdlets to allow for global load balancing</span></span>
    - <span data-ttu-id="5c3ac-368">'New-AzLoadBalancer':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-368">'New-AzLoadBalancer':</span></span>
        - <span data-ttu-id="5c3ac-369">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="5c3ac-369">Added Sku Tier property</span></span>
    - <span data-ttu-id="5c3ac-370">'New-AzPuplicIpAddress':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-370">'New-AzPuplicIpAddress':</span></span>
        - <span data-ttu-id="5c3ac-371">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="5c3ac-371">Added Sku Tier property</span></span>
    - <span data-ttu-id="5c3ac-372">'New-AzPublicIpPrefix':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-372">'New-AzPublicIpPrefix':</span></span>
        - <span data-ttu-id="5c3ac-373">adição da propriedade de Nível de SKU</span><span class="sxs-lookup"><span data-stu-id="5c3ac-373">Added Sku Tier property</span></span>
    - <span data-ttu-id="5c3ac-374">'New-AzLoadBalancerBackendAddressConfig':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-374">'New-AzLoadBalancerBackendAddressConfig':</span></span>
        - <span data-ttu-id="5c3ac-375">Adição da propriedade LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-375">Added LoadBalancerFrontendIPConfigurationId property</span></span>
* <span data-ttu-id="5c3ac-376">Atualização do planejamento para preterir os avisos dos seguintes cmdlets: –'New-AzVirtualHubRoute'   –'New-AzVirtualHubRouteTable'   –'Add-AzVirtualHubRoute'   –'Add-AzVirtualHubRouteTable'   –'Get-AzVirtualHubRouteTable'   –'Remove-AzVirtualHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-376">Updated planning to deprecate warnings for the following cmdlets   -'New-AzVirtualHubRoute'   -'New-AzVirtualHubRouteTable'   -'Add-AzVirtualHubRoute'   -'Add-AzVirtualHubRouteTable'   -'Get-AzVirtualHubRouteTable'   -'Remove-AzVirtualHubRouteTable'</span></span>
* <span data-ttu-id="5c3ac-377">Adição do planejamento para preterir os avisos no argumento 'RouteTable' nos seguintes cmdlets: –'New-AzVirtualHub'   –'Set-AzVirtualHub'   –'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-377">Added planning to deprecate warnings on the argument 'RouteTable' for the following cmdlets   -'New-AzVirtualHub'   -'Set-AzVirtualHub'   -'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="5c3ac-378">Os argumentos '-MinScaleUnits' e '-MaxScaleUnits' passaram a ser opcionais em 'Set-AzExpressRouteGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-378">Made arguments '-MinScaleUnits' and '-MaxScaleUnits' optional in 'Set-AzExpressRouteGateway'</span></span>
* <span data-ttu-id="5c3ac-379">Adição de novos cmdlets para dar suporte à autenticação mútua e aos perfis SSL no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-379">Added new cmdlets to support Mutual Authentication and SSL Profiles on Application Gateway</span></span>
    - <span data-ttu-id="5c3ac-380">'Get-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-380">'Get-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-381">'New-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-381">'New-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-382">'Remove-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-382">'Remove-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-383">'Set-AzApplicationGatewayClientAuthConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-383">'Set-AzApplicationGatewayClientAuthConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-384">'Add-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-384">'Add-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="5c3ac-385">'Get-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-385">'Get-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="5c3ac-386">'New-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-386">'New-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="5c3ac-387">'Remove-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-387">'Remove-AzApplicationGatewayTrustedClientCertificate'</span></span> 
    - <span data-ttu-id="5c3ac-388">'Set-AzApplicationGatewayTrustedClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-388">'Set-AzApplicationGatewayTrustedClientCertificate'</span></span>
    - <span data-ttu-id="5c3ac-389">'Add-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-389">'Add-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="5c3ac-390">'Get-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-390">'Get-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="5c3ac-391">'New-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-391">'New-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="5c3ac-392">'Remove-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-392">'Remove-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="5c3ac-393">'Set-AzApplicationGatewaySslProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-393">'Set-AzApplicationGatewaySslProfile'</span></span>
    - <span data-ttu-id="5c3ac-394">'Get-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-394">'Get-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="5c3ac-395">'Remove-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-395">'Remove-AzApplicationGatewaySslProfilePolicy'</span></span>
    - <span data-ttu-id="5c3ac-396">'Set-AzApplicationGatewaySslProfilePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-396">'Set-AzApplicationGatewaySslProfilePolicy'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-397">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-397">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-398">A especificação do BackupTime da política está em UTC.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-398">Specifying policy BackupTime is in UTC.</span></span>
* <span data-ttu-id="5c3ac-399">Modificação do aviso de alteração da falha no cmdlet Get-AzRecoveryServicesBackupJobDetails.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-399">Modifying breaking change warning in Get-AzRecoveryServicesBackupJobDetails cmdlet.</span></span>
* <span data-ttu-id="5c3ac-400">Atualização do texto da Ajuda do script de exemplo para o cmdlet Set-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-400">Updating sample script help text for Set-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-401">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-401">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-402">Correção de um problema em que What-If mostrava dois escopos de grupo de recursos com usos diferentes de maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-402">Fixed an issue where What-If shows two resource group scopes with different casing</span></span>
* <span data-ttu-id="5c3ac-403">Atualização de 'Export-AzResourceGroup' para uso do SDK.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-403">Updated 'Export-AzResourceGroup' to use the SDK.</span></span>
* <span data-ttu-id="5c3ac-404">Adição de informações de cultura aos métodos de análise</span><span class="sxs-lookup"><span data-stu-id="5c3ac-404">Added culture info to parse methods</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-405">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-405">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-406">Correção de problemas em que Set-AzSqlDatabaseAudit não dava suporte ao banco de dados de Hiperescala e em que não era possível determinar a edição do banco de dados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-406">Fixed issues where Set-AzSqlDatabaseAudit were not support Hyperscale database and database edition cannot be determined</span></span>
* <span data-ttu-id="5c3ac-407">Adição de MaintenanceConfigurationId a 'New-AzSqlInstance' e 'Set-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-407">Added MaintenanceConfigurationId to 'New-AzSqlInstance' and 'Set-AzSqlInstance'</span></span>
* <span data-ttu-id="5c3ac-408">Correção de um bug em GetAzureSqlDatabaseReplicationLink.cs, em que o parâmetro PartnerServerName era verificado por valor em vez de chave</span><span class="sxs-lookup"><span data-stu-id="5c3ac-408">Fixed a bug in GetAzureSqlDatabaseReplicationLink.cs where PartnerServerName parameter was being checked for by value instead of key</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-409">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-409">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-410">Adição de suporte para novos recursos de restrição de acesso: ServiceTag, multi-ip e http-headers</span><span class="sxs-lookup"><span data-stu-id="5c3ac-410">Added support for new access restriction features: ServiceTag, multi-ip and http-headers</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="5c3ac-411">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-411">Thanks to our community contributors</span></span>
* <span data-ttu-id="5c3ac-412">John Q. Martin (@johnmart82) – Adição de informações de pré-requisitos do firewall (nº 13385)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-412">John Q. Martin (@johnmart82), Adding firewall prerequisite information (#13385)</span></span>
* <span data-ttu-id="5c3ac-413">Manikandan Duraisamy (@madurais-msft) – Correção do argumento PublicSubnetName (nº 13417)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-413">Manikandan Duraisamy (@madurais-msft), Corrected the PublicSubnetName argument (#13417)</span></span>
* <span data-ttu-id="5c3ac-414">@mahortas – Atualização dos valores do parâmetro -HostNames (nº 13349)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-414">@mahortas, Update for -HostNames parameter values (#13349)</span></span>
* <span data-ttu-id="5c3ac-415">@MariachiForHire – Adição de valores compatíveis com TrafficAnalyticsInterval (nº 13304)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-415">@MariachiForHire, added supported TrafficAnalyticsInterval values (#13304)</span></span>
* <span data-ttu-id="5c3ac-416">Michael James (@mikejwhat) – permissão para que Get-AzLogicAppRunHistory retorne mais de 30 entradas (nº 13393)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-416">Michael James (@mikejwhat), Allow Get-AzLogicAppRunHistory to return more than 30 entries (#13393)</span></span>
* <span data-ttu-id="5c3ac-417">Shashikant Shakya (@shshakya) – Atualização de Restore-AzSqlInstanceDatabase.md (nº 13404)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-417">Shashikant Shakya (@shshakya), Update Restore-AzSqlInstanceDatabase.md (#13404)</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="5c3ac-418">5.0.0 – outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-418">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-419">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-420">[Alteração da Falha] Remoção de 'Get-AzProfile' e 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-420">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="5c3ac-421">Substituição da Biblioteca de Autenticação do Azure Directory pela MSAL (Biblioteca de Autenticação da Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-421">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-422">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-422">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-423">[Alteração da Falha] Remoção do alias do parâmetro 'ClientIdAndSecret' em 'New-AzAksCluster' e 'Set-AzAksCluster'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-423">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="5c3ac-424">[Alteração da Falha] Alteração do valor padrão de 'NodeVmSetType' em 'New-AzAksCluster' de 'AvailabilitySet' para 'VirtualMachineScaleSets'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-424">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="5c3ac-425">[Alteração da Falha] Alteração do valor padrão de 'NetworkPlugin' em 'New-AzAksCluster' de 'None' para 'azure'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-425">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="5c3ac-426">[Alteração da Falha] Remoção do parâmetro 'NodeOsType' em 'New-AzAksCluster', pois ele é compatível somente com um valor Linux.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-426">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="5c3ac-427">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5c3ac-427">Az.Billing</span></span>
* <span data-ttu-id="5c3ac-428">Adição do cmdlet 'Get-AzBillingAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-428">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="5c3ac-429">Adição do cmdlet 'Get-AzBillingProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-429">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="5c3ac-430">Adição do cmdlet 'Get-AzInvoiceSection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-430">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="5c3ac-431">Adição de novos parâmetros ao cmdlet 'Get-AzBillingInvoice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-431">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="5c3ac-432">Remoção das propriedades DownloadUrlExpiry, Type e BillingPeriodNames da resposta do cmdlet Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="5c3ac-432">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-433">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-433">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-434">Adição de cmdlets para dar suporte a uma funcionalidade de link privado e várias origens</span><span class="sxs-lookup"><span data-stu-id="5c3ac-434">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-435">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-436">Atualização do SDK para 7.4.0-preview.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-436">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-437">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-438">Adição do parâmetro '-VmssId ' ao 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-438">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="5c3ac-439">Adição do parâmetro 'PlatformFaultDomainCount' ao cmdlet 'New-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-439">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-440">Novo cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-440">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="5c3ac-441">Adição dos parâmetros opcionais 'Tier' e 'LogicalSectorSize' ao cmdlet New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-441">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="5c3ac-442">Adição dos parâmetros opcionais 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly' e 'DiskMBpsReadOnly' ao cmdlet 'New-AzDiskUpdateConfig'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-442">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="5c3ac-443">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c3ac-443">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5c3ac-444">[Alteração da Falha] Atualiza a versão da API para a 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="5c3ac-444">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="5c3ac-445">[Alteração da Falha] Remoção do SKU 'Classic' e do parâmetro 'StorageAccountName' de 'New-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-445">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="5c3ac-446">Adição de novos cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule' e 'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-446">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="5c3ac-447">Adição do novo parâmetro 'NetworkRuleSet' ao 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-447">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="5c3ac-448">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-448">Az.Databricks</span></span>
* <span data-ttu-id="5c3ac-449">Correção de um bug que pode causar a atualização do workspace do Databricks sem que ocorra falha do `-EncryptionKeyVersion`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-449">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-450">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-450">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-451">Atualização do SDK do .NET do ADF para a versão 4.12.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-451">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="5c3ac-452">Atualização do SDK cliente da criptografia do ADF para a versão 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="5c3ac-452">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="5c3ac-453">Adição dos comandos 'Stop-AzDataFactoryV2TriggerRun' e 'Invoke-AzDataFactoryV2TriggerRun'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-453">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="5c3ac-454">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="5c3ac-454">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="5c3ac-455">Exigir a propriedade Location para criar objetos ARM de nível superior.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-455">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="5c3ac-456">\* `ApplicationGroupType` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-456">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="5c3ac-457">\* `HostPoolArmPath` agora é obrigatório para `New-AzWvdApplicationGroup`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-457">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="5c3ac-458">\* Adição do `PreferredAppGroupType` ao `New-AzWvdHostPool`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-458">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="5c3ac-459">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="5c3ac-459">Az.Functions</span></span>
* <span data-ttu-id="5c3ac-460">[Alteração da Falha] Remoção do parâmetro de opção 'IncludeSlot' de todos os parâmetros, exceto de um conjunto de parâmetros de 'Get-AzFunctionApp'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-460">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="5c3ac-461">O cmdlet agora é compatível com a recuperação de slots de implantação nos resultados em que '-IncludeSlot' for especificado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-461">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="5c3ac-462">Atualização do 'New-AzFunctionApp':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-462">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="5c3ac-463">Correção do -DisableApplicationInsights para que nenhum projeto do Application Insights seja criado quando essa opção for especificada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-463">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="5c3ac-464">[Nº 12728]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-464">[#12728]</span></span>
  - <span data-ttu-id="5c3ac-465">[Alteração da Falha] Remoção do suporte para criar aplicativos de funções do PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-465">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="5c3ac-466">[Alteração da Falha] Alteração da versão de runtime padrão da 6.2 para a 7.0 do Functions versão 3 no Windows para aplicativos de funções do PowerShell quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-466">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="5c3ac-467">[Alteração da Falha] Alteração da versão de runtime padrão da 10 para a 12 no Functions versão 3 no Windows e Linux para aplicativos de funções do Node quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-467">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="5c3ac-468">[Alteração da Falha] Alteração da versão de runtime padrão da 3.7 para a 3.8 no Functions versão 3 no Linux para aplicativos de funções do Python quando o parâmetro RuntimeVersion não for especificado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-468">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-469">Az.HDInsight</span></span>
 * <span data-ttu-id="5c3ac-470">Para o cmdlet New-AzHDInsightCluster:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-470">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="5c3ac-471">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-471">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="5c3ac-472">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-472">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="5c3ac-473">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-473">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="5c3ac-474">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-474">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="5c3ac-475">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-475">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="5c3ac-476">Adição de novos parâmetros: 'StorageFileSystem' e 'StorageAccountManagedIdentity' para dar suporte ao ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-476">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="5c3ac-477">Adição do novo parâmetro 'EnableIDBroker' para dar suporte ao Agente de IDs do HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-477">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="5c3ac-478">Adição de novos parâmetros: Parâmetros 'KafkaClientGroupId', 'KafkaClientGroupName' e 'KafkaManagementNodeSize' para dar suporte ao Proxy REST do Kafka</span><span class="sxs-lookup"><span data-stu-id="5c3ac-478">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="5c3ac-479">Para o cmdlet New-AzHDInsightClusterConfig:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-479">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="5c3ac-480">Substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-480">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="5c3ac-481">Substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-481">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="5c3ac-482">Substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-482">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="5c3ac-483">Remoção do parâmetro 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-483">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="5c3ac-484">Remoção do parâmetro 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-484">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="5c3ac-485">Para o cmdlet Set-AzHDInsightDefaultStorage:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-485">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-486">Substituição do parâmetro 'StorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-486">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="5c3ac-487">Para o cmdlet Add-AzHDInsightSecurityProfile:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-487">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-488">Substituição do parâmetro 'Domain' por 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-488">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="5c3ac-489">Remoção do requisito obrigatório para o parâmetro 'OrganizationalUnitDN'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-489">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-490">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-491">[Alteração da Falha] O parâmetro DisableSoftDelete foi preterido em 'New-AzKeyVault', bem como EnableSoftDelete em 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-491">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="5c3ac-492">[Alteração da Falha] Remoção do atributo SecretValueText para evitar a exibição de SecretValue de modo direto [Nº 12266]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-492">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="5c3ac-493">Um novo tipo de recurso é compatível: HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-493">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="5c3ac-494">Comandos CRUD de cmdlets e do HSM gerenciado para operar chaves no HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-494">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="5c3ac-495">Backup/restauração completos do HSM, criação de chave AES, backup/restauração do domínio de segurança e RBAC</span><span class="sxs-lookup"><span data-stu-id="5c3ac-495">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5c3ac-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-496">Az.ManagedServices</span></span>
* <span data-ttu-id="5c3ac-497">[Alteração da Falha] Atualização de parâmetros de convenções de nomenclatura e exemplos associados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-497">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-498">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-498">Az.Network</span></span>
* <span data-ttu-id="5c3ac-499">[Alteração da Falha] Remoção do parâmetro 'HostedSubnet' e adição de 'Subnet' como alternativa</span><span class="sxs-lookup"><span data-stu-id="5c3ac-499">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="5c3ac-500">Adição de novos cmdlets às Rotas do Par no Nível do Roteador Virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-500">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="5c3ac-501">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-501">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="5c3ac-502">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-502">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="5c3ac-503">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-503">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-504">Adição do parâmetro '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-504">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="5c3ac-505">Adição do parâmetro '-SkuName' e, para isso, o SKU foi executado com um Alias</span><span class="sxs-lookup"><span data-stu-id="5c3ac-505">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="5c3ac-506">Remoção do parâmetro '-Sku'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-506">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="5c3ac-507">[Alteração da Falha] O argumento 'Connectionlink' agora é obrigatório em 'Start-AzVpnConnectionPacketCapture' e 'Stop-AzVpnConnectionPacketCapture'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-507">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="5c3ac-508">[Alteração da Falha] Atualização do 'New-AzNetworkWatcherConnectionMonitorEndPointObject' para remover o parâmetro '-Filter'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-508">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="5c3ac-509">[Alteração da Falha] Substituição do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' por 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-509">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="5c3ac-510">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorEndPointObject':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-510">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-511">Adição do parâmetro '-Type'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-511">Added parameter '-Type'</span></span>
    - <span data-ttu-id="5c3ac-512">Adição do parâmetro '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-512">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="5c3ac-513">Adição do parâmetro '-Scope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-513">Added parameter '-Scope'</span></span>
* <span data-ttu-id="5c3ac-514">Atualização do cmdlet 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' com o novo parâmetro '-DestinationPortBehavior'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-514">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-515">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-515">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-516">Correção da Restauração da Carga de Trabalho para permissões de colaborador.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-516">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="5c3ac-517">Adição de novos conjuntos e novas validações de parâmetros ao cmdlet Restore-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-517">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-518">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-519">Correção de um bug de análise</span><span class="sxs-lookup"><span data-stu-id="5c3ac-519">Fixed parsing bug</span></span>
* <span data-ttu-id="5c3ac-520">Atualização de cmdlets What-If do modelo do ARM para remover uma mensagem de visualização dos resultados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-520">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="5c3ac-521">Correção de um problema em que ocorria falha nos cmdlets de implantação de modelo caso '-WhatIf' fosse definido em um escopo maior [Nº13038]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-521">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="5c3ac-522">Correção de um problema em que cmdlets de implantação de modelo não preservavam maiúsculas e minúsculas para parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-522">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="5c3ac-523">Adição de uma versão de API padrão para ser usada no cmdlet 'Export-AzResourceGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-523">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="5c3ac-524">Adição de cmdlets às Especificações de Modelo ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec' e 'Export-AzTemplateSpec')</span><span class="sxs-lookup"><span data-stu-id="5c3ac-524">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="5c3ac-525">Adição de um suporte para implantar Especificações de Modelo usando cmdlets de implantação existentes (por meio do novo parâmetro -TemplateSpecId)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-525">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="5c3ac-526">Atualização do parâmetro 'Get-AzResourceGroupDeploymentOperation' para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-526">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="5c3ac-527">Remoção do parâmetro '-ApiVersion' de cmdlets '\*-AzDeployment'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-527">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-528">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-529">Correção de um problema em que ocorria uma falha de New-AzSqlDatabaseExport caso networkIsolation não fosse especificado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-529">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="5c3ac-530">Correção de um problema em que New-AzSqlDatabaseExport e New-AzSqlDatabaseImport não retornavam OperationStatusLink no objeto de resultado [Nº 13097]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-530">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="5c3ac-531">Atualizar a URL de regiões emparelhadas do Azure em avisos de redundância de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-531">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-532">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-532">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-533">Remoção da propriedade obsoleta RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="5c3ac-533">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="5c3ac-534">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-534">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="5c3ac-535">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-535">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="5c3ac-536">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-536">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="5c3ac-537">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-537">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="5c3ac-538">Alterar o Tipo de DaysAfterModificationGreaterThan de int para int?</span><span class="sxs-lookup"><span data-stu-id="5c3ac-538">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="5c3ac-539">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-539">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="5c3ac-540">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-540">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="5c3ac-541">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-541">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="5c3ac-542">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-542">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="5c3ac-543">Criação/atualização de compartilhamento de arquivo compatível com uma camada de acesso</span><span class="sxs-lookup"><span data-stu-id="5c3ac-543">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="5c3ac-544">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-544">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="5c3ac-545">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-545">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="5c3ac-546">Definição/atualização/removção recursiva de ACL compatível com um item do Datalake Gen2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-546">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="5c3ac-547">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-547">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="5c3ac-548">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-548">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="5c3ac-549">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-549">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="5c3ac-550">Política de acesso de Contêiner compatível com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="5c3ac-550">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="5c3ac-551">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-551">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="5c3ac-552">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-552">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="5c3ac-553">Alteração da saída do cmdlet da política de acesso ao Contêiner get/set mudando o tipo de Permissão de propriedade filho de enum para String</span><span class="sxs-lookup"><span data-stu-id="5c3ac-553">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="5c3ac-554">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-554">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="5c3ac-555">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-555">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="5c3ac-556">Correção de um problema do script de exemplo da política de gerenciamento de conjuntos com JSON</span><span class="sxs-lookup"><span data-stu-id="5c3ac-556">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="5c3ac-557">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-557">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-558">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-558">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-559">Adição de suporte para o tipo de preço Premium V3</span><span class="sxs-lookup"><span data-stu-id="5c3ac-559">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="5c3ac-560">Atualização do SDK de Sites para a versão 3.1.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-560">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="5c3ac-561">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-561">Thanks to our community contributors</span></span>
* <span data-ttu-id="5c3ac-562">@atul-ram, por atualizar Get-AzDelegation.md (nº 13176)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-562">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="5c3ac-563">@dineshreddy007, por obter as Funções de Aplicativos atribuídas de modo correto em caso de registro do Stack HCI usando um token WAC.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-563">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="5c3ac-564">(nº 13249)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-564">(#13249)</span></span>
* <span data-ttu-id="5c3ac-565">@kongou-ae, por atualizar New-AzOffice365PolicyProperty.md (nº 13217)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-565">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="5c3ac-566">Lohith Chowdary Chilukuri (@Lochiluk), por atualizar Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-566">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="5c3ac-567">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-567">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="5c3ac-568">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13203)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-568">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="5c3ac-569">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13190)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-569">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="5c3ac-570">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13189)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-570">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="5c3ac-571">Adicionar links aos cmdlets referenciados (nº 13137)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-571">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="5c3ac-572">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13204)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-572">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="5c3ac-573">Adicionar links aos cmdlets do PowerShell referenciados no documento (nº 13205)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-573">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="5c3ac-574">4.8.0 – Outubro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-574">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-575">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-576">Foi corrigido um problema de análise de datetime em bibliotecas comuns [#13045]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-576">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-577">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-578">Foi adicionado o cmdlet 'New-AzCognitiveServicesAccountApiProperty'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-578">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-579">Parâmetro 'ApiProperty' compatível com 'New-AzCognitiveServicesAccount' e 'Set-AzCognitiveServicesAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-579">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-580">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-580">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-581">Foi corrigido o problema em 'Update-ASRRecoveryPlan' populando o FailoverTypes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-581">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="5c3ac-582">Foram adicionados os parâmetros opcionais '-Top' e '-OrderBy' ao cmdlet 'Get-AzVmImage'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-582">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="5c3ac-583">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-583">Az.Databricks</span></span>
* <span data-ttu-id="5c3ac-584">Disponibilidade geral do módulo 'Az.Databricks'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-584">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="5c3ac-585">Foi adicionado suporte para emparelhamento de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-585">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-586">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-587">Foi corrigido erro de digitação nas mensagens de saída</span><span class="sxs-lookup"><span data-stu-id="5c3ac-587">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-588">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-588">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-589">Foi adicionado o parâmetro de opção opcional 'TrustedServiceAccessEnabled' ao cmdlet 'Set-AzEventHubNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-589">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-590">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-590">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-591">Foi adicionada uma mensagem de aviso para planejamento do preterimento dos parâmetros 'PublicNetworkAccessType' e 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-591">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="5c3ac-592">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountName' por 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-592">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="5c3ac-593">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountKey' por 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-593">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="5c3ac-594">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageAccountType' por 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-594">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="5c3ac-595">Adicionada mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageContainer' por 'StorageContainer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-595">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="5c3ac-596">Foi adicionada uma mensagem de aviso para planejar a substituição do parâmetro 'DefaultStorageRootPath' por 'StorageRootPath'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-596">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-597">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-597">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-598">O SDK de dispositivos foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-598">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-599">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-599">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-600">A data detalhada da remoção da propriedade SecretValueText foi fornecida</span><span class="sxs-lookup"><span data-stu-id="5c3ac-600">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5c3ac-601">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-601">Az.ManagedServices</span></span>
* <span data-ttu-id="5c3ac-602">Os avisos de alteração da falha nos cmdlets de definição e atribuição de serviços gerenciados foram atualizados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-602">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-603">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-603">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-604">Foi corrigido o bug que fazia com que a mensagem de aviso não pudesse ser suprimida.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-604">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="5c3ac-605">[#12889]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-605">[#12889]</span></span>
* <span data-ttu-id="5c3ac-606">Parâmetro 'SkipMetricValidation' com suporte nos critérios da regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-606">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="5c3ac-607">Permite criar uma regra de alerta em uma métrica personalizada que ainda não foi emitida, fazendo com que a validação da métrica seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-607">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-608">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-608">Az.Network</span></span>
* <span data-ttu-id="5c3ac-609">Política do Office365 adicionada ao recurso VPNSite</span><span class="sxs-lookup"><span data-stu-id="5c3ac-609">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="5c3ac-610">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-610">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-612">Foi adicionada a validação do nome do contêiner para backup da carga de trabalho.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-612">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c3ac-613">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-613">Az.RedisCache</span></span>
* <span data-ttu-id="5c3ac-614">Correção dos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache' para não falharem devido a um problema de permissão relacionado ao registro do RP do Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-614">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-615">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-615">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-616">Foi adicionado BackupStorageRedundancy ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-616">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="5c3ac-617">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-617">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="5c3ac-618">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-618">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="5c3ac-619">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-619">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="5c3ac-620">Foi removida a diferenciação de maiúsculas e minúsculas para o parâmetro BackupStorageRedundancy em todas as referências de Banco de Dados SQL</span><span class="sxs-lookup"><span data-stu-id="5c3ac-620">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="5c3ac-621">Foram atualizados os nomes das mensagens de aviso do BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-621">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-622">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-622">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-623">Suporte para habilitar/desabilitar/obter propriedades de exclusão reversível de compartilhamento no serviço de arquivo de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-623">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="5c3ac-624">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-624">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="5c3ac-625">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-625">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="5c3ac-626">Os compartilhamentos de arquivos de lista com suporte incluem os excluídos de uma conta de armazenamento e obtêm uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="5c3ac-626">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="5c3ac-627">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-627">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="5c3ac-628">Suporte para restauração de um compartilhamento de arquivo excluído</span><span class="sxs-lookup"><span data-stu-id="5c3ac-628">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="5c3ac-629">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-629">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="5c3ac-630">Foram alterados os cmdlets para modificar as propriedades do serviço blobs, não obtendo as propriedades originais do servidor, mas apenas definindo as propriedades modificadas no servidor.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-630">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="5c3ac-631">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-631">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="5c3ac-632">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-632">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="5c3ac-633">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-633">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="5c3ac-634">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-634">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="5c3ac-635">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-635">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="5c3ac-636">Foi corrigido o problema de ajuda para o valor padrão do tipo do parâmetro New-AzStorageAccount [#12189]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-636">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="5c3ac-637">Foi corrigido o problema adicionando exemplo para mostrar como definir o ContentType correto no upload do blob [#12989]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-637">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="5c3ac-638">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-638">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-639">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-639">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-640">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-640">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="5c3ac-641">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="5c3ac-641">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-642">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-642">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-643">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-643">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="5c3ac-644">[#12372]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-644">[#12372]</span></span>
* <span data-ttu-id="5c3ac-645">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-645">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="5c3ac-646">[#11239]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-646">[#11239]</span></span>
* <span data-ttu-id="5c3ac-647">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-647">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="5c3ac-648">[#11239]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-648">[#11239]</span></span>
* <span data-ttu-id="5c3ac-649">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-649">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="5c3ac-650">[#12371]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-650">[#12371]</span></span>
* <span data-ttu-id="5c3ac-651">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-651">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-653">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-653">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-654">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-655">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-655">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="5c3ac-656">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-656">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="5c3ac-657">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-657">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="5c3ac-658">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-658">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="5c3ac-659">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5c3ac-659">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="5c3ac-660">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-660">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="5c3ac-661">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-661">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="5c3ac-662">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-662">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="5c3ac-663">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-663">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="5c3ac-664">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-664">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-665">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-665">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-666">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-666">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-667">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-667">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-668">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-668">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="5c3ac-669">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-669">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="5c3ac-670">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="5c3ac-670">Az.Functions</span></span>
* <span data-ttu-id="5c3ac-671">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-671">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="5c3ac-672">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-672">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="5c3ac-673">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-673">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-674">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-674">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-675">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="5c3ac-675">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="5c3ac-676">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-676">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="5c3ac-677">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="5c3ac-677">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="5c3ac-678">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-678">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-679">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-679">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-680">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-680">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-681">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-681">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-682">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-682">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-683">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-683">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-684">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-684">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="5c3ac-685">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-685">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="5c3ac-686">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="5c3ac-686">Az.Kusto</span></span>
* <span data-ttu-id="5c3ac-687">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-687">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-688">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-688">Az.Network</span></span>
* <span data-ttu-id="5c3ac-689">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-689">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="5c3ac-690">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-690">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="5c3ac-691">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="5c3ac-691">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="5c3ac-692">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-692">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="5c3ac-693">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-693">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="5c3ac-694">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-694">Added subscription level parameter set</span></span>
    - <span data-ttu-id="5c3ac-695">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-695">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="5c3ac-696">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-696">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="5c3ac-697">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-697">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="5c3ac-698">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-698">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="5c3ac-699">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-699">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="5c3ac-700">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-700">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="5c3ac-701">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5c3ac-701">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="5c3ac-702">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-702">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="5c3ac-703">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-703">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="5c3ac-704">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-704">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="5c3ac-705">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-705">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="5c3ac-706">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-706">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="5c3ac-707">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-707">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="5c3ac-708">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-708">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="5c3ac-709">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-709">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="5c3ac-710">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-710">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="5c3ac-711">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-711">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="5c3ac-712">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-712">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-713">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-713">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-714">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-714">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-715">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-715">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-716">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-716">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="5c3ac-717">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-717">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="5c3ac-718">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="5c3ac-718">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="5c3ac-719">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-719">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-720">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-720">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-721">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-721">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="5c3ac-722">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-722">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="5c3ac-723">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-723">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="5c3ac-724">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-724">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="5c3ac-725">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-725">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="5c3ac-726">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-726">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="5c3ac-727">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-727">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="5c3ac-728">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-728">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="5c3ac-729">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-729">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="5c3ac-730">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-730">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="5c3ac-731">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-731">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="5c3ac-732">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-732">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="5c3ac-733">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-733">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="5c3ac-734">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-734">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="5c3ac-735">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-735">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="5c3ac-736">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-736">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-737">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-737">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-738">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-738">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="5c3ac-739">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-739">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="5c3ac-740">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-740">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="5c3ac-741">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-741">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="5c3ac-742">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-742">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="5c3ac-743">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-743">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="5c3ac-744">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-744">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="5c3ac-745">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-745">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="5c3ac-746">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-746">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="5c3ac-747">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-747">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="5c3ac-748">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-748">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="5c3ac-749">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-749">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="5c3ac-750">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="5c3ac-750">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="5c3ac-751">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-751">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="5c3ac-752">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-752">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="5c3ac-753">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-753">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="5c3ac-754">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-754">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="5c3ac-755">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-755">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-756">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-757">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-757">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="5c3ac-758">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3ac-758">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="5c3ac-759">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-759">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="5c3ac-760">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-760">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="5c3ac-761">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-761">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="5c3ac-762">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-762">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="5c3ac-763">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-763">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="5c3ac-764">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-764">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="5c3ac-765">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="5c3ac-765">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="5c3ac-766">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-766">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="5c3ac-767">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-767">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="5c3ac-768">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-768">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="5c3ac-769">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-769">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="5c3ac-770">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-770">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="5c3ac-771">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-771">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="5c3ac-772">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="5c3ac-772">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="5c3ac-773">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-773">Thanks to our community contributors</span></span>
* <span data-ttu-id="5c3ac-774">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-774">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="5c3ac-775">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-775">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="5c3ac-776">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-776">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="5c3ac-777">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-777">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="5c3ac-778">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-778">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="5c3ac-779">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-779">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="5c3ac-780">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-780">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="5c3ac-781">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-781">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="5c3ac-782">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-782">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="5c3ac-783">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-783">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="5c3ac-784">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-784">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="5c3ac-785">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-785">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="5c3ac-786">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-786">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-787">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-787">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="5c3ac-788">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-788">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-789">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-789">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-790">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-790">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="5c3ac-791">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-791">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-792">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-792">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-793">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="5c3ac-793">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-794">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-794">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-795">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-795">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="5c3ac-796">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-796">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="5c3ac-797">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-797">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="5c3ac-798">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-798">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-799">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-800">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-800">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-801">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-801">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-802">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-802">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-803">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-803">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-804">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="5c3ac-804">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="5c3ac-805">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="5c3ac-805">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="5c3ac-806">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-806">Az.Maintenance</span></span>
* <span data-ttu-id="5c3ac-807">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-807">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="5c3ac-808">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-808">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5c3ac-809">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-809">Az.ManagedServices</span></span>
* <span data-ttu-id="5c3ac-810">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-810">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-811">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-811">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-812">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-812">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="5c3ac-813">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="5c3ac-813">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-814">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-814">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-815">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-815">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="5c3ac-816">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-816">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="5c3ac-817">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-817">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="5c3ac-818">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="5c3ac-818">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="5c3ac-819">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-819">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="5c3ac-820">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="5c3ac-820">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="5c3ac-821">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-821">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="5c3ac-822">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="5c3ac-822">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c3ac-823">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-823">Az.SignalR</span></span>
* <span data-ttu-id="5c3ac-824">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-824">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="5c3ac-825">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-825">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-826">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-826">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-827">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="5c3ac-827">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="5c3ac-828">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-828">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="5c3ac-829">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-829">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="5c3ac-830">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-830">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="5c3ac-831">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-831">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="5c3ac-832">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-832">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="5c3ac-833">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-833">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="5c3ac-834">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-834">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="5c3ac-835">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-835">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="5c3ac-836">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-836">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="5c3ac-837">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-837">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="5c3ac-838">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-838">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="5c3ac-839">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-839">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="5c3ac-840">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-840">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="5c3ac-841">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-841">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="5c3ac-842">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-842">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-843">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-843">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-844">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-844">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="5c3ac-845">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-845">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="5c3ac-846">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-846">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="5c3ac-847">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-847">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="5c3ac-848">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="5c3ac-848">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-849">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-849">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-850">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="5c3ac-850">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="5c3ac-851">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="5c3ac-851">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-852">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-852">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-853">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-853">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-854">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-854">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-855">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-855">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-856">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-856">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-857">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-857">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-858">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-858">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-859">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-859">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-860">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-860">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-861">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-861">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-862">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-862">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-863">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-863">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-864">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-864">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-865">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-866">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-866">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-867">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-867">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-868">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-868">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-869">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-869">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-870">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-870">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="5c3ac-871">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5c3ac-871">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="5c3ac-872">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-872">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="5c3ac-873">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-873">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="5c3ac-874">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5c3ac-874">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="5c3ac-875">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-875">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="5c3ac-876">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="5c3ac-876">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-877">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-877">Az.Network</span></span>
* <span data-ttu-id="5c3ac-878">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-878">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="5c3ac-879">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-879">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="5c3ac-880">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-880">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="5c3ac-881">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-881">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-882">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-882">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-883">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-883">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="5c3ac-884">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-884">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="5c3ac-885">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-885">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-887">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-887">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-888">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-888">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-889">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-889">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="5c3ac-890">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-890">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-891">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-892">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-892">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="5c3ac-893">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5c3ac-893">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-894">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-894">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-895">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="5c3ac-895">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="5c3ac-896">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-896">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="5c3ac-897">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5c3ac-897">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="5c3ac-898">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="5c3ac-898">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="5c3ac-899">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="5c3ac-899">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="5c3ac-900">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="5c3ac-900">Supported get single file share usage</span></span>
    - <span data-ttu-id="5c3ac-901">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-901">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="5c3ac-902">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-902">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-903">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-903">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-904">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-904">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="5c3ac-905">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-905">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-906">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-906">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-907">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-907">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c3ac-908">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-908">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c3ac-909">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-909">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-910">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-910">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-911">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-911">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-912">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-912">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-913">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-913">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-914">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-914">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-915">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-915">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c3ac-916">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c3ac-916">Az.EventGrid</span></span>
* <span data-ttu-id="5c3ac-917">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-917">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="5c3ac-918">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-918">Added new features:</span></span>
    - <span data-ttu-id="5c3ac-919">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-919">Input mapping</span></span>
    - <span data-ttu-id="5c3ac-920">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-920">Event Delivery Schema</span></span>
    - <span data-ttu-id="5c3ac-921">Link Privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-921">Private Link</span></span>
    - <span data-ttu-id="5c3ac-922">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="5c3ac-922">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="5c3ac-923">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="5c3ac-923">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="5c3ac-924">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="5c3ac-924">Azure Function As Destination</span></span>
    - <span data-ttu-id="5c3ac-925">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-925">WebHook Batching</span></span>
    - <span data-ttu-id="5c3ac-926">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-926">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="5c3ac-927">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="5c3ac-927">IpFiltering</span></span>
* <span data-ttu-id="5c3ac-928">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-928">Updated cmdlets:</span></span>
    - <span data-ttu-id="5c3ac-929">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-929">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="5c3ac-930">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-930">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="5c3ac-931">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-931">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="5c3ac-932">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-932">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="5c3ac-933">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-933">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="5c3ac-934">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-934">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="5c3ac-935">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-935">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="5c3ac-936">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-936">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="5c3ac-937">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-937">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-938">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-938">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-939">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="5c3ac-939">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="5c3ac-940">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-940">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-941">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-941">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-942">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-942">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-943">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-943">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-944">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-944">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-945">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-945">Az.Network</span></span>
* <span data-ttu-id="5c3ac-946">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-946">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="5c3ac-947">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-947">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="5c3ac-948">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-948">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="5c3ac-949">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-949">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="5c3ac-950">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-950">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="5c3ac-951">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-951">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="5c3ac-952">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-952">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="5c3ac-953">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-953">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="5c3ac-954">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-954">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="5c3ac-955">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-955">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="5c3ac-956">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-956">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="5c3ac-957">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-957">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="5c3ac-958">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-958">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="5c3ac-959">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-959">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="5c3ac-960">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-960">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="5c3ac-961">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-961">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="5c3ac-962">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-962">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-963">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-963">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-964">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-964">Removed project reference to Authentication</span></span>
* <span data-ttu-id="5c3ac-965">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-965">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="5c3ac-966">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-966">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-967">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-967">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-968">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-968">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="5c3ac-969">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-969">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-970">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-970">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-971">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-971">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="5c3ac-972">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-972">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="5c3ac-973">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-973">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-974">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-975">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-975">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="5c3ac-976">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-976">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="5c3ac-977">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-977">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="5c3ac-978">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="5c3ac-979">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-979">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="5c3ac-980">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-980">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="5c3ac-981">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="5c3ac-981">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="5c3ac-982">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-982">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="5c3ac-983">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="5c3ac-983">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="5c3ac-984">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-984">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="5c3ac-985">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-985">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="5c3ac-986">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="5c3ac-986">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="5c3ac-987">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-987">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="5c3ac-988">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-988">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="5c3ac-989">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-989">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="5c3ac-990">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-990">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="5c3ac-991">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-991">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c3ac-992">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c3ac-992">Az.StorageSync</span></span>
* <span data-ttu-id="5c3ac-993">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="5c3ac-993">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="5c3ac-994">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-994">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="5c3ac-995">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-995">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="5c3ac-996">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-996">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-997">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-997">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-998">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-998">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="5c3ac-999">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-999">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1000">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1000">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1001">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1001">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="5c3ac-1002">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1002">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="5c3ac-1003">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1003">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="5c3ac-1004">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1004">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-1005">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1005">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-1006">O uso da [API AccessProfile](/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1006">Replaced usage of old [AccessProfile API](/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c3ac-1007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1007">Az.Batch</span></span>
* <span data-ttu-id="5c3ac-1008">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1008">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="5c3ac-1009">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1009">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-1010">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1010">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-1011">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1011">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="5c3ac-1012">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1012">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1013">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1013">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1014">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1014">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="5c3ac-1015">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1015">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="5c3ac-1016">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1016">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="5c3ac-1017">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1017">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="5c3ac-1018">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1018">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1019">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1019">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1020">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1020">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-1021">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1021">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-1022">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1022">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="5c3ac-1023">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1023">Az.Functions</span></span>
* <span data-ttu-id="5c3ac-1024">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1024">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-1025">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1025">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-1026">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1026">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5c3ac-1027">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1027">Az.HealthcareApis</span></span>
* <span data-ttu-id="5c3ac-1028">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1028">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="5c3ac-1029">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1029">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-1030">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1030">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-1031">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1031">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="5c3ac-1032">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1032">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1033">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1034">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1034">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="5c3ac-1035">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1035">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="5c3ac-1036">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1036">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="5c3ac-1037">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1037">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="5c3ac-1038">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1038">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="5c3ac-1039">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1039">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="5c3ac-1040">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1040">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="5c3ac-1041">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1041">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="5c3ac-1042">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1042">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="5c3ac-1043">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1043">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="5c3ac-1044">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1044">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="5c3ac-1045">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1045">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="5c3ac-1046">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1046">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="5c3ac-1047">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1047">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="5c3ac-1048">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1048">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="5c3ac-1049">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1049">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="5c3ac-1050">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1050">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="5c3ac-1051">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1051">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="5c3ac-1052">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1052">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="5c3ac-1053">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1053">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="5c3ac-1054">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1054">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="5c3ac-1055">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1055">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="5c3ac-1056">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1056">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="5c3ac-1057">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1057">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="5c3ac-1058">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1058">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="5c3ac-1059">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1059">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="5c3ac-1060">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1060">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="5c3ac-1061">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1061">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="5c3ac-1062">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1062">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1063">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1063">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1064">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1064">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1065">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1065">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1066">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1066">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1067">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1067">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="5c3ac-1068">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1068">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="5c3ac-1069">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1069">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="5c3ac-1070">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1070">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="5c3ac-1071">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1071">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="5c3ac-1072">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1072">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="5c3ac-1073">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1073">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="5c3ac-1074">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1074">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="5c3ac-1075">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1075">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="5c3ac-1076">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1076">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="5c3ac-1077">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1077">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5c3ac-1078">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1078">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5c3ac-1079">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1079">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="5c3ac-1080">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1080">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="5c3ac-1081">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1081">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="5c3ac-1082">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1082">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-1083">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1083">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-1084">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1084">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="5c3ac-1085">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1085">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="5c3ac-1086">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1086">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="5c3ac-1087">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1087">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="5c3ac-1088">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1088">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1089">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1089">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1090">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1090">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="5c3ac-1091">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1091">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1092">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1093">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1093">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="5c3ac-1094">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1094">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="5c3ac-1095">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1095">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="5c3ac-1096">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1096">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="5c3ac-1097">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1097">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="5c3ac-1098">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1098">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1099">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1099">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1100">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1100">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="5c3ac-1101">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1101">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="5c3ac-1102">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1102">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1103">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1103">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1104">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1104">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="5c3ac-1105">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1105">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="5c3ac-1106">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1106">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-1107">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1107">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-1108">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1108">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5c3ac-1109">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1109">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="5c3ac-1110">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1110">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="5c3ac-1111">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1111">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="5c3ac-1112">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1112">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="5c3ac-1113">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1113">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="5c3ac-1114">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1114">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1115">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1115">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1116">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1116">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c3ac-1117">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1117">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c3ac-1118">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1118">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-1119">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1119">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-1120">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1120">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="5c3ac-1121">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1121">Az.Billing</span></span>
* <span data-ttu-id="5c3ac-1122">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1122">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-1123">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1123">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-1124">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1124">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1125">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1125">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1126">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1126">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="5c3ac-1127">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1127">Az.DataShare</span></span>
* <span data-ttu-id="5c3ac-1128">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1128">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="5c3ac-1129">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1129">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="5c3ac-1130">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1130">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-1131">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1131">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-1132">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1132">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="5c3ac-1133">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1133">Added optional parameters to</span></span> 
    - <span data-ttu-id="5c3ac-1134">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1134">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="5c3ac-1135">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1135">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-1136">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1136">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-1137">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1137">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5c3ac-1138">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1138">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5c3ac-1139">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1139">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="5c3ac-1140">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1140">Az.PrivateDns</span></span>
* <span data-ttu-id="5c3ac-1141">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1141">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1143">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1143">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="5c3ac-1144">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1144">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1145">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1145">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1146">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1146">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="5c3ac-1147">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1147">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="5c3ac-1148">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1148">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="5c3ac-1149">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1149">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="5c3ac-1150">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1150">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1151">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1152">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1152">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="5c3ac-1153">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1153">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="5c3ac-1154">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1154">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1155">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1155">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1156">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1156">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="5c3ac-1157">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1157">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="5c3ac-1158">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1158">Highlights since the last release</span></span>
* <span data-ttu-id="5c3ac-1159">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1159">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="5c3ac-1160">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1160">General availability of Az.Functions</span></span> 
* <span data-ttu-id="5c3ac-1161">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1161">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1162">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1163">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1163">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="5c3ac-1164">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1164">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-1165">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1165">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-1166">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1166">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="5c3ac-1167">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1167">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="5c3ac-1168">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1168">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-1169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1169">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-1170">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1170">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="5c3ac-1171">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1171">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="5c3ac-1172">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1172">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5c3ac-1173">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1173">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="5c3ac-1174">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1174">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5c3ac-1175">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1175">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="5c3ac-1176">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1176">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5c3ac-1177">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1177">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="5c3ac-1178">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1178">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="5c3ac-1179">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1179">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="5c3ac-1180">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1180">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="5c3ac-1181">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1181">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="5c3ac-1182">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1182">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="5c3ac-1183">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1183">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="5c3ac-1184">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1184">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="5c3ac-1185">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1185">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5c3ac-1186">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1186">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5c3ac-1187">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1187">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="5c3ac-1188">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1188">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="5c3ac-1189">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1189">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c3ac-1190">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1190">Az.Batch</span></span>
* <span data-ttu-id="5c3ac-1191">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1191">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="5c3ac-1192">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1192">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="5c3ac-1193">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1193">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="5c3ac-1194">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1194">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="5c3ac-1195">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1195">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="5c3ac-1196">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1196">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="5c3ac-1197">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1197">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="5c3ac-1198">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1198">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="5c3ac-1199">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1199">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1200">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1200">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1201">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1201">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="5c3ac-1202">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1202">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="5c3ac-1203">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1203">Breaking changes</span></span>
    - <span data-ttu-id="5c3ac-1204">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1204">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="5c3ac-1205">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1205">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="5c3ac-1206">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1206">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="5c3ac-1207">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1207">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="5c3ac-1208">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1208">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="5c3ac-1209">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1209">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="5c3ac-1210">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1210">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1211">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1212">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1212">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-1213">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1213">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-1214">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1214">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="5c3ac-1215">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1215">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="5c3ac-1216">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1216">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="5c3ac-1217">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1217">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="5c3ac-1218">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1218">Az.Functions</span></span>
* <span data-ttu-id="5c3ac-1219">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1219">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-1220">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1220">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-1221">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1221">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5c3ac-1222">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1222">Az.HealthcareApis</span></span>
* <span data-ttu-id="5c3ac-1223">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1223">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-1224">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1224">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-1225">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1225">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="5c3ac-1226">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1226">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="5c3ac-1227">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1227">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="5c3ac-1228">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1228">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="5c3ac-1229">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1229">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="5c3ac-1230">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1230">New cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1231">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1231">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="5c3ac-1232">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1232">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="5c3ac-1233">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1233">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="5c3ac-1234">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1234">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="5c3ac-1235">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1235">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="5c3ac-1236">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1236">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-1237">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1237">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-1238">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1238">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="5c3ac-1239">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1239">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="5c3ac-1240">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1240">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="5c3ac-1241">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1241">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="5c3ac-1242">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1242">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="5c3ac-1243">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1243">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="5c3ac-1244">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1244">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-1245">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1245">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-1246">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1246">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="5c3ac-1247">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1247">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="5c3ac-1248">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1248">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="5c3ac-1249">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1249">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="5c3ac-1250">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1250">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="5c3ac-1251">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1251">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="5c3ac-1252">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1252">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1253">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1253">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1254">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1254">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="5c3ac-1255">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1255">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="5c3ac-1256">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1256">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="5c3ac-1257">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1257">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="5c3ac-1258">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1258">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="5c3ac-1259">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1259">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-1260">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1260">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="5c3ac-1261">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1261">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="5c3ac-1262">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1262">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="5c3ac-1263">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1263">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="5c3ac-1264">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1264">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="5c3ac-1265">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1265">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="5c3ac-1266">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1266">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="5c3ac-1267">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1267">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="5c3ac-1268">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1268">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="5c3ac-1269">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1269">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="5c3ac-1270">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1270">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="5c3ac-1271">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1271">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="5c3ac-1272">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1272">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="5c3ac-1273">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1273">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="5c3ac-1274">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1274">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="5c3ac-1275">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1275">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="5c3ac-1276">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1276">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="5c3ac-1277">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1277">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-1278">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1278">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-1279">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1279">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-1280">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1280">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="5c3ac-1281">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1281">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="5c3ac-1282">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1282">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="5c3ac-1283">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1283">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="5c3ac-1284">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1284">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="5c3ac-1285">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1285">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="5c3ac-1286">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1286">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="5c3ac-1287">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1287">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1288">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1288">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1289">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1289">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="5c3ac-1290">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1290">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="5c3ac-1291">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1291">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="5c3ac-1292">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1292">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="5c3ac-1293">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1293">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1294">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1294">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1295">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1295">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="5c3ac-1296">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1296">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="5c3ac-1297">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1297">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="5c3ac-1298">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1298">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="5c3ac-1299">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1299">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="5c3ac-1300">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1300">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="5c3ac-1301">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1301">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="5c3ac-1302">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1302">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="5c3ac-1303">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1303">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="5c3ac-1304">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1304">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="5c3ac-1305">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1305">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="5c3ac-1306">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1306">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="5c3ac-1307">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1307">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="5c3ac-1308">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1308">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="5c3ac-1309">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1309">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="5c3ac-1310">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1310">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="5c3ac-1311">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1311">'New-AzDeployment'</span></span>
    - <span data-ttu-id="5c3ac-1312">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1312">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="5c3ac-1313">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1313">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5c3ac-1314">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1314">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-1315">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1315">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-1316">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1316">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1317">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1318">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1318">Enhance performance of:</span></span>
    - <span data-ttu-id="5c3ac-1319">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1319">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5c3ac-1320">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1320">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5c3ac-1321">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1321">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5c3ac-1322">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1322">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="5c3ac-1323">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1323">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="5c3ac-1324">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1324">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="5c3ac-1325">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1325">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="5c3ac-1326">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1326">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="5c3ac-1327">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1327">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="5c3ac-1328">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1328">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1329">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1329">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1330">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1330">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="5c3ac-1331">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1331">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="5c3ac-1332">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1332">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="5c3ac-1333">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1333">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="5c3ac-1334">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1334">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="5c3ac-1335">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1335">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="5c3ac-1336">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1336">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="5c3ac-1337">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1337">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="5c3ac-1338">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1338">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="5c3ac-1339">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1339">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="5c3ac-1340">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1340">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="5c3ac-1341">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1341">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="5c3ac-1342">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1342">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="5c3ac-1343">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1343">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="5c3ac-1344">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1344">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="5c3ac-1345">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1345">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="5c3ac-1346">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1346">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="5c3ac-1347">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1347">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="5c3ac-1348">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1348">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5c3ac-1349">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1349">Supported failover Storage account</span></span>
    - <span data-ttu-id="5c3ac-1350">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1350">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="5c3ac-1351">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1351">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="5c3ac-1352">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1352">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="5c3ac-1353">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1353">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="5c3ac-1354">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1354">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="5c3ac-1355">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1355">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="5c3ac-1356">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1356">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="5c3ac-1357">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1357">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="5c3ac-1358">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1358">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="5c3ac-1359">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1359">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="5c3ac-1360">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1360">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="5c3ac-1361">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1361">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="5c3ac-1362">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1362">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="5c3ac-1363">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1363">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="5c3ac-1364">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1364">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="5c3ac-1365">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1365">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="5c3ac-1366">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1366">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="5c3ac-1367">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1367">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="5c3ac-1368">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1368">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5c3ac-1369">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1369">Az.TrafficManager</span></span>
* <span data-ttu-id="5c3ac-1370">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1370">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-1371">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1371">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-1372">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1372">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="5c3ac-1373">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1373">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="5c3ac-1374">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1374">Highlights since the last release</span></span>
* <span data-ttu-id="5c3ac-1375">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1375">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1376">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1376">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1377">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1377">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-1378">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1378">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-1379">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1379">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="5c3ac-1380">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1380">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1381">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-1382">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1382">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-1384">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1384">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1385">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1386">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1386">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-1387">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1387">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-1388">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1388">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-1389">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1389">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1390">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1390">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="5c3ac-1391">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1391">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="5c3ac-1392">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1392">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="5c3ac-1393">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1393">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1394">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1394">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="5c3ac-1395">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1395">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="5c3ac-1396">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1396">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="5c3ac-1397">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1397">New cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1398">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1398">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1399">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1399">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1400">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1400">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="5c3ac-1401">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1401">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="5c3ac-1402">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1402">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-1403">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1403">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-1404">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1404">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="5c3ac-1405">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1405">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="5c3ac-1406">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1406">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="5c3ac-1407">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1407">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="5c3ac-1408">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1408">Az.Maintenance</span></span>
* <span data-ttu-id="5c3ac-1409">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1409">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-1410">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1410">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-1411">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1411">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="5c3ac-1412">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1412">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5c3ac-1413">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1413">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5c3ac-1414">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1414">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5c3ac-1415">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1415">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="5c3ac-1416">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1416">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="5c3ac-1417">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1417">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="5c3ac-1418">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1418">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1419">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1420">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1420">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="5c3ac-1421">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1421">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="5c3ac-1422">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1422">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="5c3ac-1423">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1423">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="5c3ac-1424">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1424">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="5c3ac-1425">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1425">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="5c3ac-1426">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1426">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="5c3ac-1427">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1427">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="5c3ac-1428">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1428">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="5c3ac-1429">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1429">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="5c3ac-1430">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1430">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="5c3ac-1431">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1431">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="5c3ac-1432">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1432">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="5c3ac-1433">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1433">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="5c3ac-1434">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1434">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="5c3ac-1435">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1435">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-1436">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1436">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-1437">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1437">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="5c3ac-1438">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1438">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-1439">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1439">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-1440">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1440">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1441">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1441">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1442">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1442">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="5c3ac-1443">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1443">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1444">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1444">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1445">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1445">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="5c3ac-1446">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1446">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="5c3ac-1447">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1447">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="5c3ac-1448">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1448">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="5c3ac-1449">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1449">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="5c3ac-1450">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1450">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5c3ac-1451">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1451">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5c3ac-1452">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1452">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="5c3ac-1453">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1453">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5c3ac-1454">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1454">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="5c3ac-1455">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1455">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="5c3ac-1456">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1456">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="5c3ac-1457">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1457">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="5c3ac-1458">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1458">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="5c3ac-1459">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1459">General</span></span>
* <span data-ttu-id="5c3ac-1460">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1460">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="5c3ac-1461">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1461">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="5c3ac-1462">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1462">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](/azure-stack/operator/powershell-install-az-module)</span></span>
* <span data-ttu-id="5c3ac-1463">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1463">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="5c3ac-1464">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1464">Az.Billing</span></span>
  - <span data-ttu-id="5c3ac-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1465">Az.Compute</span></span>
  - <span data-ttu-id="5c3ac-1466">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1466">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="5c3ac-1467">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1467">Az.EventHub</span></span>
  - <span data-ttu-id="5c3ac-1468">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1468">Az.IotHub</span></span>
  - <span data-ttu-id="5c3ac-1469">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1469">Az.KeyVault</span></span>
  - <span data-ttu-id="5c3ac-1470">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1470">Az.Monitor</span></span>
  - <span data-ttu-id="5c3ac-1471">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1471">Az.Network</span></span>
  - <span data-ttu-id="5c3ac-1472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1472">Az.Resources</span></span>
  - <span data-ttu-id="5c3ac-1473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1473">Az.Storage</span></span>
  - <span data-ttu-id="5c3ac-1474">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1474">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-1475">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1475">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-1476">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1476">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="5c3ac-1477">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](/azure-stack/operator/powershell-install-az-module)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1477">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](/azure-stack/operator/powershell-install-az-module)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="5c3ac-1478">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1478">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1479">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1479">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1480">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1480">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1481">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1482">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1482">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="5c3ac-1483">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1483">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="5c3ac-1484">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1484">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-1485">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1485">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="5c3ac-1486">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1486">[#11354]</span></span>
* <span data-ttu-id="5c3ac-1487">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1487">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="5c3ac-1488">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1488">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="5c3ac-1489">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1489">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="5c3ac-1490">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1490">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="5c3ac-1491">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1491">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="5c3ac-1492">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1492">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="5c3ac-1493">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1493">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="5c3ac-1494">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1494">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="5c3ac-1495">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1495">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1496">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1496">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1497">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1497">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="5c3ac-1498">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1498">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-1499">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1499">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-1500">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1500">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="5c3ac-1501">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1501">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-1502">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1502">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-1503">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1503">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-1504">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1504">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-1505">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1505">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="5c3ac-1506">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1506">New Cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1507">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1507">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="5c3ac-1508">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1508">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1509">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-1510">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1510">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-1511">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1511">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-1512">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1512">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1513">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1513">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1514">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1514">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="5c3ac-1515">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1515">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5c3ac-1516">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1516">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="5c3ac-1517">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1517">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="5c3ac-1518">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1518">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="5c3ac-1519">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1519">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-1520">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1520">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-1521">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1521">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1522">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1522">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1523">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1523">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="5c3ac-1524">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1524">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="5c3ac-1525">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1525">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="5c3ac-1526">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1526">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="5c3ac-1527">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1527">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="5c3ac-1528">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1528">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1529">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1529">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1530">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1530">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="5c3ac-1531">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1531">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="5c3ac-1532">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1532">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="5c3ac-1533">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1533">Added example.</span></span>
* <span data-ttu-id="5c3ac-1534">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1534">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="5c3ac-1535">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1535">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1536">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1537">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1537">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="5c3ac-1538">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1538">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="5c3ac-1539">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1539">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="5c3ac-1540">Az.Support</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1540">Az.Support</span></span>
* <span data-ttu-id="5c3ac-1541">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1541">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-1542">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1542">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-1543">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1543">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="5c3ac-1544">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1544">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="5c3ac-1545">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1545">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="5c3ac-1546">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1546">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="5c3ac-1547">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1547">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="5c3ac-1548">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1548">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1549">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1550">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1550">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="5c3ac-1551">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1551">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="5c3ac-1552">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1552">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-1553">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1553">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-1554">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1554">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="5c3ac-1555">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1555">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="5c3ac-1556">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1556">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="5c3ac-1557">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1557">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-1558">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1558">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-1559">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1559">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-1560">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1560">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-1561">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1561">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="5c3ac-1562">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1562">New Cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1563">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1563">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5c3ac-1564">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1564">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5c3ac-1565">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1565">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5c3ac-1566">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1566">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="5c3ac-1567">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1567">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="5c3ac-1568">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1568">New Cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1569">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1569">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="5c3ac-1570">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1570">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="5c3ac-1571">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1571">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="5c3ac-1572">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1572">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="5c3ac-1573">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1573">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="5c3ac-1574">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1574">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="5c3ac-1575">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1575">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="5c3ac-1576">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1576">New Cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1577">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1577">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="5c3ac-1578">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1578">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="5c3ac-1579">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1579">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-1580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1580">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-1581">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1581">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1582">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1582">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1583">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1583">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="5c3ac-1584">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1584">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="5c3ac-1585">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1585">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="5c3ac-1586">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1586">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1587">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1587">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1588">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1588">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="5c3ac-1589">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1589">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="5c3ac-1590">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1590">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="5c3ac-1591">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1591">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="5c3ac-1592">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1592">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="5c3ac-1593">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1593">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="5c3ac-1594">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1594">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="5c3ac-1595">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1595">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="5c3ac-1596">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1596">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="5c3ac-1597">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1597">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="5c3ac-1598">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1598">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="5c3ac-1599">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1599">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="5c3ac-1600">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1600">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="5c3ac-1601">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1601">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1602">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1603">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1603">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="5c3ac-1604">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1604">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="5c3ac-1605">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1605">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="5c3ac-1606">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1606">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="5c3ac-1607">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1607">Remove an LTR backup</span></span>
    - <span data-ttu-id="5c3ac-1608">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1608">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="5c3ac-1609">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1609">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="5c3ac-1610">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1610">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="5c3ac-1611">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1611">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1612">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1612">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1613">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1613">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="5c3ac-1614">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1614">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="5c3ac-1615">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1615">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="5c3ac-1616">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1616">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="5c3ac-1617">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1617">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-1618">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1618">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-1619">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1619">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="5c3ac-1620">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1620">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="5c3ac-1621">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1621">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="5c3ac-1622">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1622">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="5c3ac-1623">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1623">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="5c3ac-1624">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1624">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c3ac-1625">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1625">Highlights since the last major release</span></span>
* <span data-ttu-id="5c3ac-1626">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1626">Updated client side telemetry.</span></span>
* <span data-ttu-id="5c3ac-1627">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1627">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="5c3ac-1628">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1628">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1629">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1629">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1630">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1630">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-1631">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1631">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-1632">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1632">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-1633">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1633">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-1634">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1634">Updated SDK to 7.0</span></span>
* <span data-ttu-id="5c3ac-1635">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1635">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1636">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1636">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1637">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1637">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-1638">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1638">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-1639">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1639">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-1640">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1640">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-1641">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1641">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="5c3ac-1642">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1642">New Cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-1643">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1643">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5c3ac-1644">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1644">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5c3ac-1645">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1645">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="5c3ac-1646">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1646">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-1647">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1647">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-1648">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1648">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-1649">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1649">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-1650">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1650">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="5c3ac-1651">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1651">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="5c3ac-1652">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1652">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1653">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1653">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1654">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1654">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-1655">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1655">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="5c3ac-1656">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1656">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="5c3ac-1657">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1657">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="5c3ac-1658">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1658">No new cmdlets are added.</span></span> <span data-ttu-id="5c3ac-1659">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1659">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1660">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1661">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1661">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1662">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1663">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1663">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="5c3ac-1664">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1664">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="5c3ac-1665">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1665">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="5c3ac-1666">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1666">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="5c3ac-1667">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1667">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="5c3ac-1668">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1668">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="5c3ac-1669">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1669">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="5c3ac-1670">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1670">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1671">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1671">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1672">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1672">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="5c3ac-1673">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1673">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="5c3ac-1674">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1674">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="5c3ac-1675">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1675">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="5c3ac-1676">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1676">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c3ac-1677">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1677">Az.StorageSync</span></span>
* <span data-ttu-id="5c3ac-1678">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1678">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="5c3ac-1679">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1679">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c3ac-1680">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1680">Highlights since the last major release</span></span>
* <span data-ttu-id="5c3ac-1681">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1681">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="5c3ac-1682">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1682">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1683">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1683">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1684">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1684">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="5c3ac-1685">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1685">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-1686">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1686">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-1687">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1687">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="5c3ac-1688">**New-AzApiManagementProduct** _ e _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1688">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="5c3ac-1689">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1689">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="5c3ac-1690">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1690">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1691">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1691">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1692">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1692">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="5c3ac-1693">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1693">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="5c3ac-1694">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1694">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="5c3ac-1695">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1695">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="5c3ac-1696">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1696">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1697">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1698">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1698">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5c3ac-1699">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1699">Az.DeploymentManager</span></span>
* <span data-ttu-id="5c3ac-1700">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1700">Adds LIST operations for resources</span></span>
* <span data-ttu-id="5c3ac-1701">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1701">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-1702">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1702">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-1703">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1703">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-1704">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1704">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-1705">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1705">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1706">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1706">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1707">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1707">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="5c3ac-1708">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1708">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="5c3ac-1709">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1709">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-1710">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1710">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="5c3ac-1711">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1711">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="5c3ac-1712">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1712">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="5c3ac-1713">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1713">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="5c3ac-1714">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1714">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="5c3ac-1715">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1715">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1716">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="5c3ac-1717">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1717">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="5c3ac-1718">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1718">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="5c3ac-1719">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1719">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-1720">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1720">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-1721">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1721">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="5c3ac-1722">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1722">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="5c3ac-1723">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1723">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="5c3ac-1724">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1724">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1725">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1725">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1726">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1726">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="5c3ac-1727">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1727">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1728">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1729">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1729">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="5c3ac-1730">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1730">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1731">Az.Sql</span></span>
<span data-ttu-id="5c3ac-1732">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1732">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1733">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1734">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1734">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="5c3ac-1735">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1735">New-AzStorageAccount</span></span>
* <span data-ttu-id="5c3ac-1736">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1736">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="5c3ac-1737">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1737">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-1738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1738">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-1739">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1739">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="5c3ac-1740">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1740">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="5c3ac-1741">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1741">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1742">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1743">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1743">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-1744">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1744">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-1745">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1745">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1746">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1746">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1747">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1747">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="5c3ac-1748">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1748">Az.ContainerInstance</span></span>
* <span data-ttu-id="5c3ac-1749">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1749">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="5c3ac-1750">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1750">Az.DataBoxEdge</span></span>
* <span data-ttu-id="5c3ac-1751">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1751">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5c3ac-1752">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1752">Get the Edge Storage Container</span></span>
* <span data-ttu-id="5c3ac-1753">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1753">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5c3ac-1754">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1754">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="5c3ac-1755">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1755">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5c3ac-1756">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1756">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="5c3ac-1757">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1757">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="5c3ac-1758">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1758">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="5c3ac-1759">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1759">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="5c3ac-1760">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1760">Get the Edge Storage Account</span></span>
* <span data-ttu-id="5c3ac-1761">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1761">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="5c3ac-1762">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1762">Create new Edge Storage Account</span></span>
* <span data-ttu-id="5c3ac-1763">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1763">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="5c3ac-1764">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1764">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="5c3ac-1765">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1765">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="5c3ac-1766">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1766">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="5c3ac-1767">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1767">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="5c3ac-1768">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1768">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1769">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1769">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1770">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1770">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="5c3ac-1771">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1771">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="5c3ac-1772">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1772">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="5c3ac-1773">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1773">Az.DevTestLabs</span></span>
* <span data-ttu-id="5c3ac-1774">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1774">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-1775">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1775">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-1776">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1776">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-1777">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1777">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-1778">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1778">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5c3ac-1779">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1779">Az.MachineLearning</span></span>
* <span data-ttu-id="5c3ac-1780">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1780">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="5c3ac-1781">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1781">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="5c3ac-1782">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1782">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="5c3ac-1783">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1783">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="5c3ac-1784">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1784">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="5c3ac-1785">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1785">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="5c3ac-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1786">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="5c3ac-1787">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1787">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1788">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1788">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1789">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1789">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1791">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1791">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="5c3ac-1792">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1792">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="5c3ac-1793">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1793">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="5c3ac-1794">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1794">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1795">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1796">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1796">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1797">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1798">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1798">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="5c3ac-1799">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1799">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="5c3ac-1800">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1800">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="5c3ac-1801">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1801">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1802">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1803">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1803">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="5c3ac-1804">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1804">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="5c3ac-1805">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1805">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="5c3ac-1806">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1806">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="5c3ac-1807">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1807">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="5c3ac-1808">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1808">General</span></span>
* <span data-ttu-id="5c3ac-1809">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1809">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1810">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1810">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1811">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1811">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="5c3ac-1812">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1812">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c3ac-1813">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1813">Az.Batch</span></span>
* <span data-ttu-id="5c3ac-1814">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1814">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1815">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1815">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1816">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1816">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-1817">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1817">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-1818">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1818">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="5c3ac-1819">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1819">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5c3ac-1820">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1820">Az.HealthcareApis</span></span>
* <span data-ttu-id="5c3ac-1821">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1821">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-1822">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1822">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-1823">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1823">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="5c3ac-1824">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1824">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="5c3ac-1825">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1825">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-1826">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1826">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-1827">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1827">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="5c3ac-1828">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1828">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="5c3ac-1829">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1829">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1830">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1831">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1831">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1832">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-1833">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1833">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="5c3ac-1834">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1834">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1835">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1836">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1836">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-1837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1837">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-1838">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1838">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="5c3ac-1839">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1839">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="5c3ac-1840">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1840">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="5c3ac-1841">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1841">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="5c3ac-1842">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1842">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="5c3ac-1843">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1843">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="5c3ac-1844">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1844">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="5c3ac-1845">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1845">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="5c3ac-1846">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1846">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="5c3ac-1847">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1847">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="5c3ac-1848">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1848">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="5c3ac-1849">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1849">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="5c3ac-1850">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1850">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="5c3ac-1851">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1851">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c3ac-1852">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1852">Highlights since the last major release</span></span>
* <span data-ttu-id="5c3ac-1853">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1853">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="5c3ac-1854">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1854">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1855">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1856">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1856">VM Reapply feature</span></span>
    - <span data-ttu-id="5c3ac-1857">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1857">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="5c3ac-1858">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1858">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="5c3ac-1859">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1859">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="5c3ac-1860">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1860">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="5c3ac-1861">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1861">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5c3ac-1862">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1862">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="5c3ac-1863">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1863">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="5c3ac-1864">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1864">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="5c3ac-1865">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1865">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="5c3ac-1866">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1866">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="5c3ac-1867">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1867">Az.DataBoxEdge</span></span>
* <span data-ttu-id="5c3ac-1868">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1868">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5c3ac-1869">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1869">Get the Order</span></span>
* <span data-ttu-id="5c3ac-1870">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1870">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5c3ac-1871">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1871">Create new Order</span></span>
* <span data-ttu-id="5c3ac-1872">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1872">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="5c3ac-1873">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1873">Remove the Order</span></span>
* <span data-ttu-id="5c3ac-1874">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1874">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="5c3ac-1875">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1875">Now creates Local Share</span></span>
* <span data-ttu-id="5c3ac-1876">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1876">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="5c3ac-1877">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1877">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="5c3ac-1878">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1878">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="5c3ac-1879">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1879">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="5c3ac-1880">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1880">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5c3ac-1881">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1881">Gets the information about Triggers</span></span>
* <span data-ttu-id="5c3ac-1882">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1882">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5c3ac-1883">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1883">Create new Triggers</span></span>
* <span data-ttu-id="5c3ac-1884">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1884">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="5c3ac-1885">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1885">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1886">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1886">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1887">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1887">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="5c3ac-1888">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1888">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-1889">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1889">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-1890">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1890">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-1891">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1891">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-1892">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1892">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-1893">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1893">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-1894">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1894">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="5c3ac-1895">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1895">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="5c3ac-1896">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1896">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="5c3ac-1897">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1897">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-1898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1898">Az.Network</span></span>
* <span data-ttu-id="5c3ac-1899">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1899">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="5c3ac-1900">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1900">Az.PrivateDns</span></span>
* <span data-ttu-id="5c3ac-1901">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1901">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-1902">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1902">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-1903">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1903">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="5c3ac-1904">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1904">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="5c3ac-1905">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1905">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c3ac-1906">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1906">Az.RedisCache</span></span>
* <span data-ttu-id="5c3ac-1907">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1907">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="5c3ac-1908">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1908">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="5c3ac-1909">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1909">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-1910">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1910">Az.Resources</span></span>
- <span data-ttu-id="5c3ac-1911">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1911">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="5c3ac-1912">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1912">Updated create policy definition help example</span></span>
- <span data-ttu-id="5c3ac-1913">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1913">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="5c3ac-1914">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1914">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="5c3ac-1915">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1915">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-1916">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1916">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-1917">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1917">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="5c3ac-1918">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1918">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="5c3ac-1919">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1919">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="5c3ac-1920">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1920">General</span></span>
* <span data-ttu-id="5c3ac-1921">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1921">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-1922">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1922">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-1923">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1923">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5c3ac-1924">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1924">Az.Advisor</span></span>
* <span data-ttu-id="5c3ac-1925">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1925">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c3ac-1926">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1926">Az.Batch</span></span>
* <span data-ttu-id="5c3ac-1927">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1927">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="5c3ac-1928">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1928">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="5c3ac-1929">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1929">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="5c3ac-1930">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1930">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="5c3ac-1931">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1931">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="5c3ac-1932">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1932">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="5c3ac-1933">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1933">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="5c3ac-1934">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1934">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="5c3ac-1935">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1935">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="5c3ac-1936">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1936">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5c3ac-1937">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1937">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="5c3ac-1938">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1938">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="5c3ac-1939">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1939">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="5c3ac-1940">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1940">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="5c3ac-1941">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1941">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="5c3ac-1942">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1942">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="5c3ac-1943">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1943">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="5c3ac-1944">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1944">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="5c3ac-1945">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1945">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="5c3ac-1946">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1946">This operation is no longer supported.</span></span>
* <span data-ttu-id="5c3ac-1947">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1947">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5c3ac-1948">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1948">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="5c3ac-1949">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1949">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="5c3ac-1950">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1950">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="5c3ac-1951">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1951">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="5c3ac-1952">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1952">New non-verified images are also now returned.</span></span> <span data-ttu-id="5c3ac-1953">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1953">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="5c3ac-1954">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1954">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="5c3ac-1955">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1955">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="5c3ac-1956">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1956">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="5c3ac-1957">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1957">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="5c3ac-1958">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1958">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="5c3ac-1959">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1959">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="5c3ac-1960">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1960">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="5c3ac-1961">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1961">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="5c3ac-1962">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1962">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-1963">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1963">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-1964">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1964">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="5c3ac-1965">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1965">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1966">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-1967">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1967">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="5c3ac-1968">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1968">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="5c3ac-1969">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1969">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="5c3ac-1970">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1970">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5c3ac-1971">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1971">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="5c3ac-1972">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1972">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="5c3ac-1973">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1973">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="5c3ac-1974">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1974">Breaking changes</span></span>
    - <span data-ttu-id="5c3ac-1975">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1975">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="5c3ac-1976">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1976">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-1977">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1977">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-1978">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1978">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-1979">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1979">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-1980">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1980">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="5c3ac-1981">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1981">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="5c3ac-1982">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1982">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="5c3ac-1983">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1983">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="5c3ac-1984">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1984">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="5c3ac-1985">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1985">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-1986">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1986">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-1987">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1987">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-1988">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1988">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-1989">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1989">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="5c3ac-1990">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1990">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="5c3ac-1991">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1991">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="5c3ac-1992">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1992">Removed five cmdlets:</span></span>
    - <span data-ttu-id="5c3ac-1993">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1993">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5c3ac-1994">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1994">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5c3ac-1995">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1995">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="5c3ac-1996">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1996">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="5c3ac-1997">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1997">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="5c3ac-1998">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1998">Added three cmdlets:</span></span>
    - <span data-ttu-id="5c3ac-1999">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-1999">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5c3ac-2000">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2000">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="5c3ac-2001">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2001">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="5c3ac-2002">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2002">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="5c3ac-2003">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2003">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="5c3ac-2004">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2004">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="5c3ac-2005">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2005">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="5c3ac-2006">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2006">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="5c3ac-2007">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2007">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="5c3ac-2008">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2008">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="5c3ac-2009">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2009">Added some scenario test cases.</span></span>
* <span data-ttu-id="5c3ac-2010">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2010">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-2011">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2011">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-2012">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2012">Breaking changes:</span></span>
    - <span data-ttu-id="5c3ac-2013">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2013">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5c3ac-2014">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2014">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5c3ac-2015">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2015">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5c3ac-2016">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2016">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5c3ac-2017">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2017">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="5c3ac-2018">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2018">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="5c3ac-2019">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2019">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="5c3ac-2020">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2020">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="5c3ac-2021">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2021">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5c3ac-2022">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2022">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="5c3ac-2023">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2023">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="5c3ac-2024">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2024">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2025">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2026">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2026">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="5c3ac-2027">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2027">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="5c3ac-2028">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2028">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="5c3ac-2029">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2029">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="5c3ac-2030">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2030">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="5c3ac-2031">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2031">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="5c3ac-2032">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2032">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="5c3ac-2033">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2033">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="5c3ac-2034">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2034">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2035">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2035">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-2036">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2036">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2037">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2037">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2038">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2038">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="5c3ac-2039">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2039">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-2040">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2040">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2041">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2041">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2042">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2042">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2043">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2043">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2044">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2044">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5c3ac-2045">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2045">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="5c3ac-2046">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2046">New cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-2047">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2047">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="5c3ac-2048">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2048">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="5c3ac-2049">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2049">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="5c3ac-2050">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2050">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="5c3ac-2051">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2051">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="5c3ac-2052">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2052">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="5c3ac-2053">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2053">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="5c3ac-2054">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2054">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="5c3ac-2055">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2055">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-2056">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2056">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="5c3ac-2057">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2057">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5c3ac-2058">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2058">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5c3ac-2059">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2059">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="5c3ac-2060">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2060">Set-AzVirtualHub</span></span>
* <span data-ttu-id="5c3ac-2061">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2061">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="5c3ac-2062">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2062">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5c3ac-2063">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2063">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5c3ac-2064">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2064">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="5c3ac-2065">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2065">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="5c3ac-2066">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2066">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="5c3ac-2067">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2067">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="5c3ac-2068">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2068">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-2069">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2069">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="5c3ac-2070">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2070">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5c3ac-2071">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2071">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5c3ac-2072">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2072">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5c3ac-2073">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2073">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5c3ac-2074">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2074">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="5c3ac-2075">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2075">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="5c3ac-2076">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2076">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="5c3ac-2077">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2077">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-2078">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2078">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="5c3ac-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2079">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="5c3ac-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2080">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="5c3ac-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2081">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="5c3ac-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2082">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="5c3ac-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2083">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="5c3ac-2084">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2084">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5c3ac-2085">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2085">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="5c3ac-2086">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2086">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="5c3ac-2087">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2087">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="5c3ac-2088">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2088">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="5c3ac-2089">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2089">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="5c3ac-2090">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2090">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="5c3ac-2091">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2091">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="5c3ac-2092">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2092">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="5c3ac-2093">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2093">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="5c3ac-2094">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2094">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="5c3ac-2095">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2095">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-2096">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2096">New-AzIpGroup</span></span>
        - <span data-ttu-id="5c3ac-2097">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2097">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="5c3ac-2098">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2098">Get-AzIpGroup</span></span>
        - <span data-ttu-id="5c3ac-2099">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2099">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-2100">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2100">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-2101">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2101">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2102">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2102">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2103">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2103">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="5c3ac-2104">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2104">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="5c3ac-2105">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2105">Removed deprecated aliases:</span></span>
* <span data-ttu-id="5c3ac-2106">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2106">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="5c3ac-2107">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2107">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="5c3ac-2108">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2108">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5c3ac-2109">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2109">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="5c3ac-2110">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2110">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="5c3ac-2111">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2111">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2112">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2112">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2113">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2113">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="5c3ac-2114">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2114">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5c3ac-2115">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2115">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5c3ac-2116">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2116">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="5c3ac-2117">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2117">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="5c3ac-2118">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2118">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="5c3ac-2119">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2119">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="5c3ac-2120">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2120">General</span></span>
* <span data-ttu-id="5c3ac-2121">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2121">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2122">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2122">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2123">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2123">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-2124">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2124">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-2125">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2125">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="5c3ac-2126">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2126">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-2127">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2127">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2128">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2128">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c3ac-2129">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2129">Az.Batch</span></span>
* <span data-ttu-id="5c3ac-2130">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2130">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2131">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2131">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2132">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2132">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="5c3ac-2133">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2133">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="5c3ac-2134">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2134">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="5c3ac-2135">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2135">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-2136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2136">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-2137">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2137">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="5c3ac-2138">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2138">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="5c3ac-2139">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2139">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-2140">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2140">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-2141">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2141">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="5c3ac-2142">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2142">Az.HealthcareApis</span></span>
* <span data-ttu-id="5c3ac-2143">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2143">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="5c3ac-2144">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2144">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="5c3ac-2145">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2145">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="5c3ac-2146">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2146">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-2147">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2147">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-2148">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2148">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="5c3ac-2149">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2149">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-2150">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2150">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-2151">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2151">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="5c3ac-2152">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2152">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="5c3ac-2153">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2153">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="5c3ac-2154">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2154">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2155">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2156">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2156">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="5c3ac-2157">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2157">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="5c3ac-2158">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2158">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-2159">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2159">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="5c3ac-2160">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2160">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5c3ac-2161">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2161">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="5c3ac-2162">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2162">Updated cmdlets:</span></span>
        - <span data-ttu-id="5c3ac-2163">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2163">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c3ac-2164">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2164">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c3ac-2165">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2165">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5c3ac-2166">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2166">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="5c3ac-2167">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2167">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="5c3ac-2168">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2168">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="5c3ac-2169">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2169">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c3ac-2170">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2170">Az.RedisCache</span></span>
* <span data-ttu-id="5c3ac-2171">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2171">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2172">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2172">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2173">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2173">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2174">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2174">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2175">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2175">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="5c3ac-2176">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2176">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5c3ac-2177">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2177">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="5c3ac-2178">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2178">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="5c3ac-2179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2179">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c3ac-2180">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2180">Az.StorageSync</span></span>
* <span data-ttu-id="5c3ac-2181">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2181">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2182">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2182">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2183">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2183">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="5c3ac-2184">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2184">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-2185">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2185">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-2186">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2186">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="5c3ac-2187">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2187">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="5c3ac-2188">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2188">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-2189">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2189">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2190">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2190">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="5c3ac-2191">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2191">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="5c3ac-2192">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2192">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2193">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2193">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2194">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2194">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="5c3ac-2195">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2195">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5c3ac-2196">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2196">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="5c3ac-2197">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2197">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="5c3ac-2198">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2198">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="5c3ac-2199">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2199">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="5c3ac-2200">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2200">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="5c3ac-2201">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2201">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="5c3ac-2202">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2202">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-2203">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2203">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-2204">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2204">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="5c3ac-2205">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2205">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-2206">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2206">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-2207">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2207">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-2208">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2208">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-2209">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2209">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="5c3ac-2210">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2210">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="5c3ac-2211">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2211">New cmdlets are:</span></span>
    - <span data-ttu-id="5c3ac-2212">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2212">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5c3ac-2213">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2213">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5c3ac-2214">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2214">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="5c3ac-2215">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2215">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-2216">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2216">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-2217">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2217">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="5c3ac-2218">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2218">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="5c3ac-2219">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2219">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="5c3ac-2220">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2220">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="5c3ac-2221">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2221">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="5c3ac-2222">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2222">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="5c3ac-2223">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2223">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="5c3ac-2224">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2224">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="5c3ac-2225">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2225">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5c3ac-2226">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2226">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="5c3ac-2227">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2227">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="5c3ac-2228">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2228">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="5c3ac-2229">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2229">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="5c3ac-2230">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2230">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="5c3ac-2231">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2231">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="5c3ac-2232">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2232">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="5c3ac-2233">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2233">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="5c3ac-2234">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2234">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="5c3ac-2235">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2235">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="5c3ac-2236">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2236">Overall improved help files</span></span>
* <span data-ttu-id="5c3ac-2237">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2237">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2238">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2238">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2239">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2239">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="5c3ac-2240">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2240">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="5c3ac-2241">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2241">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="5c3ac-2242">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2242">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="5c3ac-2243">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2243">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="5c3ac-2244">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2244">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="5c3ac-2245">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2245">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="5c3ac-2246">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2246">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="5c3ac-2247">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2247">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="5c3ac-2248">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2248">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="5c3ac-2249">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2249">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="5c3ac-2250">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2250">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="5c3ac-2251">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2251">New cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2252">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2252">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="5c3ac-2253">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2253">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="5c3ac-2254">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2254">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-2255">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2255">New-VpnSite</span></span>
        - <span data-ttu-id="5c3ac-2256">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2256">Update-VpnSite</span></span>
        - <span data-ttu-id="5c3ac-2257">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2257">New-VpnConnection</span></span>
        - <span data-ttu-id="5c3ac-2258">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2258">Update-VpnConnection</span></span>
* <span data-ttu-id="5c3ac-2259">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2259">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2260">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2260">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2261">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2261">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="5c3ac-2262">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2262">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2263">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2263">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-2264">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2264">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-2265">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2265">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-2266">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2266">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="5c3ac-2267">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2267">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="5c3ac-2268">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2268">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c3ac-2269">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2269">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5c3ac-2270">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2270">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5c3ac-2271">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2271">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="5c3ac-2272">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2272">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c3ac-2273">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2273">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c3ac-2274">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2274">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5c3ac-2275">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2275">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5c3ac-2276">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2276">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="5c3ac-2277">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2277">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="5c3ac-2278">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2278">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="5c3ac-2279">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2279">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="5c3ac-2280">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2280">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="5c3ac-2281">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2281">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c3ac-2282">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2282">Az.SignalR</span></span>
* <span data-ttu-id="5c3ac-2283">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2283">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2284">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2284">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2285">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2285">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="5c3ac-2286">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2286">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="5c3ac-2287">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2287">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="5c3ac-2288">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2288">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="5c3ac-2289">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2289">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2290">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2290">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2291">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2291">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="5c3ac-2292">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2292">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="5c3ac-2293">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2293">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="5c3ac-2294">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2294">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="5c3ac-2295">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2295">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="5c3ac-2296">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2296">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="5c3ac-2297">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2297">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="5c3ac-2298">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2298">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5c3ac-2299">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2299">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5c3ac-2300">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2300">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="5c3ac-2301">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2301">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2302">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2302">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2303">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2303">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="5c3ac-2304">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2304">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="5c3ac-2305">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2305">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="5c3ac-2306">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2306">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="5c3ac-2307">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2307">General</span></span>
* <span data-ttu-id="5c3ac-2308">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2308">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2309">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2310">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2310">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-2311">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2311">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-2312">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2312">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="5c3ac-2313">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2313">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-2314">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2314">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-2315">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2315">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="5c3ac-2316">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2316">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="5c3ac-2317">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2317">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="5c3ac-2318">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2318">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="5c3ac-2319">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2319">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c3ac-2320">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2320">Az.Batch</span></span>
* <span data-ttu-id="5c3ac-2321">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2321">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-2322">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2322">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-2323">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2323">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2324">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2325">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2325">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="5c3ac-2326">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2326">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="5c3ac-2327">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2327">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="5c3ac-2328">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2328">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="5c3ac-2329">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2329">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="5c3ac-2330">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2330">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="5c3ac-2331">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2331">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="5c3ac-2332">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2332">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-2333">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2333">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-2334">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2334">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="5c3ac-2335">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2335">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="5c3ac-2336">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2336">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="5c3ac-2337">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2337">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-2338">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2338">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-2339">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2339">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-2340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2340">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-2341">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2341">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="5c3ac-2342">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2342">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="5c3ac-2343">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2343">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="5c3ac-2344">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2344">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="5c3ac-2345">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2345">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5c3ac-2346">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2346">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-2347">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2347">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-2348">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2348">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2349">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2349">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2350">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2350">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="5c3ac-2351">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2351">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="5c3ac-2352">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2352">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="5c3ac-2353">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2353">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="5c3ac-2354">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2354">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="5c3ac-2355">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2355">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="5c3ac-2356">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2356">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-2357">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2357">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-2358">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2358">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="5c3ac-2359">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2359">Added example</span></span>
    - <span data-ttu-id="5c3ac-2360">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2360">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="5c3ac-2361">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2361">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="5c3ac-2362">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2362">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2363">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2363">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2364">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2364">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2365">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2365">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-2366">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2366">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="5c3ac-2367">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2367">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="5c3ac-2368">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2368">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="5c3ac-2369">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2369">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c3ac-2370">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2370">Az.ServiceBus</span></span>
* <span data-ttu-id="5c3ac-2371">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2371">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="5c3ac-2372">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2372">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="5c3ac-2373">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2373">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-2374">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2374">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-2375">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2375">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="5c3ac-2376">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2376">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="5c3ac-2377">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2377">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="5c3ac-2378">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2378">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="5c3ac-2379">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2379">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="5c3ac-2380">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2380">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2381">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2382">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2382">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2383">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2383">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2384">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2384">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="5c3ac-2385">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2385">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="5c3ac-2386">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2386">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="5c3ac-2387">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2387">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="5c3ac-2388">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2388">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="5c3ac-2389">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2389">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2390">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2390">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2391">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2391">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="5c3ac-2392">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2392">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2393">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2393">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2394">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2394">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="5c3ac-2395">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2395">Az.ApplicationInsights</span></span>
* <span data-ttu-id="5c3ac-2396">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2396">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-2397">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2397">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2398">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2398">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-2399">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2399">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-2400">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2400">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2401">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2401">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2402">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2402">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5c3ac-2403">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2403">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5c3ac-2404">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2404">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="5c3ac-2405">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2405">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-2406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2406">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-2407">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2407">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="5c3ac-2408">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2408">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-2409">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2409">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-2410">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2410">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5c3ac-2411">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2411">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-2412">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2412">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-2413">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2413">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c3ac-2414">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2414">Az.LogicApp</span></span>
* <span data-ttu-id="5c3ac-2415">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2415">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="5c3ac-2416">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2416">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="5c3ac-2417">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2417">Az.ManagedServices</span></span>
* <span data-ttu-id="5c3ac-2418">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2418">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2419">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2419">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2420">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2420">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="5c3ac-2421">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2421">New cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2422">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2422">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c3ac-2423">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2423">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5c3ac-2424">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2424">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2425">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2425">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2426">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2426">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2427">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2427">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="5c3ac-2428">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2428">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="5c3ac-2429">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2429">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="5c3ac-2430">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2430">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="5c3ac-2431">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2431">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="5c3ac-2432">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2432">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="5c3ac-2433">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2433">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="5c3ac-2434">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2434">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="5c3ac-2435">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2435">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="5c3ac-2436">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2436">Updated cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2437">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2437">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c3ac-2438">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2438">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="5c3ac-2439">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2439">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="5c3ac-2440">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2440">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="5c3ac-2441">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2441">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="5c3ac-2442">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2442">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-2443">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2443">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5c3ac-2444">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2444">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="5c3ac-2445">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2445">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="5c3ac-2446">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2446">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="5c3ac-2447">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2447">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="5c3ac-2448">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2448">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-2449">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2449">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-2450">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2450">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="5c3ac-2451">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2451">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2452">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2452">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2453">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2453">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5c3ac-2454">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2454">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="5c3ac-2455">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2455">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="5c3ac-2456">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2456">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="5c3ac-2457">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2457">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="5c3ac-2458">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2458">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5c3ac-2459">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2459">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="5c3ac-2460">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2460">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="5c3ac-2461">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2461">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="5c3ac-2462">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2462">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2463">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2463">Az.Resources</span></span>
- <span data-ttu-id="5c3ac-2464">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2464">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="5c3ac-2465">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2465">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c3ac-2466">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2466">Az.ServiceBus</span></span>
* <span data-ttu-id="5c3ac-2467">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2467">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="5c3ac-2468">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2468">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2469">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2470">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2470">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="5c3ac-2471">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2471">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="5c3ac-2472">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2472">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2473">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2473">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2474">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2474">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c3ac-2475">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2475">Az.StorageSync</span></span>
* <span data-ttu-id="5c3ac-2476">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2476">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="5c3ac-2477">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2477">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2478">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2479">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2479">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="5c3ac-2480">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2480">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="5c3ac-2481">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2481">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="5c3ac-2482">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2482">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2483">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2484">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2484">Add support for profile cmdlets</span></span>
* <span data-ttu-id="5c3ac-2485">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2485">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="5c3ac-2486">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2486">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="5c3ac-2487">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2487">Az.Advisor</span></span>
* <span data-ttu-id="5c3ac-2488">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2488">GA release of Az.Advisor</span></span>
* <span data-ttu-id="5c3ac-2489">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2489">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-2490">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2490">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-2491">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2491">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="5c3ac-2492">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2492">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="5c3ac-2493">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2493">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="5c3ac-2494">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2494">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="5c3ac-2495">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2495">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="5c3ac-2496">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2496">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="5c3ac-2497">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2497">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-2498">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2498">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2499">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2499">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2500">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2501">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2501">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-2502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2502">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-2503">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2503">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c3ac-2504">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2504">Az.EventGrid</span></span>
* <span data-ttu-id="5c3ac-2505">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2505">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-2506">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2506">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-2507">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2507">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2508">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2508">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2509">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2509">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="5c3ac-2510">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2510">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-2511">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2511">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-2512">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2512">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="5c3ac-2513">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2513">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-2514">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2514">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-2515">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2515">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2516">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2516">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2517">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2517">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2518">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2518">Az.Resources</span></span>
    - <span data-ttu-id="5c3ac-2519">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2519">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="5c3ac-2520">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2520">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="5c3ac-2521">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2521">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="5c3ac-2522">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2522">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c3ac-2523">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2523">Az.ServiceBus</span></span>
* <span data-ttu-id="5c3ac-2524">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2524">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2525">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2526">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2526">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="5c3ac-2527">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2527">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="5c3ac-2528">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2528">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5c3ac-2529">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2529">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5c3ac-2530">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2530">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="5c3ac-2531">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2531">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5c3ac-2532">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2532">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="5c3ac-2533">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2533">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="5c3ac-2534">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2534">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2535">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2535">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2536">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2536">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="5c3ac-2537">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2537">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="5c3ac-2538">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2538">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="5c3ac-2539">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2539">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="5c3ac-2540">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2540">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="5c3ac-2541">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2541">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="5c3ac-2542">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2542">Set-AzStorageAccount</span></span>
* <span data-ttu-id="5c3ac-2543">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2543">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="5c3ac-2544">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2544">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="5c3ac-2545">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2545">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="5c3ac-2546">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2546">Az.StorageSync</span></span>
* <span data-ttu-id="5c3ac-2547">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2547">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="5c3ac-2548">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2548">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2549">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2549">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2550">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2550">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="5c3ac-2551">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2551">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="5c3ac-2552">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2552">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="5c3ac-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2553">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="5c3ac-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2554">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2555">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2555">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2556">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2556">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="5c3ac-2557">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2557">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="5c3ac-2558">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2558">Az.Dns</span></span>
* <span data-ttu-id="5c3ac-2559">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2559">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c3ac-2560">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2560">Az.EventGrid</span></span>
* <span data-ttu-id="5c3ac-2561">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2561">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="5c3ac-2562">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2562">New cmdlets:</span></span>
    - <span data-ttu-id="5c3ac-2563">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2563">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5c3ac-2564">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2564">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5c3ac-2565">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2565">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5c3ac-2566">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2566">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="5c3ac-2567">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2567">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="5c3ac-2568">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2568">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5c3ac-2569">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2569">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5c3ac-2570">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2570">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="5c3ac-2571">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2571">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="5c3ac-2572">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2572">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="5c3ac-2573">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2573">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5c3ac-2574">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2574">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="5c3ac-2575">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2575">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="5c3ac-2576">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2576">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="5c3ac-2577">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2577">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="5c3ac-2578">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2578">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="5c3ac-2579">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2579">Updated cmdlets:</span></span>
    - <span data-ttu-id="5c3ac-2580">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2580">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="5c3ac-2581">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2581">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5c3ac-2582">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2582">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="5c3ac-2583">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2583">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="5c3ac-2584">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2584">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="5c3ac-2585">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2585">Event subscription expiration date,</span></span>
            - <span data-ttu-id="5c3ac-2586">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2586">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="5c3ac-2587">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2587">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="5c3ac-2588">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2588">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="5c3ac-2589">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2589">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="5c3ac-2590">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2590">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="5c3ac-2591">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2591">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="5c3ac-2592">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2592">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="5c3ac-2593">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2593">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-2594">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2594">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-2595">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2595">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="5c3ac-2596">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2596">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="5c3ac-2597">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2597">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="5c3ac-2598">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2598">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2599">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2599">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2600">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2600">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="5c3ac-2601">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2601">New cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2602">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="5c3ac-2603">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2603">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="5c3ac-2604">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2604">New cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2605">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2605">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="5c3ac-2606">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2606">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="5c3ac-2607">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2607">New cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2608">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2608">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5c3ac-2609">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2609">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5c3ac-2610">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2610">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="5c3ac-2611">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2611">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="5c3ac-2612">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2612">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="5c3ac-2613">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2613">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="5c3ac-2614">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2614">New cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2615">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2615">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c3ac-2616">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2616">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c3ac-2617">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2617">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="5c3ac-2618">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2618">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="5c3ac-2619">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2619">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="5c3ac-2620">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2620">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="5c3ac-2621">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2621">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="5c3ac-2622">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2622">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="5c3ac-2623">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2623">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="5c3ac-2624">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2624">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="5c3ac-2625">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2625">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="5c3ac-2626">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2626">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="5c3ac-2627">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2627">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="5c3ac-2628">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2628">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="5c3ac-2629">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2629">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="5c3ac-2630">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2630">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="5c3ac-2631">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2631">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="5c3ac-2632">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2632">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="5c3ac-2633">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2633">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-2634">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2634">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="5c3ac-2635">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2635">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="5c3ac-2636">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2636">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="5c3ac-2637">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2637">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="5c3ac-2638">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2638">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="5c3ac-2639">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2639">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5c3ac-2640">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2640">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="5c3ac-2641">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2641">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-2642">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2642">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-2643">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2643">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2644">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2644">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-2645">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2645">Support for additional Template Export options</span></span>
    - <span data-ttu-id="5c3ac-2646">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2646">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5c3ac-2647">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2647">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="5c3ac-2648">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2648">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-2649">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2649">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-2650">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2650">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2651">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2651">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2652">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2652">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="5c3ac-2653">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2653">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="5c3ac-2654">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2654">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="5c3ac-2655">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2655">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5c3ac-2656">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2656">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5c3ac-2657">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2657">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="5c3ac-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2658">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="5c3ac-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2659">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2660">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2660">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2661">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2661">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="5c3ac-2662">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2662">New-AzStorageAccount</span></span>
* <span data-ttu-id="5c3ac-2663">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2663">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="5c3ac-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2664">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2665">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2665">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2666">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2666">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="5c3ac-2667">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2667">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="5c3ac-2668">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2668">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="5c3ac-2669">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2669">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-2670">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2670">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2671">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2672">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2672">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="5c3ac-2673">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2673">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-2674">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2674">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-2675">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2675">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="5c3ac-2676">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2676">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2677">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2678">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2678">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="5c3ac-2679">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2679">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-2680">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2680">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-2681">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2681">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2682">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2682">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2683">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2683">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c3ac-2684">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2684">Az.ServiceBus</span></span>
* <span data-ttu-id="5c3ac-2685">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2685">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-2686">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2686">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-2687">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2687">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="5c3ac-2688">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2688">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2689">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2689">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2690">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2690">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="5c3ac-2691">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2691">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="5c3ac-2692">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2692">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="5c3ac-2693">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2693">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2694">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2694">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2695">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2695">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="5c3ac-2696">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2696">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-2697">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2697">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-2698">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2698">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="5c3ac-2699">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2699">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="5c3ac-2700">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2700">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="5c3ac-2701">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2701">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="5c3ac-2702">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2702">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="5c3ac-2703">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2703">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="5c3ac-2704">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2704">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="5c3ac-2705">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2705">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="5c3ac-2706">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2706">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="5c3ac-2707">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2707">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="5c3ac-2708">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2708">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="5c3ac-2709">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2709">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="5c3ac-2710">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2710">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="5c3ac-2711">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2711">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="5c3ac-2712">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2712">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="5c3ac-2713">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2713">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="5c3ac-2714">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2714">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="5c3ac-2715">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2715">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="5c3ac-2716">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2716">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="5c3ac-2717">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2717">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="5c3ac-2718">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2718">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="5c3ac-2719">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2719">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="5c3ac-2720">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2720">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="5c3ac-2721">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2721">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="5c3ac-2722">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2722">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="5c3ac-2723">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2723">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="5c3ac-2724">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2724">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="5c3ac-2725">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2725">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="5c3ac-2726">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2726">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="5c3ac-2727">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2727">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="5c3ac-2728">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2728">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="5c3ac-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2729">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="5c3ac-2730">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2730">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="5c3ac-2731">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2731">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5c3ac-2732">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2732">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="5c3ac-2733">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2733">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="5c3ac-2734">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2734">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="5c3ac-2735">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2735">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="5c3ac-2736">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2736">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="5c3ac-2737">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2737">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5c3ac-2738">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2738">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5c3ac-2739">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2739">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5c3ac-2740">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2740">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="5c3ac-2741">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2741">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="5c3ac-2742">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2742">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="5c3ac-2743">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2743">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="5c3ac-2744">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2744">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="5c3ac-2745">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2745">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="5c3ac-2746">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2746">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="5c3ac-2747">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2747">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="5c3ac-2748">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2748">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="5c3ac-2749">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2749">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="5c3ac-2750">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2750">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="5c3ac-2751">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2751">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="5c3ac-2752">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2752">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="5c3ac-2753">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2753">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="5c3ac-2754">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2754">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5c3ac-2755">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2755">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5c3ac-2756">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2756">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5c3ac-2757">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2757">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5c3ac-2758">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2758">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="5c3ac-2759">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2759">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="5c3ac-2760">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2760">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="5c3ac-2761">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2761">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="5c3ac-2762">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2762">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="5c3ac-2763">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2763">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="5c3ac-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2764">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="5c3ac-2765">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2765">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="5c3ac-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2766">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="5c3ac-2767">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2767">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="5c3ac-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2768">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="5c3ac-2769">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2769">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="5c3ac-2770">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2770">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="5c3ac-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2771">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="5c3ac-2772">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2772">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="5c3ac-2773">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2773">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="5c3ac-2774">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2774">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-2775">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2775">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2776">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2776">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="5c3ac-2777">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2777">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="5c3ac-2778">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2778">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="5c3ac-2779">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2779">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="5c3ac-2780">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2780">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="5c3ac-2781">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2781">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="5c3ac-2782">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2782">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2783">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2783">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2784">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2784">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="5c3ac-2785">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2785">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-2786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2786">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-2787">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2787">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-2788">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2788">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-2789">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2789">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2790">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2790">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2791">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2791">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="5c3ac-2792">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2792">Updated cmdlet:</span></span>
        - <span data-ttu-id="5c3ac-2793">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2793">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="5c3ac-2794">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2794">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2795">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-2796">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2796">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2797">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2797">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2798">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2798">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="5c3ac-2799">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2799">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2800">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2800">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2801">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2801">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-2802">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2802">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-2803">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2803">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="5c3ac-2804">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2804">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2805">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2806">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2806">Proximity placement group feature.</span></span>
    - <span data-ttu-id="5c3ac-2807">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2807">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="5c3ac-2808">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2808">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="5c3ac-2809">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2809">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="5c3ac-2810">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2810">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="5c3ac-2811">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2811">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="5c3ac-2812">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2812">Breaking changes</span></span>
    - <span data-ttu-id="5c3ac-2813">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2813">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="5c3ac-2814">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2814">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="5c3ac-2815">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2815">Az.DeploymentManager</span></span>
* <span data-ttu-id="5c3ac-2816">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2816">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="5c3ac-2817">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2817">Az.Dns</span></span>
* <span data-ttu-id="5c3ac-2818">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2818">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="5c3ac-2819">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2819">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="5c3ac-2820">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2820">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-2821">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2821">Az.FrontDoor</span></span>
* <span data-ttu-id="5c3ac-2822">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2822">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="5c3ac-2823">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2823">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-2824">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2824">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-2825">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2825">Removed two cmdlets:</span></span>
    - <span data-ttu-id="5c3ac-2826">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2826">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="5c3ac-2827">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2827">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5c3ac-2828">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2828">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="5c3ac-2829">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2829">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="5c3ac-2830">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2830">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="5c3ac-2831">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2831">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2832">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-2833">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2833">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="5c3ac-2834">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2834">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="5c3ac-2835">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2835">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="5c3ac-2836">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2836">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="5c3ac-2837">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2837">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="5c3ac-2838">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2838">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="5c3ac-2839">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2839">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="5c3ac-2840">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2840">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c3ac-2841">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2841">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c3ac-2842">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2842">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c3ac-2843">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2843">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c3ac-2844">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2844">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="5c3ac-2845">[Mais](/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2845">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="5c3ac-2846">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2846">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2847">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2847">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2848">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2848">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="5c3ac-2849">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2849">New cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2850">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2850">New-AzNatGateway</span></span>
        - <span data-ttu-id="5c3ac-2851">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2851">Get-AzNatGateway</span></span>
        - <span data-ttu-id="5c3ac-2852">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2852">Set-AzNatGateway</span></span>
        - <span data-ttu-id="5c3ac-2853">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2853">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="5c3ac-2854">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2854">Updated cmdlets</span></span>
        - <span data-ttu-id="5c3ac-2855">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2855">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="5c3ac-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2856">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="5c3ac-2857">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2857">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="5c3ac-2858">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2858">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="5c3ac-2859">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2859">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-2860">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2860">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-2861">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2861">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="5c3ac-2862">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2862">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="5c3ac-2863">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2863">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2864">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2864">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2865">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2865">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="5c3ac-2866">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2866">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="5c3ac-2867">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2867">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="5c3ac-2868">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2868">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="5c3ac-2869">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2869">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="5c3ac-2870">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2870">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="5c3ac-2871">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2871">Az.Relay</span></span>
* <span data-ttu-id="5c3ac-2872">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2872">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c3ac-2873">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2873">Az.ServiceBus</span></span>
* <span data-ttu-id="5c3ac-2874">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2874">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-2875">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2875">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-2876">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2876">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="5c3ac-2877">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2877">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="5c3ac-2878">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2878">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="5c3ac-2879">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2879">New-AzStorageAccount</span></span>
* <span data-ttu-id="5c3ac-2880">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2880">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="5c3ac-2881">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2881">New-AzStorageAccount</span></span>
    - <span data-ttu-id="5c3ac-2882">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2882">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="5c3ac-2883">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2883">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2884">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2884">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2885">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2885">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="5c3ac-2886">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2886">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="5c3ac-2887">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2887">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c3ac-2888">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2888">Highlights since the last major release</span></span>
* <span data-ttu-id="5c3ac-2889">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2889">General availability of `Az` module</span></span>
* <span data-ttu-id="5c3ac-2890">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2890">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c3ac-2891">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2891">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c3ac-2892">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2892">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c3ac-2893">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2893">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c3ac-2894">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2894">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2895">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2895">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2896">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2896">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2897">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2897">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="5c3ac-2898">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2898">Az.Batch</span></span>
* <span data-ttu-id="5c3ac-2899">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2899">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-2900">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2900">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-2901">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-2902">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2902">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-2903">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2904">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2904">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2905">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2905">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="5c3ac-2906">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c3ac-2907">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2907">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-2908">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2908">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-2909">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2909">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-2910">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2910">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-2911">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c3ac-2912">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2912">Az.EventGrid</span></span>
* <span data-ttu-id="5c3ac-2913">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2913">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-2914">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2914">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-2915">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2915">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="5c3ac-2916">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2916">Az.HDInsight</span></span>
* <span data-ttu-id="5c3ac-2917">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2917">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-2918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2918">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-2919">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2919">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-2920">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2920">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-2921">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2921">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c3ac-2922">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2922">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="5c3ac-2923">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2923">Az.MachineLearning</span></span>
* <span data-ttu-id="5c3ac-2924">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2924">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="5c3ac-2925">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2925">Az.Media</span></span>
* <span data-ttu-id="5c3ac-2926">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-2927">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2927">Az.Monitor</span></span>
  * <span data-ttu-id="5c3ac-2928">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2928">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="5c3ac-2929">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2929">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="5c3ac-2930">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2930">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="5c3ac-2931">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2931">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5c3ac-2932">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2932">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="5c3ac-2933">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2933">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="5c3ac-2934">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2934">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-2935">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2935">Az.Network</span></span>
* <span data-ttu-id="5c3ac-2936">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c3ac-2937">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2937">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="5c3ac-2938">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2938">Az.NotificationHubs</span></span>
* <span data-ttu-id="5c3ac-2939">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-2940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2940">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-2941">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="5c3ac-2942">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2942">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="5c3ac-2943">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2943">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-2944">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2944">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-2945">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2945">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c3ac-2946">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2946">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="5c3ac-2947">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2947">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="5c3ac-2948">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2948">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c3ac-2949">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2949">Az.RedisCache</span></span>
* <span data-ttu-id="5c3ac-2950">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2951">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2951">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-2952">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2952">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2953">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2953">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-2954">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2954">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="5c3ac-2955">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2955">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c3ac-2956">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2956">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="5c3ac-2957">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2957">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="5c3ac-2958">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2958">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="5c3ac-2959">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2959">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="5c3ac-2960">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2960">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-2961">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2961">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-2962">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2962">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="5c3ac-2963">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2963">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="5c3ac-2964">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2964">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="5c3ac-2965">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2965">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="5c3ac-2966">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2966">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c3ac-2967">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2967">Highlights since the last major release</span></span>
* <span data-ttu-id="5c3ac-2968">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2968">General availability of `Az` module</span></span>
* <span data-ttu-id="5c3ac-2969">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2969">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c3ac-2970">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2970">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c3ac-2971">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2971">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c3ac-2972">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2972">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c3ac-2973">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2973">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2974">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2974">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-2975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2975">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-2976">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2976">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c3ac-2977">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2977">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c3ac-2978">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2978">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="5c3ac-2979">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2979">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-2980">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2980">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-2981">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2981">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="5c3ac-2982">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2982">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="5c3ac-2983">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2983">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-2984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2984">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-2985">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2985">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="5c3ac-2986">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2986">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="5c3ac-2987">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2987">Az.ContainerInstance</span></span>
* <span data-ttu-id="5c3ac-2988">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2988">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-2989">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2989">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-2990">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2990">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="5c3ac-2991">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2991">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-2992">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2992">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-2993">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2993">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="5c3ac-2994">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2994">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="5c3ac-2995">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2995">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="5c3ac-2996">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2996">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="5c3ac-2997">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2997">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="5c3ac-2998">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2998">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-2999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-2999">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3000">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3000">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-3001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3001">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-3002">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3002">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="5c3ac-3003">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3003">New-AzStorageContext</span></span>
* <span data-ttu-id="5c3ac-3004">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3004">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="5c3ac-3005">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3005">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5c3ac-3006">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3006">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="5c3ac-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3007">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="5c3ac-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3008">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="5c3ac-3009">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3009">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="5c3ac-3010">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3010">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5c3ac-3011">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3011">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="5c3ac-3012">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3012">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="5c3ac-3013">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3013">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="5c3ac-3014">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3014">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="5c3ac-3015">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3015">Highlights since the last major release</span></span>
* <span data-ttu-id="5c3ac-3016">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3016">General availability of `Az` module</span></span>
* <span data-ttu-id="5c3ac-3017">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3017">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="5c3ac-3018">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3018">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="5c3ac-3019">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3019">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="5c3ac-3020">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3020">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c3ac-3021">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3021">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="5c3ac-3022">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3022">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-3023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3023">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-3024">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3024">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="5c3ac-3025">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3025">Dynamic grouping</span></span>
    * <span data-ttu-id="5c3ac-3026">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3026">Pre-Post script</span></span>
    * <span data-ttu-id="5c3ac-3027">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3027">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3028">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3028">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3029">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3029">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="5c3ac-3030">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3030">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-3031">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3031">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-3032">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3032">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3033">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3033">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3034">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3034">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="5c3ac-3035">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3035">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-3036">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3036">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-3037">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3037">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="5c3ac-3038">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3038">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3039">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3039">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3040">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3040">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="5c3ac-3041">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3041">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-3042">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3042">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3043">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3043">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-3044">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3044">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-3045">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3045">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="5c3ac-3046">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3046">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c3ac-3047">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3047">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c3ac-3048">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3048">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="5c3ac-3049">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3049">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="5c3ac-3050">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3050">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="5c3ac-3051">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3051">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-3052">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3052">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-3053">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3053">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="5c3ac-3054">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3054">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-3055">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3055">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-3056">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3056">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="5c3ac-3057">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3057">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-3058">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3058">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-3059">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3059">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="5c3ac-3060">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3060">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="5c3ac-3061">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3061">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-3062">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3062">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-3063">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3063">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3064">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3064">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3065">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3065">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-3066">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3066">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-3067">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3067">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c3ac-3068">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3068">Az.LogicApp</span></span>
* <span data-ttu-id="5c3ac-3069">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3069">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3070">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3070">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3071">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3071">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-3072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3072">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-3073">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3073">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="5c3ac-3074">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3074">SDK Update</span></span>
* <span data-ttu-id="5c3ac-3075">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3075">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="5c3ac-3076">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3076">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3077">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3077">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3078">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3078">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="5c3ac-3079">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3079">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="5c3ac-3080">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3080">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="5c3ac-3081">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3081">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="5c3ac-3082">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3082">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="5c3ac-3083">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3083">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-3084">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3084">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3085">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3085">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="5c3ac-3086">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3086">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-3087">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3087">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-3088">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3088">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="5c3ac-3089">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3089">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="5c3ac-3090">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3090">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c3ac-3091">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3091">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-3092">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3092">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-3093">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3093">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="5c3ac-3094">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3094">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="5c3ac-3095">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3095">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-3096">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3096">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-3097">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3097">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3098">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3098">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3099">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3099">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="5c3ac-3100">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3100">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="5c3ac-3101">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3101">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="5c3ac-3102">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3102">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-3103">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3103">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-3104">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3104">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="5c3ac-3105">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3105">Az.EventHub</span></span>
* <span data-ttu-id="5c3ac-3106">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3106">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-3107">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3107">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-3108">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3108">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c3ac-3109">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3109">Az.LogicApp</span></span>
* <span data-ttu-id="5c3ac-3110">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3110">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="5c3ac-3111">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3111">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="5c3ac-3112">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3112">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="5c3ac-3113">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3113">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c3ac-3114">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3114">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c3ac-3115">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3115">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="5c3ac-3116">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3116">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="5c3ac-3117">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3117">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="5c3ac-3118">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3118">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c3ac-3119">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3119">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c3ac-3120">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3120">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="5c3ac-3121">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3121">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="5c3ac-3122">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3122">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="5c3ac-3123">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3123">Az.Monitor</span></span>
* <span data-ttu-id="5c3ac-3124">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3124">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3125">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3126">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3126">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-3127">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3127">Az.OperationalInsights</span></span>
* <span data-ttu-id="5c3ac-3128">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3128">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="5c3ac-3129">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3129">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="5c3ac-3130">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3130">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3131">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3131">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3132">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3132">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5c3ac-3133">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3133">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="5c3ac-3134">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3134">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="5c3ac-3135">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3135">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-3136">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3136">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3137">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3137">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="5c3ac-3138">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3138">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-3139">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3139">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-3140">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3140">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="5c3ac-3141">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3141">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-3142">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3142">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-3143">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3143">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c3ac-3144">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3144">Az.AnalysisServices</span></span>
<span data-ttu-id="5c3ac-3145">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3145">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3146">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3146">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3147">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3147">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="5c3ac-3148">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3148">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="5c3ac-3149">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3149">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-3150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3150">Az.RecoveryServices</span></span>
<span data-ttu-id="5c3ac-3151">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3151">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3152">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3152">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3153">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3153">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="5c3ac-3154">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3154">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="5c3ac-3155">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3155">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="5c3ac-3156">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3156">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-3157">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3157">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3158">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3158">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="5c3ac-3159">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3159">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="5c3ac-3160">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3160">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="5c3ac-3161">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3161">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-3162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3162">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-3163">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3163">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="5c3ac-3164">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3164">Az.AnalysisServices</span></span>
* <span data-ttu-id="5c3ac-3165">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3165">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-3166">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3166">Az.RecoveryServices</span></span>
* <span data-ttu-id="5c3ac-3167">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3167">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="5c3ac-3168">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3168">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-3169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3169">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-3170">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3170">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="5c3ac-3171">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3171">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c3ac-3172">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3172">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="5c3ac-3173">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3173">Az.Aks</span></span>
* <span data-ttu-id="5c3ac-3174">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3174">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="5c3ac-3175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3175">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-3176">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3176">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="5c3ac-3177">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3177">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="5c3ac-3178">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3178">Az.Cdn</span></span>
* <span data-ttu-id="5c3ac-3179">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3179">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3180">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3181">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3181">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="5c3ac-3182">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3182">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="5c3ac-3183">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3183">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="5c3ac-3184">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3184">Az.ContainerRegistry</span></span>
* <span data-ttu-id="5c3ac-3185">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3185">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="5c3ac-3186">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3186">Az.DataFactory</span></span>
* <span data-ttu-id="5c3ac-3187">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3187">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-3188">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3188">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-3189">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3189">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="5c3ac-3190">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3190">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="5c3ac-3191">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3191">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-3192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3192">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-3193">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3193">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-3194">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3194">Az.KeyVault</span></span>
* <span data-ttu-id="5c3ac-3195">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3195">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3196">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3196">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3197">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3197">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3198">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3198">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3199">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3199">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="5c3ac-3200">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3200">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="5c3ac-3201">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3201">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="5c3ac-3202">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3202">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="5c3ac-3203">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3203">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="5c3ac-3204">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3204">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="5c3ac-3205">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3205">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-3206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3206">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-3207">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3207">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="5c3ac-3208">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3208">Fix some error messages.</span></span>
* <span data-ttu-id="5c3ac-3209">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3209">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="5c3ac-3210">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3210">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c3ac-3211">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3211">Az.SignalR</span></span>
* <span data-ttu-id="5c3ac-3212">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3212">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-3213">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3213">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3214">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3214">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c3ac-3215">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3215">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="5c3ac-3216">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3216">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="5c3ac-3217">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3217">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-3218">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3218">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-3219">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3219">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c3ac-3220">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3220">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="5c3ac-3221">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3221">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="5c3ac-3222">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3222">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="5c3ac-3223">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3223">Az.TrafficManager</span></span>
* <span data-ttu-id="5c3ac-3224">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3224">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-3225">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3225">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-3226">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3226">Update incorrect online help URLs</span></span>
* <span data-ttu-id="5c3ac-3227">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3227">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="5c3ac-3228">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3228">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="5c3ac-3229">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3229">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="5c3ac-3230">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3230">Az.Accounts</span></span>
* <span data-ttu-id="5c3ac-3231">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3231">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3232">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3232">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3233">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3233">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="5c3ac-3234">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3234">Updated the description of ID in help files</span></span>
* <span data-ttu-id="5c3ac-3235">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3235">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-3236">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3236">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-3237">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3237">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="5c3ac-3238">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3238">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="5c3ac-3239">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3239">Az.EventGrid</span></span>
* <span data-ttu-id="5c3ac-3240">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3240">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="5c3ac-3241">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3241">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="5c3ac-3242">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3242">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5c3ac-3243">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3243">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5c3ac-3244">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3244">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5c3ac-3245">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3245">Dead letter endpoint.</span></span>
    - <span data-ttu-id="5c3ac-3246">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3246">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="5c3ac-3247">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3247">Event Time-To-Live,</span></span>
        - <span data-ttu-id="5c3ac-3248">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3248">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="5c3ac-3249">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3249">Dead letter endpoint.</span></span>
* <span data-ttu-id="5c3ac-3250">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3250">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="5c3ac-3251">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3251">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="5c3ac-3252">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3252">Az.IotHub</span></span>
* <span data-ttu-id="5c3ac-3253">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3253">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="5c3ac-3254">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3254">Az.LogicApp</span></span>
* <span data-ttu-id="5c3ac-3255">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3255">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3256">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3256">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3257">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3257">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="5c3ac-3258">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3258">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="5c3ac-3259">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3259">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5c3ac-3260">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3260">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="5c3ac-3261">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3261">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="5c3ac-3262">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3262">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="5c3ac-3263">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3263">Az.SignalR</span></span>
* <span data-ttu-id="5c3ac-3264">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3264">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-3265">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3265">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3266">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3266">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="5c3ac-3267">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3267">Az.Storage</span></span>
* <span data-ttu-id="5c3ac-3268">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3268">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="5c3ac-3269">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3269">New-AzStorageContext</span></span>
* <span data-ttu-id="5c3ac-3270">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3270">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="5c3ac-3271">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3271">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-3272">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3272">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-3273">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3273">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="5c3ac-3274">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3274">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="5c3ac-3275">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3275">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="5c3ac-3276">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3276">General</span></span>

- <span data-ttu-id="5c3ac-3277">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3277">General Availability of Az Module</span></span>
- <span data-ttu-id="5c3ac-3278">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3278">Online help for each module</span></span>
- <span data-ttu-id="5c3ac-3279">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3279">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="5c3ac-3280">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3280">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="5c3ac-3281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3281">Az.Accounts</span></span>
- <span data-ttu-id="5c3ac-3282">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3282">Changed from Az.Profile</span></span>
- <span data-ttu-id="5c3ac-3283">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3283">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-3284">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3284">Az.ApiManagement</span></span>
- <span data-ttu-id="5c3ac-3285">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3285">Fixes for #7002</span></span>
- <span data-ttu-id="5c3ac-3286">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="5c3ac-3287">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3287">Az.Batch</span></span>
- <span data-ttu-id="5c3ac-3288">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3288">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="5c3ac-3289">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3289">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="5c3ac-3290">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3290">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="5c3ac-3291">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3291">Az.Billing</span></span>
- <span data-ttu-id="5c3ac-3292">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3292">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="5c3ac-3293">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3293">Az.CognitivServices</span></span>
- <span data-ttu-id="5c3ac-3294">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3294">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="5c3ac-3295">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3295">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5c3ac-3296">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3296">Az.ContainerInstance</span></span>
- <span data-ttu-id="5c3ac-3297">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3297">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="5c3ac-3298">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3298">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="5c3ac-3299">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3299">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-3300">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3300">Az.DataLakeStore</span></span>
- <span data-ttu-id="5c3ac-3301">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3301">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="5c3ac-3302">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3302">Az.Monitor</span></span>
- <span data-ttu-id="5c3ac-3303">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3303">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="5c3ac-3304">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3304">Az.KeyVault</span></span>
- <span data-ttu-id="5c3ac-3305">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3305">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="5c3ac-3306">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3306">Az.MachineLearning</span></span>
- <span data-ttu-id="5c3ac-3307">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3307">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="5c3ac-3308">Az.Media</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3308">Az.Media</span></span>
- <span data-ttu-id="5c3ac-3309">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3309">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3310">Az.Network</span></span>
<span data-ttu-id="5c3ac-3311">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3311">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="5c3ac-3312">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3312">New cmdlets added:</span></span>
        - <span data-ttu-id="5c3ac-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3313">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c3ac-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3314">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c3ac-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3315">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c3ac-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3316">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c3ac-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3317">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="5c3ac-3318">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3318">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="5c3ac-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3319">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="5c3ac-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3320">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="5c3ac-3321">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3321">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="5c3ac-3322">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3322">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="5c3ac-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3323">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5c3ac-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3324">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="5c3ac-3325">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3325">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="5c3ac-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3326">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="5c3ac-3327">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3327">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="5c3ac-3328">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3328">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="5c3ac-3329">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3329">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5c3ac-3330">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3330">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="5c3ac-3331">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3331">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="5c3ac-3332">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3332">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="5c3ac-3333">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3333">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="5c3ac-3334">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3334">Az.OperationalInsights</span></span>
- <span data-ttu-id="5c3ac-3335">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3335">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="5c3ac-3336">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3336">Az.Profile</span></span>
- <span data-ttu-id="5c3ac-3337">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3337">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-3338">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3338">Az.RecoveryServices</span></span>
- <span data-ttu-id="5c3ac-3339">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="5c3ac-3340">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3340">Az.Resources</span></span>
- <span data-ttu-id="5c3ac-3341">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-3342">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3342">Az.ServiceFabric</span></span>
- <span data-ttu-id="5c3ac-3343">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3343">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="5c3ac-3344">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3344">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="5c3ac-3345">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3345">Az.SIgnalR</span></span>
- <span data-ttu-id="5c3ac-3346">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3346">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="5c3ac-3347">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3347">Az.Sql</span></span>
- <span data-ttu-id="5c3ac-3348">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3348">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="5c3ac-3349">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3349">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="5c3ac-3350">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3350">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="5c3ac-3351">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3351">Az.Storage</span></span>
- <span data-ttu-id="5c3ac-3352">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3352">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5c3ac-3353">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3353">Az.Websites</span></span>
- <span data-ttu-id="5c3ac-3354">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3354">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="5c3ac-3355">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3355">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="5c3ac-3356">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3356">General</span></span>

* <span data-ttu-id="5c3ac-3357">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3357">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="5c3ac-3358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3358">Az.Compute</span></span>

* <span data-ttu-id="5c3ac-3359">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3359">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-3360">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3360">Az.DataLakeStore</span></span>

* <span data-ttu-id="5c3ac-3361">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3361">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="5c3ac-3362">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3362">Az.FrontDoor</span></span>

* <span data-ttu-id="5c3ac-3363">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3363">Fixed some broken links</span></span>
    - <span data-ttu-id="5c3ac-3364">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3364">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="5c3ac-3365">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3365">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="5c3ac-3366">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3366">Az.RecoveryServices</span></span>

* <span data-ttu-id="5c3ac-3367">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3367">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="5c3ac-3368">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3368">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="5c3ac-3369">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3369">Az.Resources</span></span>

* <span data-ttu-id="5c3ac-3370">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3370">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="5c3ac-3371">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3371">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="5c3ac-3372">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3372">Az.Sql</span></span>

* <span data-ttu-id="5c3ac-3373">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3373">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="5c3ac-3374">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3374">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="5c3ac-3375">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3375">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="5c3ac-3376">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3376">Az.Storage</span></span>

* <span data-ttu-id="5c3ac-3377">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3377">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="5c3ac-3378">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3378">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="5c3ac-3379">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3379">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5c3ac-3380">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3380">Support Static Website configuration</span></span>
    - <span data-ttu-id="5c3ac-3381">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3381">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="5c3ac-3382">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3382">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="5c3ac-3383">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3383">Az.Websites</span></span>

* <span data-ttu-id="5c3ac-3384">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3384">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="5c3ac-3385">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3385">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="5c3ac-3386">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3386">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="5c3ac-3387">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3387">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="5c3ac-3388">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3388">Az.ApiManagement</span></span>
* <span data-ttu-id="5c3ac-3389">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3389">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="5c3ac-3390">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3390">Az.Automation</span></span>
* <span data-ttu-id="5c3ac-3391">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3391">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="5c3ac-3392">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3392">Added Update Management cmdlets</span></span>
* <span data-ttu-id="5c3ac-3393">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3393">Added Source Control cmdlets</span></span>
* <span data-ttu-id="5c3ac-3394">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3394">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="5c3ac-3395">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3395">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="5c3ac-3396">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3396">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3397">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3397">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="5c3ac-3398">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3398">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="5c3ac-3399">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3399">Az.ContainerInstance</span></span>
* <span data-ttu-id="5c3ac-3400">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3400">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="5c3ac-3401">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3401">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="5c3ac-3402">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3402">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3403">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3404">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3404">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="5c3ac-3405">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3405">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="5c3ac-3406">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3406">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="5c3ac-3407">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3407">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="5c3ac-3408">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3408">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5c3ac-3409">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3409">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="5c3ac-3410">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3410">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="5c3ac-3411">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3411">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="5c3ac-3412">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3412">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="5c3ac-3413">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3413">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="5c3ac-3414">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3414">Az.Relay</span></span>
* <span data-ttu-id="5c3ac-3415">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3415">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="5c3ac-3416">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3416">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3417">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3417">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="5c3ac-3418">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3418">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="5c3ac-3419">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3419">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-3420">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3420">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-3421">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3421">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="5c3ac-3422">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3422">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3423">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3423">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="5c3ac-3424">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3424">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c3ac-3425">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3425">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c3ac-3426">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3426">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c3ac-3427">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3427">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="5c3ac-3428">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3428">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c3ac-3429">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3429">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c3ac-3430">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3430">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="5c3ac-3431">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3431">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="5c3ac-3432">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3432">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="5c3ac-3433">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3433">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="5c3ac-3434">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3434">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="5c3ac-3435">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3435">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5c3ac-3436">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3436">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="5c3ac-3437">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3437">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="5c3ac-3438">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3438">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="5c3ac-3439">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3439">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="5c3ac-3440">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3440">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5c3ac-3441">Geral</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3441">General</span></span>
* <span data-ttu-id="5c3ac-3442">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3442">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="5c3ac-3443">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3443">Az.Profile</span></span>
* <span data-ttu-id="5c3ac-3444">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3444">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="5c3ac-3445">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3445">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="5c3ac-3446">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3446">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="5c3ac-3447">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3447">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="5c3ac-3448">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3448">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="5c3ac-3449">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3449">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="5c3ac-3450">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3450">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-3451">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3451">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-3452">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3452">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3453">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3453">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3454">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3454">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="5c3ac-3455">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3455">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="5c3ac-3456">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3456">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-3457">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3457">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-3458">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3458">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="5c3ac-3459">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3459">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="5c3ac-3460">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3460">Az.Insights</span></span>
* <span data-ttu-id="5c3ac-3461">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3461">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="5c3ac-3462">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3462">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="5c3ac-3463">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3463">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="5c3ac-3464">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3464">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3465">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3466">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3466">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="5c3ac-3467">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3467">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="5c3ac-3468">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3468">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="5c3ac-3469">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3469">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="5c3ac-3470">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3470">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5c3ac-3471">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3471">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5c3ac-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3472">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="5c3ac-3473">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3473">Az.PolicyInsights</span></span>
* <span data-ttu-id="5c3ac-3474">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3474">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3475">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3475">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3476">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3476">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="5c3ac-3477">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3477">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="5c3ac-3478">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3478">Az.ServiceBus</span></span>
* <span data-ttu-id="5c3ac-3479">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3479">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="5c3ac-3480">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3480">Az.ServiceFabric</span></span>
* <span data-ttu-id="5c3ac-3481">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3481">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="5c3ac-3482">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3482">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="5c3ac-3483">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3483">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="5c3ac-3484">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3484">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="5c3ac-3485">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3485">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="5c3ac-3486">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3486">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="5c3ac-3487">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3487">Az.Profile</span></span>
* <span data-ttu-id="5c3ac-3488">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3488">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="5c3ac-3489">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3489">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3490">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3491">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3491">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="5c3ac-3492">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3492">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="5c3ac-3493">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3493">Az.DataLakeStore</span></span>
* <span data-ttu-id="5c3ac-3494">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3494">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="5c3ac-3495">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3495">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="5c3ac-3496">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3496">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5c3ac-3497">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3497">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="5c3ac-3498">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3498">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3499">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3500">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3500">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="5c3ac-3501">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3501">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3502">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3503">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3503">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="5c3ac-3504">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3504">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="5c3ac-3505">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3505">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="5c3ac-3506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3506">Azure.Storage</span></span>
* <span data-ttu-id="5c3ac-3507">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3507">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="5c3ac-3508">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3508">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="5c3ac-3509">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3509">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="5c3ac-3510">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3510">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="5c3ac-3511">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3511">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="5c3ac-3512">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3512">Az.CognitiveServices</span></span>
* <span data-ttu-id="5c3ac-3513">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3513">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="5c3ac-3514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3514">Az.Compute</span></span>
* <span data-ttu-id="5c3ac-3515">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3515">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="5c3ac-3516">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3516">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="5c3ac-3517">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3517">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="5c3ac-3518">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3518">Az.DataFactoryV2</span></span>
* <span data-ttu-id="5c3ac-3519">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3519">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="5c3ac-3520">Az.Network</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3520">Az.Network</span></span>
* <span data-ttu-id="5c3ac-3521">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3521">Added NetworkProfile functionality.</span></span> <span data-ttu-id="5c3ac-3522">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3522">new cmdlets added</span></span>
    - <span data-ttu-id="5c3ac-3523">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3523">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c3ac-3524">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3524">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c3ac-3525">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3525">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c3ac-3526">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3526">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="5c3ac-3527">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3527">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="5c3ac-3528">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3528">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="5c3ac-3529">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3529">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="5c3ac-3530">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3530">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="5c3ac-3531">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3531">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="5c3ac-3532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3532">Az.RedisCache</span></span>
* <span data-ttu-id="5c3ac-3533">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3533">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="5c3ac-3534">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3534">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="5c3ac-3535">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3535">Az.Resources</span></span>
* <span data-ttu-id="5c3ac-3536">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3536">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="5c3ac-3537">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3537">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="5c3ac-3538">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3538">Az.Sql</span></span>
* <span data-ttu-id="5c3ac-3539">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3539">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="5c3ac-3540">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3540">Az.Websites</span></span>
* <span data-ttu-id="5c3ac-3541">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3541">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="5c3ac-3542">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3542">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="5c3ac-3543">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3543">0.2.0 - September 2018</span></span>
 <span data-ttu-id="5c3ac-3544">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="5c3ac-3544">Initial Release</span></span>