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
ms.date: 05/18/2017
ms.openlocfilehash: 2e17b6f7f62f25d8d91c4d32a4a1ae5c45b8665d
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821795"
---
# <a name="release-notes"></a><span data-ttu-id="06870-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="06870-103">Release notes</span></span>

<span data-ttu-id="06870-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06870-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-380"></a><span data-ttu-id="06870-105">Versão 3.8.0</span><span class="sxs-lookup"><span data-stu-id="06870-105">Version 3.8.0</span></span>
* <span data-ttu-id="06870-106">Computação</span><span class="sxs-lookup"><span data-stu-id="06870-106">Compute</span></span>
  - <span data-ttu-id="06870-107">Corrigir um bug nos cmdlets Get-\* para permitir a recuperação de várias páginas de dados (mais de 120 itens)</span><span class="sxs-lookup"><span data-stu-id="06870-107">Fix bug in Get-\* cmdlets, to allow retrieving multiple pages of data (more than 120 items)</span></span>
* <span data-ttu-id="06870-108">DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="06870-108">DataLakeAnalytics</span></span>
  - <span data-ttu-id="06870-109">Corrija a ajuda de alguns comandos para ter a devida explicação e exemplos.</span><span class="sxs-lookup"><span data-stu-id="06870-109">Fix help for some commands to have the proper verbage and examples.</span></span>
* <span data-ttu-id="06870-110">DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="06870-110">DataLakeStore</span></span>
  - <span data-ttu-id="06870-111">Adicione suporte do início e final ao cmdlet `Get-AzureRMDataLakeStoreItemContent`.</span><span class="sxs-lookup"><span data-stu-id="06870-111">Add support for head and tail to the `Get-AzureRMDataLakeStoreItemContent` cmdlet.</span></span> <span data-ttu-id="06870-112">Isso permite retornar as linhas, a serem exibidas, delimitadas pelo caractere de nova linha com o primeiro ou último N.</span><span class="sxs-lookup"><span data-stu-id="06870-112">This enables returning the top N or last N new line delimited rows to be displayed.</span></span>
* <span data-ttu-id="06870-113">HDInsight</span><span class="sxs-lookup"><span data-stu-id="06870-113">HDInsight</span></span>
  - <span data-ttu-id="06870-114">Suporte adicionado para o tipo de cluster RServer</span><span class="sxs-lookup"><span data-stu-id="06870-114">Added support for RServer cluster type</span></span>
    + <span data-ttu-id="06870-115">O tamanho da VM Edgenode pode ser especificado para o cluster RServer em New-AzureRmHDInsightCluster ou New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="06870-115">Edgenode VM size can be specified for RServer cluster in New-AzureRmHDInsightCluster or New-AzureRmHDInsightClusterConfig</span></span>
    + <span data-ttu-id="06870-116">Agora, RServer é uma opção de configuração em Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="06870-116">RServer is now a configuration option in Add-AzureRmHDInsightConfigValues.</span></span> <span data-ttu-id="06870-117">Permite que o sinalizador RStudio seja definido para indicar que a instalação do RStudio deve ser feita.</span><span class="sxs-lookup"><span data-stu-id="06870-117">It allows for RStudio flag to be set to indicate that R Studio installation should be done.</span></span>
* <span data-ttu-id="06870-118">LogicApp</span><span class="sxs-lookup"><span data-stu-id="06870-118">LogicApp</span></span>
  - <span data-ttu-id="06870-119">Os cmdlets Set-AzureRmIntegrationAccountSchema e Set-AzureRmIntegrationAccountMap são corrigidos para o problema do contentlink (o conteúdo e o contentlink foram definidos, resultando em uma falha de atualização).</span><span class="sxs-lookup"><span data-stu-id="06870-119">Set-AzureRmIntegrationAccountSchema and Set-AzureRmIntegrationAccountMap cmdlets are fixed for the contentlink issue(Both content and contentlink were set resulting in update failure).</span></span>
* <span data-ttu-id="06870-120">Rede</span><span class="sxs-lookup"><span data-stu-id="06870-120">Network</span></span>
  - <span data-ttu-id="06870-121">Suporte adicionado dos novos recursos de firewall do aplicativo Web para os Gateways de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="06870-121">Added support for new web application firewall features to Application Gateways</span></span>
    + <span data-ttu-id="06870-122">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig adicionado</span><span class="sxs-lookup"><span data-stu-id="06870-122">Added New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>
    + <span data-ttu-id="06870-123">Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets) adicionado</span><span class="sxs-lookup"><span data-stu-id="06870-123">Added Get-AzureRmApplicationGatewayAvailableWafRuleSets (Alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)</span></span>
    + <span data-ttu-id="06870-124">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration atualizado: parâmetros adicionados -RuleSetType -RuleSetVersion e -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="06870-124">Updated New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
    + <span data-ttu-id="06870-125">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration atualizado: parâmetros atualizados -RuleSetType -RuleSetVersion e -DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="06870-125">Updated Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: Added parameter -RuleSetType -RuleSetVersion and -DisabledRuleGroups</span></span>
  - <span data-ttu-id="06870-126">Suporte adicionado das políticas IPSec para as Conexões de Gateway da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="06870-126">Added support for IPSec policies to Virtual Network Gateway Connections</span></span>
  - <span data-ttu-id="06870-127">New-AzureRmIpsecPolicy adicionado</span><span class="sxs-lookup"><span data-stu-id="06870-127">Added New-AzureRmIpsecPolicy</span></span>
  - <span data-ttu-id="06870-128">New-AzureRmVirtualNetworkGatewayConnection atualizado: parâmetros adicionados -IpsecPolicies e -UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="06870-128">Updated New-AzureRmVirtualNetworkGatewayConnection: Added parameter -IpsecPolicies and -UsePolicyBasedTrafficSelectors</span></span>
* <span data-ttu-id="06870-129">Perfil</span><span class="sxs-lookup"><span data-stu-id="06870-129">Profile</span></span>
  - <span data-ttu-id="06870-130">*Obsoleto*: Save-AzureRmProfile é renomeado como Save-AzureRmContext, há um alias para o antigo nome do cmdlet, o alias será removido na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="06870-130">*Obsolete*: Save-AzureRmProfile is renamed to Save-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="06870-131">*Obsoleto*: Select-AzureRmProfile é renomeado como Import-AzureRmContext, há um alias para o antigo nome do cmdlet, o alias será removido na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="06870-131">*Obsolete*: Select-AzureRmProfile is renamed to Import-AzureRmContext, there is an alias to the old cmdlet name, the alias will be removed in the next release.</span></span>
  - <span data-ttu-id="06870-132">Os tipos de saída PSAzureContext e PSAzureProfile dos cmdlets de perfil serão alterados na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="06870-132">The PSAzureContext and PSAzureProfile output types of profile cmdlets will be changed in the next release.</span></span>
  - <span data-ttu-id="06870-133">O cmdlet Save-AzureRmContext não terá nenhum OutputType na próxima versão.</span><span class="sxs-lookup"><span data-stu-id="06870-133">The Save-AzureRmContext cmdlet will have no OutputType in the next release.</span></span>
  - <span data-ttu-id="06870-134">Corrija o bug no código comum do cmdlet para usar um algoritmo compatível com o FIPS dos hashes de dados: https://github.com/Azure/azure-powershell/issues/3651</span><span class="sxs-lookup"><span data-stu-id="06870-134">Fix bug in cmdlet common code to use FIPS-compliant algorithm for data hashes: https://github.com/Azure/azure-powershell/issues/3651</span></span>
* <span data-ttu-id="06870-135">Sql</span><span class="sxs-lookup"><span data-stu-id="06870-135">Sql</span></span>
  - <span data-ttu-id="06870-136">Correções de bugs nos Cmdlets do Grupo de Failover do Azure</span><span class="sxs-lookup"><span data-stu-id="06870-136">Bug fixes on Azure Failover Group Cmdlets</span></span>
  - <span data-ttu-id="06870-137">Corrigir para sondagem da operação</span><span class="sxs-lookup"><span data-stu-id="06870-137">Fix for operation polling</span></span>
  - <span data-ttu-id="06870-138">Corrigir o valor GracePeriodWithDataLossHour ao definir a FailoverPolicy para Manual</span><span class="sxs-lookup"><span data-stu-id="06870-138">Fix GracePeriodWithDataLossHour value when setting FailoverPolicy to Manual</span></span>
* <span data-ttu-id="06870-139">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="06870-139">TrafficManager</span></span>
  - <span data-ttu-id="06870-140">Suporte para o método de roteamento de tráfego Geográfico</span><span class="sxs-lookup"><span data-stu-id="06870-140">Support for the Geographic traffic routing method</span></span>
    + <span data-ttu-id="06870-141">Novo valor 'Geográfico' para o parâmetro TrafficRoutingMethod de New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="06870-141">New value 'Geographic' for the TrafficRoutingMethod parameter of New-AzureRmTrafficManagerProfile</span></span>
    + <span data-ttu-id="06870-142">Novo parâmetro ‘GeoMapping’ para New-AzureRmTrafficManagerEndpoint e Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="06870-142">New parameter 'GeoMapping' for the New-AzureRmTrafficManagerEndpoint and Add-AzureRmTrafficManagerEndpointConfig</span></span>
    + <span data-ttu-id="06870-143">Corrigir o direcionamento de Get-AzureRmTrafficManagerProfile quando ele retorna uma coleção de perfis</span><span class="sxs-lookup"><span data-stu-id="06870-143">Fix piping for Get-AzureRmTrafficManagerProfile when it returns a collection of profiles</span></span>
* <span data-ttu-id="06870-144">ServiceManagement</span><span class="sxs-lookup"><span data-stu-id="06870-144">ServiceManagement</span></span>
  - <span data-ttu-id="06870-145">Restart-AzureVM: parâmetro InitiateMaintenance adicionado para executar a manutenção durante a reinicialização da VM.</span><span class="sxs-lookup"><span data-stu-id="06870-145">Restart-AzureVM: Added InitiateMaintenance parameter for performing maintenance during VM restart.</span></span>
  - <span data-ttu-id="06870-146">Get-AzureVM: campo do Status da Manutenção adicionado.</span><span class="sxs-lookup"><span data-stu-id="06870-146">Get-AzureVM: Added Maintenance Status field.</span></span>
  - <span data-ttu-id="06870-147">Novos cmdlets adicionados para oferecer suporte à atualização do cofre dos Serviços de Recuperação</span><span class="sxs-lookup"><span data-stu-id="06870-147">Added new cmdlets to support Recovery Services vault upgrade</span></span>
    + <span data-ttu-id="06870-148">Test-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="06870-148">Test-AzureRecoveryServicesVaultUpgrade</span></span>
    + <span data-ttu-id="06870-149">Invoke-AzureRecoveryServicesVaultUpgrade</span><span class="sxs-lookup"><span data-stu-id="06870-149">Invoke-AzureRecoveryServicesVaultUpgrade</span></span>
