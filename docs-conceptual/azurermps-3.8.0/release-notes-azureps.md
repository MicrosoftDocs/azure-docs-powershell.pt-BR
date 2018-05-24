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
ms.date: 05/18/2017
ms.openlocfilehash: ec01bca961bbeebf089b4da5951f4b810ccd7a11
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a><span data-ttu-id="5c325-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="5c325-103">Release notes</span></span>

<span data-ttu-id="5c325-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5c325-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="5c325-105">Versão 3.8.0</span><span class="sxs-lookup"><span data-stu-id="5c325-105">Version 3.8.0</span></span>
* <span data-ttu-id="5c325-106">Computação</span><span class="sxs-lookup"><span data-stu-id="5c325-106">Compute</span></span>
  - <span data-ttu-id="5c325-107">Corrigir um bug nos cmdlets Get-\* para permitir a recuperação de várias páginas de dados (mais de 120 itens)</span><span class="sxs-lookup"><span data-stu-id="5c325-107">Fix bug in Get-\* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="5c325-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5c325-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="5c325-109">Corrija a ajuda de alguns comandos para ter a devida explicação e exemplos.</span><span class="sxs-lookup"><span data-stu-id="5c325-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="5c325-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5c325-110">DataLakeStore</span></span>
  - <span data-ttu-id="5c325-111">Adicione suporte do início e final ao cmdlet `Get-AzureRMDataLakeStoreItemContent`.</span><span class="sxs-lookup"><span data-stu-id="5c325-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="5c325-112">Isso permite retornar as linhas, a serem exibidas, delimitadas pelo caractere de nova linha com o primeiro ou último N.</span><span class="sxs-lookup"><span data-stu-id="5c325-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="5c325-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="5c325-113">HDInsight</span></span>
  - <span data-ttu-id="5c325-114">Suporte adicionado para o tipo de cluster RServer</span><span class="sxs-lookup"><span data-stu-id="5c325-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="5c325-115">O tamanho da VM Edgenode pode ser especificado para o cluster RServer em New-AzureRmHDInsightCluster ou New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="5c325-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="5c325-116">Agora, RServer é uma opção de configuração em Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="5c325-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="5c325-117">Permite que o sinalizador RStudio seja definido para indicar que a instalação do RStudio deve ser feita.</span><span class="sxs-lookup"><span data-stu-id="5c325-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="5c325-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="5c325-118">LogicApp</span></span>
  - <span data-ttu-id="5c325-119">Os cmdlets Set-AzureRmIntegrationAccountSchema e Set-AzureRmIntegrationAccountMap são corrigidos para o problema do contentlink (o conteúdo e o contentlink foram definidos, resultando em uma falha de atualização).</span><span class="sxs-lookup"><span data-stu-id="5c325-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="5c325-120">Rede</span><span class="sxs-lookup"><span data-stu-id="5c325-120">Network</span></span>
  - <span data-ttu-id="5c325-121">Suporte adicionado dos novos recursos de firewall do aplicativo Web para os Gateways de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="5c325-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="5c325-122">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig adicionado</span><span class="sxs-lookup"><span data-stu-id="5c325-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="5c325-123">Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets) adicionado</span><span class="sxs-lookup"><span data-stu-id="5c325-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="5c325-124">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration atualizado: parâmetros adicionados -RuleSetType -RuleSetVersion e -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="5c325-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="5c325-125">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration atualizado: parâmetros atualizados -RuleSetType -RuleSetVersion e -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="5c325-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="5c325-126">Suporte adicionado das políticas IPSec para as Conexões de Gateway da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="5c325-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="5c325-127">New-AzureRmIpsecPolicy adicionado</span><span class="sxs-lookup"><span data-stu-id="5c325-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="5c325-128">New-AzureRmVirtualNetworkGatewayConnection atualizado: parâmetros adicionados -IpsecPolicies e -UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="5c325-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="5c325-129">Perfil</span><span class="sxs-lookup"><span data-stu-id="5c325-129">Profile</span></span>
  - <span data-ttu-id="5c325-130">*Obsoleto*: Save-AzureRmProfile é renomeado como Save-AzureRmContext, há um alias para o antigo nome do cmdlet, o alias será removido na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="5c325-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="5c325-131">*Obsoleto*: Select-AzureRmProfile é renomeado como Import-AzureRmContext, há um alias para o antigo nome do cmdlet, o alias será removido na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="5c325-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="5c325-132">Os tipos de saída PSAzureContext e PSAzureProfile dos cmdlets de perfil serão alterados na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="5c325-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="5c325-133">O cmdlet Save-AzureRmContext não terá nenhum OutputType na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="5c325-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="5c325-134">Corrija o bug no código comum do cmdlet para usar um algoritmo compatível com o FIPS dos hashes de dados: https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="5c325-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="5c325-135">Sql</span><span class="sxs-lookup"><span data-stu-id="5c325-135">Sql</span></span>
  - <span data-ttu-id="5c325-136">Correções de bugs nos Cmdlets do Grupo de Failover do Azure</span><span class="sxs-lookup"><span data-stu-id="5c325-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="5c325-137">Corrigir para sondagem da operação</span><span class="sxs-lookup"><span data-stu-id="5c325-137">Fix for operation polling</span></span>
  - <span data-ttu-id="5c325-138">Corrigir o valor GracePeriodWithDataLossHour ao definir a FailoverPolicy para Manual</span><span class="sxs-lookup"><span data-stu-id="5c325-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="5c325-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5c325-139">TrafficManager</span></span>
  - <span data-ttu-id="5c325-140">Suporte para o método de roteamento de tráfego Geográfico</span><span class="sxs-lookup"><span data-stu-id="5c325-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="5c325-141">Novo valor 'Geográfico' para o parâmetro TrafficRoutingMethod de New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c325-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="5c325-142">Novo parâmetro ‘GeoMapping’ para New-AzureRmTrafficManagerEndpoint e Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5c325-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="5c325-143">Corrigir o direcionamento de Get-AzureRmTrafficManagerProfile quando ele retorna uma coleção de perfis</span><span class="sxs-lookup"><span data-stu-id="5c325-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="5c325-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="5c325-144">ServiceManagement</span></span>
  - <span data-ttu-id="5c325-145">Restart-AzureVM: parâmetro InitiateMaintenance adicionado para executar a manutenção durante a reinicialização da VM.</span><span class="sxs-lookup"><span data-stu-id="5c325-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="5c325-146">Get-AzureVM: campo do Status da Manutenção adicionado.</span><span class="sxs-lookup"><span data-stu-id="5c325-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="5c325-147">Novos cmdlets adicionados para oferecer suporte à atualização do cofre dos Serviços de Recuperação</span><span class="sxs-lookup"><span data-stu-id="5c325-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="5c325-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="5c325-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="5c325-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="5c325-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
