---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 98bae70dbd61c74aa92e69cb67afc89ebae23f70
ms.sourcegitcommit: 15f21c40dcb7610e2fbaaabf264ad925e4224500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "90927938"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="d00cb-103">Notas sobre a versão do Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d00cb-103">Azure PowerShell release notes</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="d00cb-104">4.7.0 – Setembro de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-104">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-105">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-106">As próximas mensagens de alteração da falha foram formatadas</span><span class="sxs-lookup"><span data-stu-id="d00cb-106">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="d00cb-107">O assembly Azure.Core foi atualizado para 1.4.1</span><span class="sxs-lookup"><span data-stu-id="d00cb-107">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00cb-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00cb-108">Az.Aks</span></span>
* <span data-ttu-id="d00cb-109">A lógica de validação de parâmetro do lado do cliente foi adicionada para 'New-AzAksCluster', 'Set-AzAksCluster' e 'New-AzAksNodePool'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-109">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="d00cb-110">[#12372]</span><span class="sxs-lookup"><span data-stu-id="d00cb-110">[#12372]</span></span>
* <span data-ttu-id="d00cb-111">O suporte para complementos em 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-111">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="d00cb-112">[#11239]</span><span class="sxs-lookup"><span data-stu-id="d00cb-112">[#11239]</span></span>
* <span data-ttu-id="d00cb-113">Os cmdlets 'Enable-AzAksAddOn' e 'Disable-AzAksAddOn' dos complementos foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-113">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="d00cb-114">[#11239]</span><span class="sxs-lookup"><span data-stu-id="d00cb-114">[#11239]</span></span>
* <span data-ttu-id="d00cb-115">O parâmetro 'GenerateSshKey' para 'New-AzAksCluster' foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-115">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="d00cb-116">[#12371]</span><span class="sxs-lookup"><span data-stu-id="d00cb-116">[#12371]</span></span>
* <span data-ttu-id="d00cb-117">Versão da API atualizada para a versão de 01/06/2020.</span><span class="sxs-lookup"><span data-stu-id="d00cb-117">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-118">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-118">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-119">Foram mostrados termos legais adicionais de determinadas APIs.</span><span class="sxs-lookup"><span data-stu-id="d00cb-119">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-120">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-120">Az.Compute</span></span>
* <span data-ttu-id="d00cb-121">O parâmetro opcional '-EncryptionType' foi adicionado a 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-121">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="d00cb-122">Novos cmdlets para o novo tipo de recurso: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="d00cb-122">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="d00cb-123">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-123">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="d00cb-124">Os parâmetros opcionais '-DiskAccessId' e '-NetworkAccessPolicy' foram adicionados a 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-124">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="d00cb-125">A propriedade 'PatchStatus' foi adicionada à Exibição de Instância do VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d00cb-125">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="d00cb-126">A propriedade 'VMHealth' foi adicionada à exibição de instância da máquina virtual, que é o objeto retornado quando 'Get-AzVm' for invocado com '-Status'</span><span class="sxs-lookup"><span data-stu-id="d00cb-126">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="d00cb-127">O campo 'AssignedHost' foi adicionado às exibições de instância 'Get-AzVM' e 'Get-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-127">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="d00cb-128">O campo mostra a ID de recurso da instância de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="d00cb-128">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="d00cb-129">O parâmetro opcional '-SupportAutomaticPlacement' foi adicionado a 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-129">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="d00cb-130">O parâmetro '-HostGroupId' foi adicionado a 'New-AzVm' e 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="d00cb-130">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-131">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-131">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-132">A versão do SDK do .NET do ADF foi atualizada para 4.11.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-132">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-133">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-133">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-134">Novos cmdlets do Cluster foram adicionados: 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-134">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="d00cb-135">O problema #10722 foi consertado: Conserto (fix) para atribuir somente 'Listen' aos direitos de AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="d00cb-135">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d00cb-136">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d00cb-136">Az.Functions</span></span>
* <span data-ttu-id="d00cb-137">A capacidade de criar o Functions v2 em regiões que não têm compatibilidade foi removida.</span><span class="sxs-lookup"><span data-stu-id="d00cb-137">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="d00cb-138">PowerShell 6.2 preterido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-138">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="d00cb-139">Foi adicionado um aviso para quando um usuário criar um aplicativo de funções do PowerShell 6.2 que, em vez disso, aconselha a criação de um aplicativo de funções do PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="d00cb-139">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-140">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-141">Suporte à criação de cluster com configuração de Dimensionamento Automático</span><span class="sxs-lookup"><span data-stu-id="d00cb-141">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="d00cb-142">Adição do novo parâmetro 'AutoscaleConfiguration' ao cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="d00cb-142">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="d00cb-143">Suporte à configuração de Dimensionamento Automático do cluster operacional</span><span class="sxs-lookup"><span data-stu-id="d00cb-143">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="d00cb-144">Adicionar novo cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-144">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d00cb-145">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-145">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d00cb-146">Adicionar novo cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-146">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d00cb-147">Adicionar novo cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-147">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="d00cb-148">Adicionar novo cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="d00cb-148">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-149">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-149">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-150">O suporte para a autorização de RBAC foi adicionado [#10557]</span><span class="sxs-lookup"><span data-stu-id="d00cb-150">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="d00cb-151">Tratamento de erro aprimorado em 'Set-AzKeyVaultAccessPolicy' [#4007]</span><span class="sxs-lookup"><span data-stu-id="d00cb-151">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="d00cb-152">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="d00cb-152">Az.Kusto</span></span>
* <span data-ttu-id="d00cb-153">Disponibilidade geral do módulo 'Az.Kusto'</span><span class="sxs-lookup"><span data-stu-id="d00cb-153">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-154">Az.Network</span></span>
* <span data-ttu-id="d00cb-155">[Alteração da Falha] Os cmdlets abaixo foram atualizados para alinhar o roteador virtual do recurso e o hub virtual</span><span class="sxs-lookup"><span data-stu-id="d00cb-155">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="d00cb-156">'New-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="d00cb-156">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="d00cb-157">O parâmetro -HostedSubnet foi adicionado para dar suporte ao recurso filho da configuração de IP</span><span class="sxs-lookup"><span data-stu-id="d00cb-157">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="d00cb-158">-HostedGateway e -HostedGatewayId foram excluídos</span><span class="sxs-lookup"><span data-stu-id="d00cb-158">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="d00cb-159">'Get-AzVirtualRouter':</span><span class="sxs-lookup"><span data-stu-id="d00cb-159">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="d00cb-160">O conjunto de parâmetros de nível de assinatura foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-160">Added subscription level parameter set</span></span>
    - <span data-ttu-id="d00cb-161">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="d00cb-161">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="d00cb-162">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-162">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="d00cb-163">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-163">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="d00cb-164">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-164">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="d00cb-165">O novo cmdlet para a Porta do Express Route do Azure foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-165">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="d00cb-166">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="d00cb-166">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="d00cb-167">A propriedade RemoteBgpCommunities foi adicionada ao Recurso de Emparelhamento da VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d00cb-167">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="d00cb-168">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d00cb-168">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="d00cb-169">O VpnGatewayIpConfigurations foi adicionado à saída 'Get-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="d00cb-169">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="d00cb-170">Um bug para 'Set-AzApplicationGatewaySslCertificate' foi consertado [#9488]</span><span class="sxs-lookup"><span data-stu-id="d00cb-170">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="d00cb-171">O parâmetro 'AllowActiveFTP' foi adicionado a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="d00cb-171">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="d00cb-172">Atualizados os comandos para o recurso a seguir: Habilite definir/remover a segurança de Internet no P2SVpnGateway da VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d00cb-172">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="d00cb-173">'New-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' foi adicionado para que os clientes definam como true para habilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="d00cb-173">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="d00cb-174">'Update-AzP2sVpnGateway' foi atualizado: O parâmetro de opção opcional 'EnableInternetSecurityFlag' ou 'DisableInternetSecurityFlag' foi adicionado para que os clientes definam como true/false para habilitar/desabilitar a segurança da Internet no P2SVpnGateway, o que será aplicado aos clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="d00cb-174">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="d00cb-175">Um novo cmdlet 'Reset-AzP2sVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o P2SVpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-175">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="d00cb-176">Um novo cmdlet 'Reset-AzVpnGateway' foi adicionado para que os clientes redefinam/reiniciem o VpnGateway da VirtualWan para solucionar problemas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-176">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="d00cb-177">'Set-AzVirtualNetworkSubnetConfig' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="d00cb-177">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="d00cb-178">Definir as propriedades de NSG e da Tabela de Rotas da sub-rede como null se elas forem definidas explicitamente nos parâmetros [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="d00cb-178">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-179">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-179">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-180">O Estado de Exclusão para Itens de Backup de carga de trabalho foi consertado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-180">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-181">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-181">Az.Resources</span></span>
* <span data-ttu-id="d00cb-182">Uma verificação ausente foi adicionada para Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d00cb-182">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="d00cb-183">Um atributo de alteração da falha foi adicionado ao parâmetro 'SubscriptionId' de 'Get-AzResourceGroupDeploymentOperation'</span><span class="sxs-lookup"><span data-stu-id="d00cb-183">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="d00cb-184">Os cmdlets What-If do modelo do ARM foram atualizados para mostrar as alterações de recursos 'Ignore' por último</span><span class="sxs-lookup"><span data-stu-id="d00cb-184">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="d00cb-185">Os problemas de serialização de parâmetros de matriz e de segurança para cmdlets de implantação foram consertados [#12773]</span><span class="sxs-lookup"><span data-stu-id="d00cb-185">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-186">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-186">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-187">Novos cmdlets foram adicionados a tipos de nós e clusters gerenciados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-187">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="d00cb-188">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="d00cb-188">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d00cb-189">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="d00cb-189">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d00cb-190">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="d00cb-190">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d00cb-191">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="d00cb-191">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="d00cb-192">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="d00cb-192">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="d00cb-193">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="d00cb-193">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="d00cb-194">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="d00cb-194">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d00cb-195">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="d00cb-195">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d00cb-196">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="d00cb-196">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d00cb-197">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="d00cb-197">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="d00cb-198">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="d00cb-198">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="d00cb-199">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="d00cb-199">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="d00cb-200">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="d00cb-200">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="d00cb-201">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="d00cb-201">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="d00cb-202">O SDK do Service Fabric foi atualizado para a versão 1.2.0, que usa a versão de API 2020-03-01 do provedor de recursos do Service Fabric no modelo atual e a 2020-01-01-preview nos clusters gerenciados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-202">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-203">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-203">Az.Sql</span></span>
* <span data-ttu-id="d00cb-204">BackupStorageRedundancy foi adicionado a 'New-AzSqlInstance' e 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="d00cb-204">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="d00cb-205">O cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-205">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d00cb-206">O cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-206">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d00cb-207">O parâmetro Force foi adicionado a 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="d00cb-207">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="d00cb-208">Os cmdlets para o serviço de Reprodução de Log do Banco de Dados Gerenciado foram adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-208">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="d00cb-209">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="d00cb-209">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="d00cb-210">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="d00cb-210">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="d00cb-211">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="d00cb-211">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="d00cb-212">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="d00cb-212">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="d00cb-213">O cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-213">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d00cb-214">O cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-214">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d00cb-215">O cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-215">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d00cb-216">Os cmdlets 'New-AzSqlDatabaseImport' e 'New-AzSqlDatabaseExport' foram atualizados para dar suporte à funcionalidade de isolamento de rede</span><span class="sxs-lookup"><span data-stu-id="d00cb-216">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="d00cb-217">O cmdlet 'New-AzSqlDatabaseImportExisting' foi adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-217">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="d00cb-218">Os cmdlets de Bancos de Dados foram atualizados para dar suporte à especificação de tipo de armazenamento de backup</span><span class="sxs-lookup"><span data-stu-id="d00cb-218">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="d00cb-219">O parâmetro Force foi adicionado a 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="d00cb-219">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="d00cb-220">Um aviso para a configuração do BackupStorageRedundancy foi adicionado em regiões selecionadas no 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="d00cb-220">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="d00cb-221">Os cmdlets de ActiveDirectoryOnlyAuthentication do servidor e da instância foram atualizados para incluir ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-221">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-222">Az.Storage</span></span>
* <span data-ttu-id="d00cb-223">Uma falha no blob de upload foi consertada por meio da atualização para Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span><span class="sxs-lookup"><span data-stu-id="d00cb-223">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="d00cb-224">Restauração Pontual com suporte</span><span class="sxs-lookup"><span data-stu-id="d00cb-224">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="d00cb-225">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-225">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d00cb-226">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-226">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="d00cb-227">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="d00cb-227">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="d00cb-228">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="d00cb-228">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="d00cb-229">Suporte à obtenção do status de restauração do blob da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="d00cb-229">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="d00cb-230">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-230">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="d00cb-231">Uma mensagem de aviso de alteração da falha foi adicionada para alteração de saída de cmdlet futura</span><span class="sxs-lookup"><span data-stu-id="d00cb-231">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="d00cb-232">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-232">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="d00cb-233">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-233">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="d00cb-234">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-234">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="d00cb-235">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-235">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="d00cb-236">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="d00cb-236">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="d00cb-237">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-237">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="d00cb-238">O SDK do Microsoft.Azure.Cosmos.Table foi atualizado para 1.0.8</span><span class="sxs-lookup"><span data-stu-id="d00cb-238">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="d00cb-239">Agradecimentos aos colaboradores da comunidade</span><span class="sxs-lookup"><span data-stu-id="d00cb-239">Thanks to our community contributors</span></span>
* <span data-ttu-id="d00cb-240">Thomas Van Laere (@ThomVanL), adição de Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="d00cb-240">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="d00cb-241">Lohith Chowdary Chilukuri (@Lochiluk), atualização de Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="d00cb-241">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="d00cb-242">Roberth Strand (@roberthstrand), Get-AzResourceGroup – Novo exemplo e limpeza (#12828)</span><span class="sxs-lookup"><span data-stu-id="d00cb-242">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="d00cb-243">Ravi Mishra (@inmishrar), atualização da pilha de runtime do Aplicativo Web do Azure para DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="d00cb-243">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="d00cb-244">@jack-education, atualizou Set-AzVirtualNetworkSubnetConfig para permitir que o NSG e a Tabela de Rotas sejam removidos da sub-rede (#12351)</span><span class="sxs-lookup"><span data-stu-id="d00cb-244">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="d00cb-245">@hagop-globanet, atualização de Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="d00cb-245">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="d00cb-246">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="d00cb-246">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="d00cb-247">Atualização da ortografia de "Property" para "Property" (#12821)</span><span class="sxs-lookup"><span data-stu-id="d00cb-247">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="d00cb-248">Atualização de exemplos de New-AzResourceLock.md (#12806)</span><span class="sxs-lookup"><span data-stu-id="d00cb-248">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="d00cb-249">Eragon Riddle (@eragonriddle), corrigiu o nome do campo de parâmetro no exemplo (#12825)</span><span class="sxs-lookup"><span data-stu-id="d00cb-249">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="d00cb-250">@rossifumax, consertou um erro de digitação em New-AzConfigurationAssignment.md (#12701)</span><span class="sxs-lookup"><span data-stu-id="d00cb-250">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="d00cb-251">4.6.1 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-251">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="d00cb-252">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-252">Az.Compute</span></span>
* <span data-ttu-id="d00cb-253">Foi corrigido o parâmetro '-EncryptionAtHost' em 'New-AzVm' para remover o valor padrão de false [#12776]</span><span class="sxs-lookup"><span data-stu-id="d00cb-253">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="d00cb-254">4.6.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-254">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-255">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-256">Carregamento de todos os ambientes de nuvem pública quando o ponto de extremidade de descoberta não retorna AzureCloud padrão ou outros ambientes públicos [nº 12.633]</span><span class="sxs-lookup"><span data-stu-id="d00cb-256">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="d00cb-257">Exposição de SubscriptionPolicies em 'Get-AzSubscription' [nº 12.551]</span><span class="sxs-lookup"><span data-stu-id="d00cb-257">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-258">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-258">Az.Automation</span></span>
* <span data-ttu-id="d00cb-259">Adição de parâmetros '-RunOn' a 'Set-AzAutomationWebhook' para especificar um grupo do Hybrid Worker</span><span class="sxs-lookup"><span data-stu-id="d00cb-259">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-260">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-260">Az.Compute</span></span>
* <span data-ttu-id="d00cb-261">Adição do parâmetro '-EncryptionAtHost' a 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM' e 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="d00cb-261">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="d00cb-262">Adição de 'SecurityProfile' ao objeto de retorno 'Get-AzVM' e 'Get-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="d00cb-262">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="d00cb-263">Adição da opção '-InstanceView' como um parâmetro opcional a 'Get-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-263">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="d00cb-264">Adição do novo cmdlet 'Invoke-AzVmPatchAssessment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-264">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-265">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-265">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-266">Adição de propriedades ausentes à classe PSPipelineRun.</span><span class="sxs-lookup"><span data-stu-id="d00cb-266">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-267">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-267">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-268">Suporte à criação de cluster com a criptografia no recurso de host.</span><span class="sxs-lookup"><span data-stu-id="d00cb-268">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-269">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-269">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-270">Adição de mensagens de aviso ao planejamento para desabilitar a exclusão temporária</span><span class="sxs-lookup"><span data-stu-id="d00cb-270">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="d00cb-271">Adição de mensagens de aviso ao planejamento para remover o atributo SecretValueText</span><span class="sxs-lookup"><span data-stu-id="d00cb-271">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="d00cb-272">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="d00cb-272">Az.Maintenance</span></span>
* <span data-ttu-id="d00cb-273">Adição de campos opcionais relacionados ao agendamento a 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-273">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="d00cb-274">Adição de um novo cmdlet a 'Get-AzMaintenancePublicConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-274">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d00cb-275">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-275">Az.ManagedServices</span></span>
* <span data-ttu-id="d00cb-276">Adição de avisos de alteração da falha em cmdlets de definição e atribuição de serviços gerenciados</span><span class="sxs-lookup"><span data-stu-id="d00cb-276">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-277">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-277">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-278">Extensão do conjunto de parâmetros em 'Set-AzDiagnosticSetting' para separação de logs e habilitação de métricas [nº 12.482]</span><span class="sxs-lookup"><span data-stu-id="d00cb-278">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="d00cb-279">Correção do bug de 'Add-AzMetricAlertRuleV2' ao obter o alerta de métrica do pipeline</span><span class="sxs-lookup"><span data-stu-id="d00cb-279">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-280">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-280">Az.Resources</span></span>
* <span data-ttu-id="d00cb-281">Atualização da resposta de 'Get-AzPolicyAlias' para incluir informações que indicam se o alias é modificável pelo Azure Policy.</span><span class="sxs-lookup"><span data-stu-id="d00cb-281">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="d00cb-282">Criação do cmdlet 'Set-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-282">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="d00cb-283">Adição de 'Get-AzDeploymentManagementGroupWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do Grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-283">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="d00cb-284">Adição do novo cmdlet 'Get-AzTenantWhatIfResult' para obter os resultados What-If do modelo ARM no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="d00cb-284">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="d00cb-285">Substituição de '-WhatIf' e '-Confirm' por 'New-AzManagementGroupDeployment' e 'New-AzTenantDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="d00cb-285">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="d00cb-286">Correção dos comportamentos de '-WhatIf' e '-Confirm' nos novos cmdlets de implantação para que eles estejam em conformidade com False e</span><span class="sxs-lookup"><span data-stu-id="d00cb-286">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="d00cb-287">Correção do erro de serialização de '-TemplateObject' e 'TemplateParameterObject' [nº 1.528] [nº 6.292]</span><span class="sxs-lookup"><span data-stu-id="d00cb-287">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="d00cb-288">Adição do atributo de alteração da falha a 'Get-AzResourceGroupDeploymentOperation' para a próxima alteração do tipo de saída</span><span class="sxs-lookup"><span data-stu-id="d00cb-288">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d00cb-289">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d00cb-289">Az.SignalR</span></span>
* <span data-ttu-id="d00cb-290">Correção dos erros dos arquivos de ajuda 'Restart-AzSignalR' e 'Update-AzSignalR'</span><span class="sxs-lookup"><span data-stu-id="d00cb-290">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="d00cb-291">Adição dos cmdlets 'Update-AzSignalRNetworkAcl' e 'Set-AzSignalRUpstream'</span><span class="sxs-lookup"><span data-stu-id="d00cb-291">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-292">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-292">Az.Storage</span></span>
* <span data-ttu-id="d00cb-293">Suporte à aceleração de consulta de blob</span><span class="sxs-lookup"><span data-stu-id="d00cb-293">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="d00cb-294">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="d00cb-294">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="d00cb-295">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-295">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="d00cb-296">Atualização do arquivo de ajuda, adição de descrição extra e correção de erro de digitação</span><span class="sxs-lookup"><span data-stu-id="d00cb-296">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="d00cb-297">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-297">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="d00cb-298">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="d00cb-298">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="d00cb-299">Correção da falha de download de blob quando o subdiretório relacionado não existe [nº 12.592]</span><span class="sxs-lookup"><span data-stu-id="d00cb-299">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="d00cb-300">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-300">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="d00cb-301">Suporte à Política de Replicação Definir/Obter/Remover Objeto em contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-301">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="d00cb-302">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-302">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="d00cb-303">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-303">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="d00cb-304">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-304">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="d00cb-305">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-305">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="d00cb-306">Suporte da habilitação/desabilitação de ChangeFeed no serviço Blob de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-306">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="d00cb-307">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="d00cb-307">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="d00cb-308">4.5.0 – Agosto de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-308">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-309">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-310">Atualização de Connect-AzAccount para aceitar o parâmetro MaxContextPopulation [9865]</span><span class="sxs-lookup"><span data-stu-id="d00cb-310">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="d00cb-311">Atualização da versão do SubscriptionClient para 2019-06-01 e a exibição dos domínios de locatário [9838]</span><span class="sxs-lookup"><span data-stu-id="d00cb-311">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="d00cb-312">Suporte para as informações de assinatura do locatário inicial e do locatário managedBy</span><span class="sxs-lookup"><span data-stu-id="d00cb-312">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="d00cb-313">Correção do nome do módulo, informações sobre a versão nos dados telemétricos</span><span class="sxs-lookup"><span data-stu-id="d00cb-313">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="d00cb-314">Ajuste de SqlDatabaseDnsSuffix e ServiceManagementUrl se o ponto de extremidade dos metadados do ambiente retornar um valor incompatível</span><span class="sxs-lookup"><span data-stu-id="d00cb-314">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00cb-315">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00cb-315">Az.Aks</span></span>
* <span data-ttu-id="d00cb-316">Remoção de ClientIdAndSecret para ServicePrincipalIdAndSecret e definição de ClientIdAndSecret como alias [#12381].</span><span class="sxs-lookup"><span data-stu-id="d00cb-316">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="d00cb-317">Remoção de Get-AzAks/New-AzAks/Remove-AzAks/Set-AzAks para Get-AzAksCluster/New-AzAksCluster/Remove-AzAksCluster/Set-AzAksCluster e definição dos originais como alias [12373].</span><span class="sxs-lookup"><span data-stu-id="d00cb-317">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-318">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-318">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-319">Adição do novo cmdlet Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-319">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="d00cb-320">Adição do novo cmdlet Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-320">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d00cb-321">Adição do novo cmdlet Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d00cb-321">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="d00cb-322">Adição do novo cmdlet Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="d00cb-322">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="d00cb-323">Adição do novo cmdlet New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-323">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d00cb-324">Adição do novo cmdlet New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d00cb-324">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="d00cb-325">Adição do novo cmdlet New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="d00cb-325">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="d00cb-326">Adição do novo cmdlet Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-326">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="d00cb-327">Adição do novo cmdlet Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-327">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d00cb-328">Adição do novo cmdlet Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d00cb-328">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="d00cb-329">Adição do novo cmdlet Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-329">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="d00cb-330">Adição do novo parâmetro opcional [-GatewayId] ao cmdlet Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="d00cb-330">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-331">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-331">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-332">Deny usado especificamente como ação padrão de NetworkRules.</span><span class="sxs-lookup"><span data-stu-id="d00cb-332">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-333">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-333">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-334">Correção de um problema em que uma exceção é gerada quando Enum.Parse tenta forçar um valor nulo para valores de enumeração habilitados ou desabilitados [12344]</span><span class="sxs-lookup"><span data-stu-id="d00cb-334">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-335">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-335">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-336">Suporte à criação de cluster com criptografia no recurso de trânsito.</span><span class="sxs-lookup"><span data-stu-id="d00cb-336">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="d00cb-337">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d00cb-337">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="d00cb-338">Adição do novo parâmetro EncryptionInTransit ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-338">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="d00cb-339">Suporte à criação de cluster com o recurso de link privado:</span><span class="sxs-lookup"><span data-stu-id="d00cb-339">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="d00cb-340">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d00cb-340">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="d00cb-341">Adição dos novos parâmetros PublicNetworkAccessType e OutboundPublicNetworkAccessType ao cmdlet New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-341">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="d00cb-342">Informações de rede virtual retornadas ao chamar New-AzHDInsightCluster ou Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d00cb-342">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-343">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-343">Az.Network</span></span>
* <span data-ttu-id="d00cb-344">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-344">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="d00cb-345">Alterações sem interrupção adicionadas: Recurso PeerAddressType para Emparelhamento Privado em Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="d00cb-345">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="d00cb-346">Alteração de código para ignorar maiúsculas e minúsculas nos parâmetros AddressPrefixType e PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="d00cb-346">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="d00cb-347">Modificação da mensagem de aviso de New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress e New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d00cb-347">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-348">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-348">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-349">Adição da opção -ForceDelete a Remove-AzOperationalInsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="d00cb-349">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="d00cb-350">Adição do novo cmdlet Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="d00cb-350">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="d00cb-351">Adição do novo cmdlet Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d00cb-351">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-352">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-353">Melhoria da experiência de descoberta de contêiner/item do Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-353">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-354">Az.Resources</span></span>
* <span data-ttu-id="d00cb-355">Adição das propriedades Condition, ConditionVersion e Description a New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d00cb-355">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="d00cb-356">Inclui todas as alterações relevantes nos modelos de dados</span><span class="sxs-lookup"><span data-stu-id="d00cb-356">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-357">Az.Sql</span></span>
* <span data-ttu-id="d00cb-358">Correção do possível erro na diferenciação de maiúsculas e minúsculas do nome do servidor em New-AzSqlServer e Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="d00cb-358">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="d00cb-359">Correção do nome incorreto de banco de dados retornado em um erro no banco de dados existente em New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d00cb-359">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-360">Az.Storage</span></span>
* <span data-ttu-id="d00cb-361">Suporte à criação de token SAS de contêiner/blob com a nova permissão x,t</span><span class="sxs-lookup"><span data-stu-id="d00cb-361">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="d00cb-362">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="d00cb-362">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="d00cb-363">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d00cb-363">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="d00cb-364">Suporte à criação de token SAS de conta com a nova permissão x,t,f</span><span class="sxs-lookup"><span data-stu-id="d00cb-364">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="d00cb-365">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="d00cb-365">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="d00cb-366">Suporte para obter uso de compartilhamento de arquivo único</span><span class="sxs-lookup"><span data-stu-id="d00cb-366">Supported get single file share usage</span></span>
    - <span data-ttu-id="d00cb-367">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-367">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="d00cb-368">4.4.0 – julho de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-368">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-369">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-369">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-370">Novo cmdlet 'Invoke-AzRestMethod' adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-370">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="d00cb-371">Corrigido um problema que podia causar erros de autenticação em cenários com vários processos, como a execução de vários cmdlets do Azure PowerShell usando 'Start-Job' [#9448]</span><span class="sxs-lookup"><span data-stu-id="d00cb-371">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00cb-372">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00cb-372">Az.Aks</span></span>
* <span data-ttu-id="d00cb-373">Corrigido o bug em que 'Get-AzAks' não obtinha todos os clusters [#12296]</span><span class="sxs-lookup"><span data-stu-id="d00cb-373">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00cb-374">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-374">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00cb-375">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="d00cb-375">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-376">Az.Automation</span></span>
* <span data-ttu-id="d00cb-377">Corrigido o problema que a cadeia de caracteres com caracteres de escape não podia ser convertida em um objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="d00cb-377">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-378">Az.Compute</span></span>
* <span data-ttu-id="d00cb-379">Adicionado um aviso ao usar 'New-AzVmss' sem a versão da imagem 'latest'</span><span class="sxs-lookup"><span data-stu-id="d00cb-379">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-380">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-380">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-381">Parâmetros globais adicionados ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d00cb-381">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00cb-382">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00cb-382">Az.EventGrid</span></span>
* <span data-ttu-id="d00cb-383">Atualizado para usar a versão de API 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="d00cb-383">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="d00cb-384">Novos recursos adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-384">Added new features:</span></span>
    - <span data-ttu-id="d00cb-385">Mapeamento de entrada</span><span class="sxs-lookup"><span data-stu-id="d00cb-385">Input mapping</span></span>
    - <span data-ttu-id="d00cb-386">Esquema de entrega de eventos</span><span class="sxs-lookup"><span data-stu-id="d00cb-386">Event Delivery Schema</span></span>
    - <span data-ttu-id="d00cb-387">Link Privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-387">Private Link</span></span>
    - <span data-ttu-id="d00cb-388">Esquema de evento de nuvem V10</span><span class="sxs-lookup"><span data-stu-id="d00cb-388">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="d00cb-389">Tópico do Barramento de Serviço como destino</span><span class="sxs-lookup"><span data-stu-id="d00cb-389">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="d00cb-390">Função do Azure como destino</span><span class="sxs-lookup"><span data-stu-id="d00cb-390">Azure Function As Destination</span></span>
    - <span data-ttu-id="d00cb-391">Envio em lote de webhooks</span><span class="sxs-lookup"><span data-stu-id="d00cb-391">WebHook Batching</span></span>
    - <span data-ttu-id="d00cb-392">Webhook Seguro (suporte do AAD)</span><span class="sxs-lookup"><span data-stu-id="d00cb-392">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="d00cb-393">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="d00cb-393">IpFiltering</span></span>
* <span data-ttu-id="d00cb-394">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-394">Updated cmdlets:</span></span>
    - <span data-ttu-id="d00cb-395">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="d00cb-395">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="d00cb-396">Adicione novos parâmetros opcionais para dar suporte ao envio em lote de webhooks.</span><span class="sxs-lookup"><span data-stu-id="d00cb-396">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="d00cb-397">Adicione novos parâmetros opcionais para dar suporte ao webhook seguro usando o AAD.</span><span class="sxs-lookup"><span data-stu-id="d00cb-397">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="d00cb-398">Adicione uma nova enumeração para o parâmetro EndpointType para dar suporte à Função do Azure e ao tópico do Barramento de Serviço como novos destinos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-398">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="d00cb-399">Adicione um novo parâmetro opcional para o esquema de entrega.</span><span class="sxs-lookup"><span data-stu-id="d00cb-399">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="d00cb-400">'New-AzEventGridTopic'/'Update-AzEventGridTopic' e 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="d00cb-400">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="d00cb-401">Adicione novos parâmetros opcionais para dar suporte a IpFiltering.</span><span class="sxs-lookup"><span data-stu-id="d00cb-401">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="d00cb-402">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="d00cb-402">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="d00cb-403">Adicione novos parâmetros opcionais para dar suporte ao mapeamento de entrada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-403">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-404">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-404">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-405">Módulo atualizado para usar a API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="d00cb-405">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="d00cb-406">Adicionado suporte do Link Privado para recursos do Serviço de Aplicativo Web, Armazenamento e Key Vault</span><span class="sxs-lookup"><span data-stu-id="d00cb-406">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-407">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-407">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-408">Suporte adicionado à criação de clusters com armazenamento ADLSGen1/2 em nuvens nacionais.</span><span class="sxs-lookup"><span data-stu-id="d00cb-408">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-409">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-409">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-410">Corrigido o bug para 'Get-AzDiagnosticSetting' quando as métricas ou os logs são nulos [#12272]</span><span class="sxs-lookup"><span data-stu-id="d00cb-410">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-411">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-411">Az.Network</span></span>
* <span data-ttu-id="d00cb-412">Corrigida a troca de parâmetros na conexão VWan HubVnet</span><span class="sxs-lookup"><span data-stu-id="d00cb-412">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="d00cb-413">Novos cmdlets adicionados para sites da Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-413">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="d00cb-414">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="d00cb-414">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d00cb-415">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="d00cb-415">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d00cb-416">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="d00cb-416">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d00cb-417">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="d00cb-417">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="d00cb-418">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="d00cb-418">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="d00cb-419">Novos cmdlets adicionados à Solução de Virtualização de Rede do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-419">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="d00cb-420">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="d00cb-420">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d00cb-421">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="d00cb-421">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d00cb-422">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="d00cb-422">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d00cb-423">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="d00cb-423">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="d00cb-424">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="d00cb-424">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="d00cb-425">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="d00cb-425">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="d00cb-426">Gateway de Aplicativo integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-426">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="d00cb-427">StorageSync integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-427">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="d00cb-428">SignalR integrado a cmdlets comuns do Link Privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-428">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-429">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-429">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-430">Removida a referência do projeto à autenticação</span><span class="sxs-lookup"><span data-stu-id="d00cb-430">Removed project reference to Authentication</span></span>
* <span data-ttu-id="d00cb-431">Os cmdlets ajustados do Backup do Azure ajudam a tornar o texto mais preciso.</span><span class="sxs-lookup"><span data-stu-id="d00cb-431">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="d00cb-432">Suporte adicionado ao Backup do Azure para buscar trabalhos do agente MAB usando o cmdlet 'Get-AzRecoveryServicesBackupJob'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-432">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-433">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-433">Az.Resources</span></span>
* <span data-ttu-id="d00cb-434">'Save-AzResourceGroupDeploymentTemplate' atualizado para usar o SDK.</span><span class="sxs-lookup"><span data-stu-id="d00cb-434">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="d00cb-435">Cmdlet 'Unregister-AzResourceProvider' adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-435">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-436">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-436">Az.Sql</span></span>
* <span data-ttu-id="d00cb-437">Suporte adicionado para entidade de serviço e usuários convidados no cmdlet 'Set-AzSqlInstanceActiveDirectoryAdministrator'</span><span class="sxs-lookup"><span data-stu-id="d00cb-437">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="d00cb-438">Corrigido um bug nos cmdlets de classificação de dados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-438">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="d00cb-439">Suporte adicionado para failover da Instância Gerenciada de SQL do Azure: 'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="d00cb-439">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-440">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-440">Az.Storage</span></span>
* <span data-ttu-id="d00cb-441">Corrigido o problema que fazia com que o UserAgent não fosse adicionado a alguns cmdlets do plano de dados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-441">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="d00cb-442">Suporte adicionado à criação/atualização de conta de Armazenamento com MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="d00cb-442">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="d00cb-443">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-443">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="d00cb-444">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-444">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d00cb-445">Suporte à habilitação/desabilitação do controle de versão no Serviço Blob de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-445">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="d00cb-446">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="d00cb-446">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="d00cb-447">Suporte à listagem de blobs com versões de blob</span><span class="sxs-lookup"><span data-stu-id="d00cb-447">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="d00cb-448">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="d00cb-448">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="d00cb-449">Suporte à obtenção/remoção de instantâneo de blob único ou versão de blob</span><span class="sxs-lookup"><span data-stu-id="d00cb-449">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="d00cb-450">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="d00cb-450">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="d00cb-451">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="d00cb-451">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="d00cb-452">Suporte a pipeline de objeto de blob gerado por meio do Azure.Storage.Blobs V12</span><span class="sxs-lookup"><span data-stu-id="d00cb-452">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="d00cb-453">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-453">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="d00cb-454">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="d00cb-454">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="d00cb-455">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="d00cb-455">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="d00cb-456">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-456">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="d00cb-457">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-457">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00cb-458">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00cb-458">Az.StorageSync</span></span>
* <span data-ttu-id="d00cb-459">Adicionada uma nova versão de SDK do StorageSync direcionada à ApiVersion 2020-03-01</span><span class="sxs-lookup"><span data-stu-id="d00cb-459">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="d00cb-460">Adicionado cmdlet de atualização do Serviço de Sincronização de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-460">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="d00cb-461">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="d00cb-461">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="d00cb-462">Adicionados IncomingTrafficPolicy e PrivateEndpointConnections aos cmdlets do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d00cb-462">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-463">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-463">Az.Websites</span></span>
* <span data-ttu-id="d00cb-464">Agora há compatibilidade para realizar operações para os slots que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d00cb-464">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="d00cb-465">4.3.0 – junho de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-465">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-466">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-467">Suporte à configuração de ambiente de descoberta por padrão e adição de ambiente por meio de 'Add-AzEnvironment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-467">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="d00cb-468">Atualizar assemblies pré-carregados [#12024], [#11976]</span><span class="sxs-lookup"><span data-stu-id="d00cb-468">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="d00cb-469">O assembly Azure.Core foi atualizado</span><span class="sxs-lookup"><span data-stu-id="d00cb-469">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="d00cb-470">Foi corrigido um problema que pode fazer com que 'Connect-AzAccount' falhe na execução em múltiplos threads [#11201]</span><span class="sxs-lookup"><span data-stu-id="d00cb-470">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00cb-471">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00cb-471">Az.Aks</span></span>
* <span data-ttu-id="d00cb-472">O uso da [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) antiga foi substituído por chamadas para as APIs [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) e [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials)</span><span class="sxs-lookup"><span data-stu-id="d00cb-472">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00cb-473">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-473">Az.Batch</span></span>
* <span data-ttu-id="d00cb-474">Az.Batch foi atualizado para usar a versão 11.0.0 do SDK 'Microsoft.Azure.Management.Batch'</span><span class="sxs-lookup"><span data-stu-id="d00cb-474">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="d00cb-475">A capacidade de definir a Identidade BatchAccount foi adicionada no cmdlet 'New-AzBatchAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-475">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-476">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-476">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-477">Suporte à exibição de funcionalidades da conta.</span><span class="sxs-lookup"><span data-stu-id="d00cb-477">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="d00cb-478">Suporte à modificação de PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="d00cb-478">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-479">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-479">Az.Compute</span></span>
* <span data-ttu-id="d00cb-480">O parâmetro SimulateEviction foi adicionado aos cmdlets Set-AzVM e Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d00cb-480">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="d00cb-481">'Premium_LRS' foi adicionado ao finalizador de argumento do parâmetro StorageAccountType para o cmdlet New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d00cb-481">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="d00cb-482">Os Substatus foram adicionados a VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="d00cb-482">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="d00cb-483">'Delete' foi adicionado ao finalizador de argumento do parâmetro EvictionPolicy para os cmdlets New-AzVM e New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d00cb-483">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="d00cb-484">Foi corrigido o nome da nova Extensão de VM para SAP</span><span class="sxs-lookup"><span data-stu-id="d00cb-484">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-485">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-485">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-486">A versão do SDK do .NET do ADF foi atualizada para 4.9.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-486">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-487">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-487">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-488">Os parâmetros de Identidade Gerenciada foram adicionados aos cmdlets 'New-AzEventHubNamespace' e 'Set-AzEventHubNamespace'</span><span class="sxs-lookup"><span data-stu-id="d00cb-488">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d00cb-489">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d00cb-489">Az.Functions</span></span>
* <span data-ttu-id="d00cb-490">Foi adicionado suporte para criar aplicativos de funções do PowerShell 7.0 e do Java 11</span><span class="sxs-lookup"><span data-stu-id="d00cb-490">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-491">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-491">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-492">Suporte à listagem de hosts e reinicialização de hosts específicos do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d00cb-492">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d00cb-493">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d00cb-493">Az.HealthcareApis</span></span>
* <span data-ttu-id="d00cb-494">A versão do SDK foi atualizada para 1.1.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-494">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="d00cb-495">Foi adicionado suporte para configurações de Exportação e Identidade Gerenciada</span><span class="sxs-lookup"><span data-stu-id="d00cb-495">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-496">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-496">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-497">Foi corrigido o parâmetro de objeto de entrada para 'Set-AzActivityLogAlert'</span><span class="sxs-lookup"><span data-stu-id="d00cb-497">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="d00cb-498">Foi corrigido o parâmetro 'InputObject' para 'Set-AzActionGroup' [#10868]</span><span class="sxs-lookup"><span data-stu-id="d00cb-498">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-499">Az.Network</span></span>
* <span data-ttu-id="d00cb-500">Foi adicionado suporte do parâmetro AddressPrefixType para 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-500">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="d00cb-501">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-501">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="d00cb-502">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="d00cb-502">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="d00cb-503">Suporte para FQDN de Destino em Regras de Rede para Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="d00cb-503">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="d00cb-504">Foi adicionado suporte para operações do pool de endereços de back-end</span><span class="sxs-lookup"><span data-stu-id="d00cb-504">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="d00cb-505">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-505">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="d00cb-506">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="d00cb-506">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="d00cb-507">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="d00cb-507">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="d00cb-508">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="d00cb-508">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="d00cb-509">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="d00cb-509">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="d00cb-510">A validação de nome foi adicionada para 'New-AzIpGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-510">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="d00cb-511">Novos cmdlets foram adicionados para o Azure FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-511">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="d00cb-512">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="d00cb-512">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="d00cb-513">Atualizados os comandos para o recurso a seguir: Os servidores DNS personalizados são definidos/removidos no VirtualWan P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-513">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="d00cb-514">New-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="d00cb-514">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="d00cb-515">Update-AzP2sVpnGateway foi atualizado: O parâmetro opcional '-CustomDnsServer' foi adicionado para que os clientes especifiquem os seus servidores DNS a serem definidos em P2SVpnGateway, o que pode ser usado por clientes Ponto a site.</span><span class="sxs-lookup"><span data-stu-id="d00cb-515">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="d00cb-516">'Update-AzVpnGateway' foi atualizado</span><span class="sxs-lookup"><span data-stu-id="d00cb-516">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="d00cb-517">O parâmetro opcional '-BgpPeeringAddress' foi adicionado para que os clientes especifiquem os seus bgps personalizados a serem definidos em VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-517">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="d00cb-518">O novo cmdlet foi adicionado para dar suporte à redefinição do estado de roteamento de um recurso VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="d00cb-518">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="d00cb-519">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="d00cb-519">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="d00cb-520">Os itens a seguir foram atualizados com base na alteração recente do Swagger para a Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="d00cb-520">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="d00cb-521">Altera os nomes de RuleGroup, RuleCollectionGroup e RuleType</span><span class="sxs-lookup"><span data-stu-id="d00cb-521">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="d00cb-522">Foi adicionado suporte a múltiplas Coleções de Regras NAT nas Coleções de Regras NAT de Política de Firewall</span><span class="sxs-lookup"><span data-stu-id="d00cb-522">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="d00cb-523">[Alteração da Falha] Foi adicionado o parâmetro obrigatório 'SourceIpGroup' para 'New-AzFirewallPolicyApplicationRule' e 'New-AzFirewallPolicyNetworkRule'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-523">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="d00cb-524">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d00cb-524">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="d00cb-525">[Alteração da Falha] Foi corrigido o 'New-AzFirewallPolicyApplicationRule'; o parâmetro 'SourceAddress' passa a ser obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d00cb-525">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="d00cb-526">[Alteração da Falha] Parâmetros obrigatórios removidos: 'TranslatedAddress', 'TranslatedPort' para 'New-AzFirewallPolicyNatRuleCollection'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-526">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="d00cb-527">Novos cmdlets foram adicionados para dar suporte a PrivateLink no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d00cb-527">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="d00cb-528">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-528">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d00cb-529">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-529">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d00cb-530">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-530">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d00cb-531">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-531">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d00cb-532">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-532">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="d00cb-533">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-533">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="d00cb-534">Novos cmdlets foram adicionados para o recurso filho HubRouteTables do VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="d00cb-534">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="d00cb-535">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="d00cb-535">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="d00cb-536">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="d00cb-536">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="d00cb-537">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="d00cb-537">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="d00cb-538">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="d00cb-538">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="d00cb-539">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="d00cb-539">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="d00cb-540">Os cmdlets existentes foram atualizados para dar suporte ao parâmetro de entrada RoutingConfiguration opcional para roteamento personalizado no VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d00cb-540">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="d00cb-541">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-541">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="d00cb-542">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-542">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="d00cb-543">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-543">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d00cb-544">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-544">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d00cb-545">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-545">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="d00cb-546">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-546">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="d00cb-547">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="d00cb-547">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="d00cb-548">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="d00cb-548">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-549">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-549">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-550">Foi corrigido o bug em que PSWorkspace não implementa IOperationalInsightsWorkspace [#12135]</span><span class="sxs-lookup"><span data-stu-id="d00cb-550">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="d00cb-551">'pergb2018' foi adicionado ao conjunto de valores válido do parâmetro 'Sku' em 'Set-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="d00cb-551">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="d00cb-552">O alias 'FunctionParameters' do parâmetro 'FunctionParameter' foi adicionado a</span><span class="sxs-lookup"><span data-stu-id="d00cb-552">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="d00cb-553">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="d00cb-553">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="d00cb-554">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="d00cb-554">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-555">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-556">Foi adicionado suporte à busca de itens MAB no Backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-556">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="d00cb-557">O Azure Site Recovery dá suporte ao tipo de disco 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="d00cb-557">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-558">Az.Resources</span></span>
* <span data-ttu-id="d00cb-559">'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' foram adicionados ao 'PSADUser' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="d00cb-559">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="d00cb-560">Foi corrigido o problema em que '-Mail' não funciona no 'Get-AzADUser' [#11981]</span><span class="sxs-lookup"><span data-stu-id="d00cb-560">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="d00cb-561">O parâmetro '-ExcludeChangeType ' foi adicionado a 'Get-AzDeploymentWhatIfResult' e 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="d00cb-561">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="d00cb-562">O parâmetro '-WhatIfExcludeChangeType' foi adicionado a 'New-AzDeployment' e 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-562">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="d00cb-563">Os cmdlets 'Test-Az\*Deployment' foram atualizados para mostrar melhor as mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="d00cb-563">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="d00cb-564">Foi corrigida a mensagem de ajuda do parâmetro '-Name' de criação de implantação e dos cmdlets What-If</span><span class="sxs-lookup"><span data-stu-id="d00cb-564">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-565">Az.Sql</span></span>
* <span data-ttu-id="d00cb-566">Foi adicionado suporte à entidade de serviço para o cmdlet de Definição do Administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="d00cb-566">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="d00cb-567">Foi corrigido o problema de sincronização nos cmdlets de Classificação de Dados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-567">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="d00cb-568">Suporte à pesquisa de usuário por email em 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span><span class="sxs-lookup"><span data-stu-id="d00cb-568">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-569">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-569">Az.Storage</span></span>
* <span data-ttu-id="d00cb-570">Suporte à criação de Conta de armazenamento com RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="d00cb-570">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="d00cb-571">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-571">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="d00cb-572">A lógica de carregamento do Azure.Core foi movida para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-572">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-573">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-573">Az.Websites</span></span>
* <span data-ttu-id="d00cb-574">Proteção adicionada para excluir o aplicativo Web criado se a restauração falhar em 'Restore-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="d00cb-574">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d00cb-575">'SourceWebApp.Location' foi adicionado para 'New-AzWebApp' e 'New-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="d00cb-575">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="d00cb-576">Foi corrigido o bug que impediu a alteração das configurações de Contêiner em 'Set-AzWebApp' e 'Set-AzWebAppSlot'</span><span class="sxs-lookup"><span data-stu-id="d00cb-576">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="d00cb-577">Foi corrigido o bug ao obter SiteConfig quando -Name não for fornecido para Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-577">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="d00cb-578">Foi adicionado um suporte para criar Aplicativos ASP para Linux</span><span class="sxs-lookup"><span data-stu-id="d00cb-578">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="d00cb-579">Exceções adicionadas para clonagem em grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="d00cb-579">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="d00cb-580">4.2.0 – Junho de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-580">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-581">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-581">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-582">Correção de um problema que pode fazer o AZ ignorar logs na Automação do Azure ou trabalhos do PowerShell [#11492]</span><span class="sxs-lookup"><span data-stu-id="d00cb-582">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00cb-583">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-583">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00cb-584">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-584">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-585">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-585">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-586">Versão do assembly de cmdlets de gerenciamento de serviços atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-586">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="d00cb-587">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d00cb-587">Az.Billing</span></span>
* <span data-ttu-id="d00cb-588">Versão do assembly de cmdlets de consumo atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-588">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-589">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-590">Suporte ao controle PrivateEndpoint e PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="d00cb-590">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-591">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-592">Versão do assembly de cmdlets de data factory V2 atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-592">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="d00cb-593">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-593">Az.DataShare</span></span>
* <span data-ttu-id="d00cb-594">Disponibilidade geral do módulo ''Az.DataShare''</span><span class="sxs-lookup"><span data-stu-id="d00cb-594">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="d00cb-595">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="d00cb-595">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="d00cb-596">Disponibilidade geral do módulo ''Az.DesktopVirtualization''</span><span class="sxs-lookup"><span data-stu-id="d00cb-596">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-597">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-597">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-598">SDK atualizado para 0.21.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-598">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="d00cb-599">Parâmetros opcionais adicionados a</span><span class="sxs-lookup"><span data-stu-id="d00cb-599">Added optional parameters to</span></span> 
    - <span data-ttu-id="d00cb-600">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="d00cb-600">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="d00cb-601">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="d00cb-601">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-602">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-602">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-603">Exemplo corrigido 3 para 'Start-AzPolicyComplianceScan'</span><span class="sxs-lookup"><span data-stu-id="d00cb-603">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d00cb-604">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d00cb-604">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d00cb-605">Versão do assembly de cmdlets do PowerBI atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-605">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d00cb-606">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d00cb-606">Az.PrivateDns</span></span>
* <span data-ttu-id="d00cb-607">Formatação de cadeia de caracteres de saída detalhada corrigida para Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-607">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-608">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-608">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-609">Suporte do Azure Site Recovery para a criação de um plano de recuperação para replicação de zona para zona da entrada XML.</span><span class="sxs-lookup"><span data-stu-id="d00cb-609">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="d00cb-610">Versão de assembly atualizada de cmdlets de backup e SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d00cb-610">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-611">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-611">Az.Resources</span></span>
* <span data-ttu-id="d00cb-612">Adicionado o parâmetro Tail aos cmdlets Get-AzDeploymentScriptLog e Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="d00cb-612">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="d00cb-613">Propriedade de saída formatada e mostrá-la na saída do cmdlet Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="d00cb-613">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="d00cb-614">Parâmetro -DeploymentScriptInputObject renomeado para -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-614">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="d00cb-615">Corrigido o nome de arquivo/destino ausente nas mensagens de cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d00cb-615">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="d00cb-616">Versão do assembly do gerenciador de recursos e cmdlets de marcas atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-616">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-617">Az.Sql</span></span>
* <span data-ttu-id="d00cb-618">Adição de UsePrivateLinkConnection a 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="d00cb-618">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="d00cb-619">Adição de SyncMemberAzureDatabaseResourceId a 'New-AzSqlSyncMember' e 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="d00cb-619">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="d00cb-620">Adição do suporte de pesquisa de usuário convidado para definir o cmdlet de administrador do Azure Active Directory do SQL Server</span><span class="sxs-lookup"><span data-stu-id="d00cb-620">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-621">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-621">Az.Storage</span></span>
* <span data-ttu-id="d00cb-622">Versão do assembly de cmdlets do plano de dados atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-622">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="d00cb-623">4.1.0 – Maio de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-623">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="d00cb-624">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="d00cb-624">Highlights since the last release</span></span>
* <span data-ttu-id="d00cb-625">Versões do PowerShell com suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="d00cb-625">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="d00cb-626">Disponibilidade geral do Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d00cb-626">General availability of Az.Functions</span></span> 
* <span data-ttu-id="d00cb-627">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources e Az.Storage têm versão principal</span><span class="sxs-lookup"><span data-stu-id="d00cb-627">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-628">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-629">'Add-AzEnvironment' e 'Set-AzEnvironment' atualizados para aceitar os parâmetros 'AzureSynapseAnalyticsEndpointResourceId' e 'AzureSynapseAnalyticsEndpointSuffix'</span><span class="sxs-lookup"><span data-stu-id="d00cb-629">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="d00cb-630">Adição de assemblies do Azure.Core relacionados em Az.Accounts. As plataformas do PowerShell com suporte incluem Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="d00cb-630">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00cb-631">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00cb-631">Az.Aks</span></span>
* <span data-ttu-id="d00cb-632">Versão de API atualizada para 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="d00cb-632">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="d00cb-633">Compatível para criar o AKS usando o contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="d00cb-633">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="d00cb-634">Novos cmdlets fornecidos: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="d00cb-634">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-635">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-635">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-636">'New-AzApiManagement' e 'Set-AzApiManagement': parâmetro [-AssignIdentity] renomeado como [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="d00cb-636">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="d00cb-637">'New-AzApiManagement' e 'Set-AzApiManagement': Novo parâmetro adicionado: [-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="d00cb-637">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="d00cb-638">'Get-AzApiManagementProperty': renomeado como 'Get-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-638">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d00cb-639">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d00cb-639">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d00cb-640">'New-AzApiManagementProperty': renomeado como 'New-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-640">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d00cb-641">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d00cb-641">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="d00cb-642">'Set-AzApiManagementProperty': renomeado como 'Set-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-642">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d00cb-643">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d00cb-643">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d00cb-644">'Remove-AzApiManagementProperty': renomeado como 'Remove-AzApiManagementNamedValue'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-644">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="d00cb-645">O parâmetro PropertyId foi renomeado como NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="d00cb-645">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="d00cb-646">Novo cmdlet 'Get-AzApiManagementAuthorizationServerClientSecret' adicionado e 'Get-AzApiManagementAuthorizationServer' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="d00cb-646">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="d00cb-647">Novo cmdlet 'Get-AzApiManagementNamedValueSecretValue' adicionado e 'Get-AzApiManagementNamedValue' não retornará o valor secreto.</span><span class="sxs-lookup"><span data-stu-id="d00cb-647">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="d00cb-648">Novo cmdlet 'Get-AzApiManagementOpenIdConnectProviderClientSecret' adicionado e 'Get-AzApiManagementOpenIdConnectProvider' não mais retornará o segredo do cliente.</span><span class="sxs-lookup"><span data-stu-id="d00cb-648">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="d00cb-649">Novo cmdlet 'Get-AzApiManagementSubscriptionKey' adicionado e 'Get-AzApiManagementSubscription' não mais retornará as chaves de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d00cb-649">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="d00cb-650">Novo cmdlet 'Get-AzApiManagementTenantAccessSecret' adicionado e 'Get-AzApiManagementTenantAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="d00cb-650">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="d00cb-651">Novo cmdlet 'Get-AzApiManagementTenantGitAccessSecret' adicionado e 'Get-AzApiManagementTenantGitAccess' não mais retornará as chaves.</span><span class="sxs-lookup"><span data-stu-id="d00cb-651">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d00cb-652">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-652">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d00cb-653">Parâmetros adicionados: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="d00cb-653">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="d00cb-654">Cmdlet 'Update-AzApplicationInsights' criado</span><span class="sxs-lookup"><span data-stu-id="d00cb-654">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="d00cb-655">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="d00cb-655">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00cb-656">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-656">Az.Batch</span></span>
* <span data-ttu-id="d00cb-657">Az.Batch atualizado para usar o SDK 'Microsoft.Azure.Batch' versão 13.0.0 e o SDK 'Microsoft.Azure.Management.Batch' versão 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="d00cb-657">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="d00cb-658">Adicionada a capacidade de selecionar o tipo de certificado que está sendo adicionado usando o novo parâmetro '-CertificateKind' a 'New-AzBatchCertificate'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-658">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="d00cb-659">A propriedade 'ApplicationPackages' foi removida de 'PSApplication', que anteriormente era sempre ''.</span><span class="sxs-lookup"><span data-stu-id="d00cb-659">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="d00cb-660">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando 'Get-AzBatchApplicationPackage'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-660">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="d00cb-661">Por exemplo:  'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-661">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="d00cb-662">Ao criar um pool usando 'New-AzBatchPool', a propriedade 'VirtualMachineImageId' de 'PSImageReference' agora pode apenas se referir a uma imagem da Galeria de Imagens Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-662">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="d00cb-663">Ao criar um pool usando 'New-AzBatchPool', o pool pode ser provisionado sem um IP público usando a nova propriedade 'PublicIPAddressConfiguration' de 'PSNetworkConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-663">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="d00cb-664">A propriedade 'PublicIPs' de 'PSNetworkConfiguration' também foi movida para 'PSPublicIPAddressConfiguration'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-664">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="d00cb-665">Essa propriedade só poderá ser especificada se 'IPAddressProvisioningType' for 'UserManaged'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-665">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-666">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-666">Az.Compute</span></span>
* <span data-ttu-id="d00cb-667">Parâmetro HostId adicionado ao cmdlet 'Update-AzVM'</span><span class="sxs-lookup"><span data-stu-id="d00cb-667">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="d00cb-668">Documentos de ajuda atualizados para os cmdlet 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' e 'Set-AzVmssOsProfile'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-668">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="d00cb-669">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="d00cb-669">Breaking changes</span></span>
    - <span data-ttu-id="d00cb-670">O parâmetro FilterExpression foi removido do cmdlet 'Get-AzVMImage'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-670">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="d00cb-671">O parâmetro AssignIdentity foi removido dos cmdlets 'New-AzVmssConfig', 'New-AzVMConfig' e 'Update-AzVM'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-671">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="d00cb-672">AutomaticRepairMaxInstanceRepairsPercent foi removido dos cmdlets 'New-AzVmssConfig' e 'Update-AzVmss'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-672">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="d00cb-673">As propriedades AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus e VirtualMachineScaleSetsColocationStatus foram removidas de ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d00cb-673">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="d00cb-674">A propriedade MaxInstanceRepairsPercent foi removida de AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="d00cb-674">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="d00cb-675">Os tipos de AvailabilitySets, VirtualMachines e VirtualMachineScaleSets foram alterados de IList<SubResource> para IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="d00cb-675">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="d00cb-676">A descrição do cmdlet 'Get-AzVM' foi atualizada para melhor descrevê-lo.</span><span class="sxs-lookup"><span data-stu-id="d00cb-676">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-677">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-677">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-678">CRUD com suporte de propriedades de runtime de fluxo de dados no IR gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-678">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-679">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-679">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-680">Novos cmdlets adicionados para criação, atualização, recuperação e exclusão do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="d00cb-680">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="d00cb-681">Cmdlets auxiliares adicionados para a construção do objeto do mecanismo de regras do Front Door</span><span class="sxs-lookup"><span data-stu-id="d00cb-681">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="d00cb-682">Referência do mecanismo de regras adicionada ao objeto de regra de roteamento do Front Door.</span><span class="sxs-lookup"><span data-stu-id="d00cb-682">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="d00cb-683">Parâmetros do Link Privado adicionados ao objeto de back-end do Front Door</span><span class="sxs-lookup"><span data-stu-id="d00cb-683">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="d00cb-684">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d00cb-684">Az.Functions</span></span>
* <span data-ttu-id="d00cb-685">Disponibilidade geral do módulo "Az.Functions"</span><span class="sxs-lookup"><span data-stu-id="d00cb-685">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-686">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-686">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-687">Suporte à criptografia de disco de chave gerenciada pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="d00cb-687">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d00cb-688">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d00cb-688">Az.HealthcareApis</span></span>
* <span data-ttu-id="d00cb-689">As políticas de acesso não são mais padronizadas para a entidade de segurança atual</span><span class="sxs-lookup"><span data-stu-id="d00cb-689">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-690">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-690">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-691">Cmdlet adicionado para invocar uma consulta em um hub IoT a fim de recuperar informações usando uma linguagem semelhante a SQL.</span><span class="sxs-lookup"><span data-stu-id="d00cb-691">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="d00cb-692">Correção do problema em que 'Add-AzIotHubDevice' falha ao criar o dispositivo habilitado para borda sem dispositivos filho [#11597]</span><span class="sxs-lookup"><span data-stu-id="d00cb-692">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="d00cb-693">Cmdlet adicionado para gerar o token SAS para o Hub IoT, dispositivo ou módulo.</span><span class="sxs-lookup"><span data-stu-id="d00cb-693">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="d00cb-694">Cmdlet adicionado para invocar a consulta de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="d00cb-694">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="d00cb-695">Gerencie a implantação automática do IoT Edge em escala.</span><span class="sxs-lookup"><span data-stu-id="d00cb-695">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="d00cb-696">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-696">New cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-697">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-697">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d00cb-698">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-698">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d00cb-699">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-699">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="d00cb-700">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-700">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="d00cb-701">Cmdlet adicionado para invocar uma consulta de métricas de implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="d00cb-701">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="d00cb-702">Cmdlet adicionado para aplicar o conteúdo de configuração ao dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-702">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-703">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-703">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-704">Dois aliases removidos: 'New-AzKeyVaultCertificateAdministratorDetails' e 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="d00cb-704">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="d00cb-705">Exclusão temporária habilitada por padrão ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="d00cb-705">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="d00cb-706">As regras de rede podem ser definidas para governar a acessibilidade de locais de rede específicos ao criar um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="d00cb-706">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="d00cb-707">Suporte adicionado para BYOK (Bring Your Own Key)</span><span class="sxs-lookup"><span data-stu-id="d00cb-707">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="d00cb-708">'Add-AzKeyVaultKey' dá suporte à geração de uma chave de troca de chaves</span><span class="sxs-lookup"><span data-stu-id="d00cb-708">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="d00cb-709">'Get-AzKeyVaultKey' dá suporte ao download de uma chave pública no formato PEM</span><span class="sxs-lookup"><span data-stu-id="d00cb-709">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="d00cb-710">Atualização da parte 'KeyOps' do documento de ajuda de 'Add-AzKeyVaultKey'</span><span class="sxs-lookup"><span data-stu-id="d00cb-710">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-711">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-712">Corrigido o bug para 'Set-AzDiagnosticSettings'. A política de retenção não se aplicará a todas as categorias [#11589]</span><span class="sxs-lookup"><span data-stu-id="d00cb-712">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="d00cb-713">Critérios de disponibilidade de WebTest com suporte para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="d00cb-713">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="d00cb-714">'New-AzMetricAlertRuleV2Criteria': uma opção para criar critérios de disponibilidade de WebTest foi adicionada</span><span class="sxs-lookup"><span data-stu-id="d00cb-714">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="d00cb-715">'Add-AzMetricAlertRuleV2': dá suporte aos novos critérios de disponibilidade de WebTest</span><span class="sxs-lookup"><span data-stu-id="d00cb-715">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="d00cb-716">Removida a definição redundante para RetentionPolicy em PSLogProfile [#7608]</span><span class="sxs-lookup"><span data-stu-id="d00cb-716">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="d00cb-717">Removidas as propriedades redundantes definidas no PSEventData [#11353]</span><span class="sxs-lookup"><span data-stu-id="d00cb-717">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="d00cb-718">'Get-AzLog' renomeado para 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="d00cb-718">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-719">Az.Network</span></span>
* <span data-ttu-id="d00cb-720">Adicionado o atributo de alteração da falha para notificar que o comportamento padrão da zona será alterado</span><span class="sxs-lookup"><span data-stu-id="d00cb-720">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="d00cb-721">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="d00cb-721">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="d00cb-722">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="d00cb-722">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="d00cb-723">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-723">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="d00cb-724">Suporte adicionado para um novo recurso de nível superior SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d00cb-724">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="d00cb-725">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-725">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-726">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d00cb-726">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d00cb-727">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d00cb-727">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d00cb-728">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d00cb-728">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="d00cb-729">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="d00cb-729">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="d00cb-730">'RequiredZoneNames' adicionado a 'PSPrivateLinkResource' e 'GroupId' a 'PSPrivateEndpointConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-730">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="d00cb-731">Corrigido o tipo incorreto de parâmetro SuccessThresholdRoundTripTimeMs para New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-731">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="d00cb-732">Cmdlets VirtualWan atualizados para definir o valor padrão do argumento AllowVnetToVnetTraffic como True.</span><span class="sxs-lookup"><span data-stu-id="d00cb-732">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="d00cb-733">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="d00cb-733">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="d00cb-734">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="d00cb-734">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="d00cb-735">Novos cmdlets adicionados para dar suporte ao grupo de zonas DNS para o ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-735">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="d00cb-736">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="d00cb-736">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="d00cb-737">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-737">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d00cb-738">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-738">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d00cb-739">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-739">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="d00cb-740">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-740">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="d00cb-741">Adição dos parâmetros 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' e 'DNSServers' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="d00cb-741">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="d00cb-742">Adição dos parâmetros 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' e 'DnsServer' a 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="d00cb-742">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="d00cb-743">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d00cb-743">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00cb-744">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d00cb-744">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-745">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-745">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-746">Código herdado atualizado para aplicar o novo SDK gerado</span><span class="sxs-lookup"><span data-stu-id="d00cb-746">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="d00cb-747">Cmdlets excluídos devido a APIs preteridas</span><span class="sxs-lookup"><span data-stu-id="d00cb-747">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="d00cb-748">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="d00cb-748">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="d00cb-749">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="d00cb-749">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="d00cb-750">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="d00cb-750">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="d00cb-751">Parâmetros adicionados para 'Set-AzOperationalInsightsWorkspace' e 'New-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="d00cb-751">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="d00cb-752">Cmdlets criados para a Conta de Armazenamento Vinculada</span><span class="sxs-lookup"><span data-stu-id="d00cb-752">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="d00cb-753">Cmdlets criados para clusters e serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="d00cb-753">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-754">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-754">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-755">O Azure Site Recovery adicionou suporte para proteger as máquinas virtuais do grupo de posicionamento por proximidade do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-755">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="d00cb-756">O Azure Site Recovery adicionou suporte para replicação de zona para zona.</span><span class="sxs-lookup"><span data-stu-id="d00cb-756">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="d00cb-757">O Backup do Azure adicionou suporte de retenção de longo prazo para pontos de recuperação do Azure FileShare.</span><span class="sxs-lookup"><span data-stu-id="d00cb-757">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="d00cb-758">O Backup do Azure adicionou propriedades de exclusão de disco à saída do cmdlet 'Get-AzRecoveryServicesBackupItem'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-758">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="d00cb-759">Adicionado ponto de extremidade privado para arquivo de credencial do cofre para o serviço de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="d00cb-759">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-760">Az.Resources</span></span>
* <span data-ttu-id="d00cb-761">Adição de aviso de mensagem sobre o atraso de exibição ao criar uma definição de função</span><span class="sxs-lookup"><span data-stu-id="d00cb-761">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="d00cb-762">Cmdlets de política alterados para gerar objetos fortemente tipados</span><span class="sxs-lookup"><span data-stu-id="d00cb-762">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="d00cb-763">Remoção do parâmetro '-TenantLevel' usado para o cmdlet 'Get-AzResourceLock' [#11335]</span><span class="sxs-lookup"><span data-stu-id="d00cb-763">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="d00cb-764">Correção de 'Remove-AzResourceGroup -Id ResourceId' [#9882]</span><span class="sxs-lookup"><span data-stu-id="d00cb-764">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="d00cb-765">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo do grupo de recursos: 'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="d00cb-765">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="d00cb-766">Adicionado novo cmdlet para obter resultados What-If do modelo ARM no escopo de assinatura: 'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="d00cb-766">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="d00cb-767">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="d00cb-767">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="d00cb-768">Parâmetros '-WhatIf' e '-Confirm' substituídos por 'New-AzDeployment' e 'New-AzResourceGroupDeployment' para usar os resultados What-If do modelo ARM</span><span class="sxs-lookup"><span data-stu-id="d00cb-768">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="d00cb-769">Mensagem de substituição adicionada para o parâmetro 'ApiVersion' nos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="d00cb-769">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="d00cb-770">Capacidade adicionada para mostrar mensagens de erro aprimoradas para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="d00cb-770">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="d00cb-771">Adicionado registro em log de correlationId para falhas de implantação</span><span class="sxs-lookup"><span data-stu-id="d00cb-771">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="d00cb-772">Propriedade 'error' adicionada à saída do script de implantação</span><span class="sxs-lookup"><span data-stu-id="d00cb-772">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="d00cb-773">Nuget Microsoft.Azure.Management.ResourceManager atualizado para '3.7.1-versão prévia'</span><span class="sxs-lookup"><span data-stu-id="d00cb-773">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="d00cb-774">Casos de teste específicos removidos como propriedade de erro em DeploymentValidateResult foram alterados para somente leitura do Nuget 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="d00cb-774">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="d00cb-775">GenericResourceExpanded trazido do SDK ResourceManager 3.7.1-versão prévia</span><span class="sxs-lookup"><span data-stu-id="d00cb-775">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="d00cb-776">Adição de suporte de marca para todos os cmdlets Get para implantação, bem como</span><span class="sxs-lookup"><span data-stu-id="d00cb-776">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="d00cb-777">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-777">'New-AzDeployment'</span></span>
    - <span data-ttu-id="d00cb-778">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-778">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="d00cb-779">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-779">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d00cb-780">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-780">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-781">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-781">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-782">Corrigido o bug em Adicionar certificado usando --SecretIdentifier que estava recebendo a impressão digital do certificado errada</span><span class="sxs-lookup"><span data-stu-id="d00cb-782">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-783">Az.Sql</span></span>
* <span data-ttu-id="d00cb-784">Melhorar desempenho de:</span><span class="sxs-lookup"><span data-stu-id="d00cb-784">Enhance performance of:</span></span>
    - <span data-ttu-id="d00cb-785">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="d00cb-785">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d00cb-786">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="d00cb-786">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d00cb-787">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="d00cb-787">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d00cb-788">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="d00cb-788">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="d00cb-789">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="d00cb-789">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d00cb-790">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="d00cb-790">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d00cb-791">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="d00cb-791">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="d00cb-792">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="d00cb-792">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="d00cb-793">Validação do lado do cliente removida do parâmetro 'RetentionDays' do cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-793">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="d00cb-794">Auditoria para uma conta de armazenamento na Vnet, corrigindo um bug ao criar uma função de Colaborador de Dados do Storage Blob.</span><span class="sxs-lookup"><span data-stu-id="d00cb-794">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-795">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-795">Az.Storage</span></span>
* <span data-ttu-id="d00cb-796">'-AsJob' adicionado para obter/listar o cmdlet de conta 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-796">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="d00cb-797">Torne a keyversion opcional ao atualizar a conta de armazenamento com KeyvaultEncryption, para dar suporte à rotação automática de chave</span><span class="sxs-lookup"><span data-stu-id="d00cb-797">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="d00cb-798">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-798">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d00cb-799">Correção da falha ao remover o diretório de arquivos do Azure com o pipeline</span><span class="sxs-lookup"><span data-stu-id="d00cb-799">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="d00cb-800">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="d00cb-800">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="d00cb-801">Corrigido [#9880]: Altere a definição do valor NetWorkRule DefaultAction para alinhar ao Swagger.</span><span class="sxs-lookup"><span data-stu-id="d00cb-801">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="d00cb-802">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="d00cb-802">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="d00cb-803">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="d00cb-803">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="d00cb-804">Corrigido [#11624]: Ignorar regras duplicadas ao adicionar NetworkRules para evitar falha do servidor</span><span class="sxs-lookup"><span data-stu-id="d00cb-804">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="d00cb-805">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-805">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="d00cb-806">SDK do Microsoft.Azure.Cosmos.Table atualizado para 1.0.7</span><span class="sxs-lookup"><span data-stu-id="d00cb-806">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="d00cb-807">Adicionada uma mensagem de aviso para lembrar o usuário de listar novamente com ContinuationToken quando apenas os itens da parte são retornados na lista de itens do DataLake Gen2,</span><span class="sxs-lookup"><span data-stu-id="d00cb-807">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="d00cb-808">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="d00cb-808">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="d00cb-809">Suporte para criar ou atualizar a conta de armazenamento com Autenticação do Serviço do Domínio do Active Directory dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-809">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="d00cb-810">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-810">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="d00cb-811">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-811">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d00cb-812">Suporte para novas ou listar chaves Kerberos da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-812">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="d00cb-813">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="d00cb-813">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="d00cb-814">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="d00cb-814">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d00cb-815">Suporte à conta de armazenamento de failover</span><span class="sxs-lookup"><span data-stu-id="d00cb-815">Supported failover Storage account</span></span>
    - <span data-ttu-id="d00cb-816">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="d00cb-816">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="d00cb-817">Ajuda de 'Get-AzStorageBlobCopyState' atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-817">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="d00cb-818">Ajuda de 'Get-AzStorageFileCopyState' e 'Start-AzStorageBlobCopy' atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-818">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="d00cb-819">Biblioteca de clientes de armazenamento integrado v12 para cmdlets de arquivo e fila</span><span class="sxs-lookup"><span data-stu-id="d00cb-819">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="d00cb-820">Tipo de saída alterado de CloudFile para AzureStorageFile. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="d00cb-820">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d00cb-821">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="d00cb-821">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="d00cb-822">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="d00cb-822">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="d00cb-823">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-823">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="d00cb-824">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-824">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="d00cb-825">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-825">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="d00cb-826">Tipo de saída alterado de CloudFileDirectory para AzureStorageFileDirectory. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="d00cb-826">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d00cb-827">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="d00cb-827">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="d00cb-828">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="d00cb-828">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="d00cb-829">Tipo de saída alterado de CloudFileShare para AzureStorageFileShare. A saída original se tornará uma propriedade filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="d00cb-829">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="d00cb-830">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="d00cb-830">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="d00cb-831">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="d00cb-831">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="d00cb-832">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="d00cb-832">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="d00cb-833">Tipo de saída alterado de FileShareProperties para AzureStorageFileShare. A saída original se tornará uma propriedade sub-filho da nova saída</span><span class="sxs-lookup"><span data-stu-id="d00cb-833">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="d00cb-834">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="d00cb-834">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d00cb-835">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d00cb-835">Az.TrafficManager</span></span>
* <span data-ttu-id="d00cb-836">Nome de perfil incorreto corrigido na saída detalhada de 'DisableAzureTrafficManagerEndpoint'</span><span class="sxs-lookup"><span data-stu-id="d00cb-836">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-837">Az.Websites</span></span>
* <span data-ttu-id="d00cb-838">Correção de erro de digitação da ajuda de 'Update-AzWebAppAccessRestrictionConfig'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-838">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="d00cb-839">3.8.0 – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-839">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="d00cb-840">Destaques desde a última versão</span><span class="sxs-lookup"><span data-stu-id="d00cb-840">Highlights since the last release</span></span>
* <span data-ttu-id="d00cb-841">Versões do PowerShell que o Az.Storage dá suporte: Windows PowerShell 5.1, PowerShell Core 6.2.4+ e PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="d00cb-841">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-842">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-842">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-843">URL atualizada da pesquisa do Azure PowerShell em 'Resolve-AzError' [nº 11507]</span><span class="sxs-lookup"><span data-stu-id="d00cb-843">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-844">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-845">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="d00cb-845">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="d00cb-846">Documentação atualizada de 'Set-AzApiManagementGroup' para especificar o parâmetro GroupId</span><span class="sxs-lookup"><span data-stu-id="d00cb-846">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00cb-847">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-847">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-848">Correção da exibição de SKU de preços relacionados ao ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="d00cb-848">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-849">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-849">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-850">Identidade, criptografia, UserOwnedStorage compatíveis</span><span class="sxs-lookup"><span data-stu-id="d00cb-850">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-851">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-851">Az.Compute</span></span>
* <span data-ttu-id="d00cb-852">Cmdlet 'Set-AzVmssOrchestrationServiceState' adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-852">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="d00cb-853">'Get-AzVmss' com -InstanceView mostra estados de OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="d00cb-853">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-854">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-854">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-855">Gerenciar a configuração de dispositivo gêmeo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-855">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-856">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="d00cb-856">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="d00cb-857">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="d00cb-857">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="d00cb-858">Cmdlet adicionado para invocar o método direto sobre um dispositivo em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="d00cb-858">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="d00cb-859">Gerenciar a configuração de módulo gêmeo do dispositivo IoT. Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-859">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-860">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="d00cb-860">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="d00cb-861">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="d00cb-861">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="d00cb-862">Gerenciar a configuração automática de gerenciamento de dispositivos da IoT em escala.</span><span class="sxs-lookup"><span data-stu-id="d00cb-862">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="d00cb-863">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-863">New cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-864">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-864">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d00cb-865">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-865">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d00cb-866">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-866">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="d00cb-867">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-867">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="d00cb-868">Cmdlet adicionado para invocar um método de módulo de borda em um Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="d00cb-868">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-869">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-869">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-870">Adição de um novo cmdlet 'Update-AzKeyVault' que pode habilitar a exclusão temporária e limpar a proteção de dados em um cofre</span><span class="sxs-lookup"><span data-stu-id="d00cb-870">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="d00cb-871">Suporte adicionado ao Microsoft.PowerShell.SecretManagement [no 11178]</span><span class="sxs-lookup"><span data-stu-id="d00cb-871">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="d00cb-872">Erro corrigido nos exemplos de 'Remove-AzKeyVaultManagedStorageSasDefinition' [no 11479]</span><span class="sxs-lookup"><span data-stu-id="d00cb-872">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="d00cb-873">Suporte adicionado ao ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-873">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="d00cb-874">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="d00cb-874">Az.Maintenance</span></span>
* <span data-ttu-id="d00cb-875">Publicação da versão de lançamento dos cmdlets de Manutenção para disponibilidade geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-875">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-876">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-876">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-877">Cmdlets adicionados para o escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-877">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="d00cb-878">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="d00cb-878">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d00cb-879">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="d00cb-879">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d00cb-880">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="d00cb-880">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d00cb-881">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="d00cb-881">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="d00cb-882">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="d00cb-882">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="d00cb-883">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="d00cb-883">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="d00cb-884">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="d00cb-884">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-885">Az.Network</span></span>
* <span data-ttu-id="d00cb-886">Cmdlets atualizados para habilitar a conexão em IP privado para o Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="d00cb-886">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="d00cb-887">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="d00cb-887">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="d00cb-888">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="d00cb-888">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="d00cb-889">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-889">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="d00cb-890">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-890">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="d00cb-891">Cmdlets atualizados para habilitar LocalNetworkGateways e VpnSites baseados em nome de domínio totalmente qualificado</span><span class="sxs-lookup"><span data-stu-id="d00cb-891">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="d00cb-892">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="d00cb-892">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="d00cb-893">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="d00cb-893">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="d00cb-894">Suporte adicionado para a família de endereços IPv6 no ExpressRouteCircuitConnectionConfig (Alcance Global)</span><span class="sxs-lookup"><span data-stu-id="d00cb-894">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="d00cb-895">'Set-AzExpressRouteCircuitConnectionConfig' adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-895">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="d00cb-896">permite a configuração de todas as propriedades existentes, incluindo o IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="d00cb-896">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="d00cb-897">'Add-AzExpressRouteCircuitConnectionConfig' atualizado</span><span class="sxs-lookup"><span data-stu-id="d00cb-897">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="d00cb-898">Outro parâmetro opcional AddressPrefixType foi adicionado para especificar a família de endereços do prefixo de endereço</span><span class="sxs-lookup"><span data-stu-id="d00cb-898">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="d00cb-899">Cmdlets atualizados para habilitar a configuração do tempo limite de DPD em Conexões de Gateway de Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="d00cb-899">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="d00cb-900">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-900">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="d00cb-901">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-901">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-902">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-902">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-903">Cmdlet 'Start-AzPolicyComplianceScan' adicionado para disparar exames de conformidade com a política</span><span class="sxs-lookup"><span data-stu-id="d00cb-903">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="d00cb-904">Foram adicionadas a definição de política, a definição de conjunto e as versões de atribuição à saída 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="d00cb-904">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-905">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-905">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-906">Aprimoramento da formatação de código e da usabilidade dos exemplos 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="d00cb-906">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-907">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-907">Az.Sql</span></span>
* <span data-ttu-id="d00cb-908">Cmdlets 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation' adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-908">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="d00cb-909">Auditoria compatível para uma conta de armazenamento na VNet.</span><span class="sxs-lookup"><span data-stu-id="d00cb-909">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-910">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-910">Az.Storage</span></span>
* <span data-ttu-id="d00cb-911">O aviso de alteração da falha foi adicionado para a alteração de saída de cmdlets do Arquivo do Azure em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="d00cb-911">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="d00cb-912">Novo SkuName StandardGZRS compatível, StandardRAGZRS ao criar/atualizar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-912">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="d00cb-913">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-913">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="d00cb-914">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-914">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="d00cb-915">DataLake Gen2 compatível</span><span class="sxs-lookup"><span data-stu-id="d00cb-915">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="d00cb-916">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="d00cb-916">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d00cb-917">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="d00cb-917">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d00cb-918">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="d00cb-918">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="d00cb-919">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="d00cb-919">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d00cb-920">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="d00cb-920">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="d00cb-921">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="d00cb-921">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="d00cb-922">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-922">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="d00cb-923">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="d00cb-923">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="d00cb-924">0.10.0–versão prévia – abril de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-924">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="d00cb-925">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-925">General</span></span>
* <span data-ttu-id="d00cb-926">Os módulos Az já estão disponíveis no Azure Stack Hub em versão prévia.</span><span class="sxs-lookup"><span data-stu-id="d00cb-926">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="d00cb-927">Isso permite a compatibilidade entre plataformas com o Linux e o macOs.</span><span class="sxs-lookup"><span data-stu-id="d00cb-927">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="d00cb-928">O Azure Stack Hub agora é compatível com o PowerShell Core com os módulos Az. Mais informações podem ser encontradas [aqui](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="d00cb-928">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="d00cb-929">Os módulos Az são compatíveis com o perfil 2019-03-01-híbrido:</span><span class="sxs-lookup"><span data-stu-id="d00cb-929">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="d00cb-930">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d00cb-930">Az.Billing</span></span>
  - <span data-ttu-id="d00cb-931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-931">Az.Compute</span></span>
  - <span data-ttu-id="d00cb-932">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d00cb-932">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="d00cb-933">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-933">Az.EventHub</span></span>
  - <span data-ttu-id="d00cb-934">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-934">Az.IotHub</span></span>
  - <span data-ttu-id="d00cb-935">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-935">Az.KeyVault</span></span>
  - <span data-ttu-id="d00cb-936">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-936">Az.Monitor</span></span>
  - <span data-ttu-id="d00cb-937">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-937">Az.Network</span></span>
  - <span data-ttu-id="d00cb-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-938">Az.Resources</span></span>
  - <span data-ttu-id="d00cb-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-939">Az.Storage</span></span>
  - <span data-ttu-id="d00cb-940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-940">Az.Websites</span></span>
* <span data-ttu-id="d00cb-941">Três novos módulos do PowerShell para az foram introduzidos e funcionam com o Azure Stack Hub, que são Az.Databox, Az.IotHub e Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-941">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="d00cb-942">Os comandos permanecem relativamente os mesmos com pequenas alterações, como a alteração do AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d00cb-942">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="d00cb-943">O link atualizado para a documentação do PowerShell para o Azure Stack Hub pode ser encontrado [aqui](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="d00cb-943">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="d00cb-944">3.7.0 – março de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-944">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-945">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-945">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-946">Corrigida a geração de NullReferenceException por 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' quando o logon não era realizado [nº 10292]</span><span class="sxs-lookup"><span data-stu-id="d00cb-946">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-947">Az.Compute</span></span>
* <span data-ttu-id="d00cb-948">Foram adicionados os seguintes parâmetros ao cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="d00cb-948">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="d00cb-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="d00cb-949">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="d00cb-950">Propriedade de criptografia permitida para o parâmetro de destino do cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-950">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="d00cb-951">Corrigido o problema de tempDisk para os cmdlets 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-951">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="d00cb-952">[nº 11354]</span><span class="sxs-lookup"><span data-stu-id="d00cb-952">[#11354]</span></span>
* <span data-ttu-id="d00cb-953">Suporte para os cmdlets abaixo adicionado para a nova extensão SAP</span><span class="sxs-lookup"><span data-stu-id="d00cb-953">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="d00cb-954">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="d00cb-954">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d00cb-955">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="d00cb-955">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d00cb-956">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="d00cb-956">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="d00cb-957">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="d00cb-957">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="d00cb-958">Corrigidos erros em exemplos do documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-958">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="d00cb-959">Mostrado o valor de cadeia de caracteres exato para o PowerState da VM no formato de tabela.</span><span class="sxs-lookup"><span data-stu-id="d00cb-959">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="d00cb-960">'New-AzVmssConfig': corrigida a serialização da propriedade AutomaticRepairs quando SinglePlacementGroup está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-960">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="d00cb-961">[nº 11257]</span><span class="sxs-lookup"><span data-stu-id="d00cb-961">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-962">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-963">Atualizada a versão do SDK do .NET do ADF para 4.8.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-963">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="d00cb-964">Parâmetros opcionais adicionados ao comando 'Invoke-AzDataFactoryV2Pipeline' para dar suporte à repetição de execução</span><span class="sxs-lookup"><span data-stu-id="d00cb-964">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-965">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-965">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-966">Adicionada descrição de alteração da falha para 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="d00cb-966">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="d00cb-967">Adicionada a opção de codificação de bytes para 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-967">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-968">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-968">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-969">Adicionado suporte para especificar a versão de TLS mínima compatível ao criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="d00cb-969">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-970">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-970">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-971">Adicionado suporte para gerenciar configurações distribuídas por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d00cb-971">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="d00cb-972">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-972">New Cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-973">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="d00cb-973">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="d00cb-974">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="d00cb-974">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-975">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-975">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-976">Adição de atributos de alteração da falha a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="d00cb-976">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-977">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-977">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-978">Documentação atualizada para 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="d00cb-978">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-979">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-979">Az.Network</span></span>
* <span data-ttu-id="d00cb-980">Cmdlets atualizados para permitir VirtualHubVnetConnections entre locatários</span><span class="sxs-lookup"><span data-stu-id="d00cb-980">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="d00cb-981">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-981">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d00cb-982">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="d00cb-982">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="d00cb-983">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="d00cb-983">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="d00cb-984">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="d00cb-984">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="d00cb-985">Removida da dependência do SDK de gerenciamento do SQL</span><span class="sxs-lookup"><span data-stu-id="d00cb-985">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-986">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-986">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-987">Mensagens de erro aprimoradas</span><span class="sxs-lookup"><span data-stu-id="d00cb-987">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-988">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-988">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-989">Adicionado suporte ao Azure Site Recovery para refazer uma proteção e atualizar as propriedades da VM para máquinas virtuais criptografadas do Azure Disk.</span><span class="sxs-lookup"><span data-stu-id="d00cb-989">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="d00cb-990">Adicionado monitoramento de DR em propriedades de VmwareToAzure do Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="d00cb-990">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="d00cb-991">Adicionado suporte ao Backup do Azure para a repetição de tentativas de atualização da política para itens com falha.</span><span class="sxs-lookup"><span data-stu-id="d00cb-991">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="d00cb-992">Adicionado suporte ao Backup do Azure para as configurações de exclusão de disco durante o backup e a restauração.</span><span class="sxs-lookup"><span data-stu-id="d00cb-992">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="d00cb-993">Adicionado suporte ao Backup do Azure para restaurar vários arquivos/pastas no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-993">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="d00cb-994">Adicionado suporte ao Backup do Azure para um grupo de recursos especificado pelo usuário ao atualizar a política IaasVM</span><span class="sxs-lookup"><span data-stu-id="d00cb-994">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-995">Az.Resources</span></span>
* <span data-ttu-id="d00cb-996">Corrigido 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' para usar a apiVersion real dos recursos, em vez da apiVersion padrão [nº. 11267]</span><span class="sxs-lookup"><span data-stu-id="d00cb-996">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="d00cb-997">Adicionado registro em log de correlationId para cenários de erro</span><span class="sxs-lookup"><span data-stu-id="d00cb-997">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="d00cb-998">Pequena alteração de documentação para 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-998">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="d00cb-999">Exemplo adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-999">Added example.</span></span>
* <span data-ttu-id="d00cb-1000">Aspas simples de escape no valor do parâmetro de 'Get-AzADUser' [nº. 11317]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1000">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="d00cb-1001">Novos cmdlets adicionados para scripts de implantação ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="d00cb-1001">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1002">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1002">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1003">Adicionado um parâmetro de réplica secundária para leitura para 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1003">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="d00cb-1004">Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication' adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1004">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="d00cb-1005">Classificação de confidencialidade salva ao classificar colunas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1005">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="d00cb-1006">Az.Support</span><span class="sxs-lookup"><span data-stu-id="d00cb-1006">Az.Support</span></span>
* <span data-ttu-id="d00cb-1007">Disponibilidade geral do módulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1007">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-1008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-1008">Az.Websites</span></span>
* <span data-ttu-id="d00cb-1009">Adicionado suporte para trabalhar com regras de roteamento de tráfego de aplicativo Web por meio dos novos cmdlets abaixo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1009">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="d00cb-1010">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1010">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d00cb-1011">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1011">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d00cb-1012">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1012">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="d00cb-1013">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1013">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="d00cb-1014">3.6.1 – Março de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-1014">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1015">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1016">Abrir a página de pesquisa do Azure PowerShell em 'Send-Feedback' [nº 11.020]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1016">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="d00cb-1017">Exibir a URL da pesquisa do Azure PowerShell em 'Resolve-Error' [nº 11.021]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1017">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="d00cb-1018">A versão Az foi adicionada ao UserAgent</span><span class="sxs-lookup"><span data-stu-id="d00cb-1018">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-1019">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-1019">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-1020">Agora há compatibilidade para recuperar e configurar o domínio personalizado no ponto de extremidade do Portal do Desenvolvedor [nº 11.007]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1020">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="d00cb-1021">'Export-AzApiManagementApi' agora é compatível com o download da definição de API no formato JSON [nº 9.987]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1021">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="d00cb-1022">'Import-AzApiManagementApi' agora é compatível com a importação da definição da OpenApi 3.0 de um documento JSON</span><span class="sxs-lookup"><span data-stu-id="d00cb-1022">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="d00cb-1023">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider' agora são compatíveis com a configuração de 'Signin Tenant' para o provedor do AAD B2C [nº 9.784]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1023">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-1024">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-1024">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-1025">A referência a System.Buffers foi explicitamente adicionada a csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1025">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-1026">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1026">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-1027">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1027">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d00cb-1028">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1028">New Cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-1029">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1029">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d00cb-1030">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1030">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d00cb-1031">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1031">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d00cb-1032">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1032">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="d00cb-1033">Agora há compatibilidade para gerenciar módulos em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1033">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="d00cb-1034">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1034">New Cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-1035">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1035">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="d00cb-1036">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1036">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="d00cb-1037">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1037">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="d00cb-1038">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1038">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="d00cb-1039">Cmdlet adicionado para obter a cadeia de conexão de um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1039">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d00cb-1040">Cmdlet adicionado para obter a cadeia de conexão de um módulo em um dispositivo IoT de destino em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1040">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="d00cb-1041">Agora há compatibilidade com o dispositivo pai get/set de um dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1041">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="d00cb-1042">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1042">New Cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-1043">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1043">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="d00cb-1044">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1044">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="d00cb-1045">Agora há compatibilidade para gerenciar a relação pai-filho de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1045">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-1046">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1046">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-1047">Valor de saída fixo para 'Get-AzMetricDefinition' [nº 9.714]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1047">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1048">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1048">Az.Network</span></span>
* <span data-ttu-id="d00cb-1049">Atualização do SDK de gerenciamento do SQL.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1049">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="d00cb-1050">Correção de um problema de diferença de nomenclatura na classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1050">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="d00cb-1051">Mapeamento do campo ActionsRequired para ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1051">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="d00cb-1052">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1052">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1053">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1053">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1054">Correção de um bug de referência nula em 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1054">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="d00cb-1055">Marcação das opções '-Force' e '-PassThru' opcionais em 'Remove-AzADGroup' [nº 10.849]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1055">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="d00cb-1056">Correção do problema em que 'MailNickname' não é retornado em 'Remove-AzADGroup' [nº 11.167]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1056">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="d00cb-1057">Correção do problema em que a operação de pipe 'Remove-AzADGroup' não funciona [nº 11.171]</span><span class="sxs-lookup"><span data-stu-id="d00cb-1057">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="d00cb-1058">Correção de um bug de referência nula em GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="d00cb-1058">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="d00cb-1059">Adição de atributos de alteração da falha para futuras alterações nos cmdlets de política</span><span class="sxs-lookup"><span data-stu-id="d00cb-1059">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="d00cb-1060">Atualização de 'Get-AzResourceGroup' para realizar a filtragem de tags de grupo de recursos no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1060">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="d00cb-1061">Cmdlets de tag estendida para aceitar -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d00cb-1061">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="d00cb-1062">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d00cb-1062">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d00cb-1063">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d00cb-1063">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="d00cb-1064">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d00cb-1064">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="d00cb-1065">Novo cmdlet de tag adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1065">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="d00cb-1066">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="d00cb-1066">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="d00cb-1067">Disponibilização de ScopedDeployment do SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1067">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1068">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1069">Inclusão de PublicNetworkAccess em 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1069">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="d00cb-1070">Agora há compatibilidade com a configuração de backup de retenção de longo prazo para os bancos de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1070">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="d00cb-1071">Get/Set de política de LTR em um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1071">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="d00cb-1072">Obtenção de backups de LTR por um banco de dados gerenciado, uma instância gerenciada ou por local</span><span class="sxs-lookup"><span data-stu-id="d00cb-1072">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="d00cb-1073">Remoção de um backup de LTR</span><span class="sxs-lookup"><span data-stu-id="d00cb-1073">Remove an LTR backup</span></span>
    - <span data-ttu-id="d00cb-1074">Restauração de um backup de LTR para criar um banco de dados gerenciados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1074">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="d00cb-1075">Inclusão de MinimalTlsVersion em New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="d00cb-1075">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="d00cb-1076">Inclusão de MinimalTlsVersion em New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-1076">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="d00cb-1077">Descarte da versão do SDK do SQL para Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1077">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1078">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1078">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1079">Compatibilidade com AllowProtectedAppendWrite em ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1079">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="d00cb-1080">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1080">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="d00cb-1081">Adição de mensagem de aviso de alteração da falha para alteração do tipo AzureStorageTable em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="d00cb-1081">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="d00cb-1082">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1082">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="d00cb-1083">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1083">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-1084">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-1084">Az.Websites</span></span>
* <span data-ttu-id="d00cb-1085">Adição do parâmetro Tag a 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1085">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="d00cb-1086">Interrupção da execução do cmdlet se uma exceção for gerada ao adicionar um domínio personalizado a um site</span><span class="sxs-lookup"><span data-stu-id="d00cb-1086">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="d00cb-1087">Agora há compatibilidade para realizar operações para os Serviços de Aplicativos que não estão no mesmo grupo de recursos que o Plano do Serviço de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1087">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="d00cb-1088">Restrição de acesso aplicada a WebApp/Function em grupos de recursos diferentes</span><span class="sxs-lookup"><span data-stu-id="d00cb-1088">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="d00cb-1089">Correção do problema para definir nomes de host personalizados para WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="d00cb-1089">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="d00cb-1090">3.5.0 – Fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-1090">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00cb-1091">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d00cb-1091">Highlights since the last major release</span></span>
* <span data-ttu-id="d00cb-1092">Telemetria do lado do cliente atualizada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1092">Updated client side telemetry.</span></span>
* <span data-ttu-id="d00cb-1093">Az.IotHub adicionou cmdlets ao suporte para gerenciar os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1093">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="d00cb-1094">Az.SqlVirtualMachine adicionou cmdlets para o ouvinte do grupo de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1094">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1095">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1095">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1096">SubscriptionId, TenantId e o tempo de execução foram adicionados aos dados de telemetria do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="d00cb-1096">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-1097">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1097">Az.Automation</span></span>
* <span data-ttu-id="d00cb-1098">Correção de um erro de digitação no Exemplo 1 da documentação de referência do 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1098">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-1100">Atualização do SDK para a versão 7.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1100">Updated SDK to 7.0</span></span>
* <span data-ttu-id="d00cb-1101">Melhoria da mensagem de erro quando as respostas do servidor mostram um corpo vazio</span><span class="sxs-lookup"><span data-stu-id="d00cb-1101">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1102">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1103">Permissão de valor vazio para ProximityPlacementGroupId durante a atualização</span><span class="sxs-lookup"><span data-stu-id="d00cb-1103">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-1104">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1104">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-1105">Cmdlet adicionado para obter as definições de regra gerenciada que podem ser usadas no WAF</span><span class="sxs-lookup"><span data-stu-id="d00cb-1105">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-1106">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1106">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-1107">Adição de suporte para o gerenciamento de dispositivos em um Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1107">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="d00cb-1108">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1108">New Cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-1109">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1109">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d00cb-1110">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1110">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d00cb-1111">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1111">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="d00cb-1112">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1112">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-1113">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-1113">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-1114">Correção do texto duplicado em Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="d00cb-1114">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-1115">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1115">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-1116">Correção da descrição do cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1116">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="d00cb-1117">Um novo parâmetro chamado ActionGroupId foi adicionado ao comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1117">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="d00cb-1118">O usuário pode fornecer ActionGroupId(string) ou ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="d00cb-1118">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1119">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1119">Az.Network</span></span>
* <span data-ttu-id="d00cb-1120">Adição de mais uma observação ao parâmetro '-EnableProxyProtocol' para o cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1120">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="d00cb-1121">Correção do exemplo de FilterData em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1121">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d00cb-1122">Adição de exemplo de captura de pacote para a captura de todos os pacotes internos e externos em Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1122">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="d00cb-1123">Suporte à Política de Firewall do Azure nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1123">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="d00cb-1124">Nenhum novo cmdlet adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1124">No new cmdlets are added.</span></span> <span data-ttu-id="d00cb-1125">Relaxamento da restrição da política de firewall nos firewalls da VNet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1125">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1126">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1126">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1127">Adição de suporte para restauração como arquivos aos Bancos de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1127">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1128">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1129">Refatoração dos cmdlets de implantação de modelo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1129">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="d00cb-1130">Adição de novos cmdlets para gerenciar implantações no grupo de gerenciamento: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d00cb-1130">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="d00cb-1131">Adição de novos cmdlets para gerenciar implantações no escopo do locatário: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d00cb-1131">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="d00cb-1132">Refatoração dos cmdlets \*-AzDeployment para trabalhar especificamente no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="d00cb-1132">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="d00cb-1133">Criação de aliases de \*-AzSubscriptionDeployment para os cmdlets \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d00cb-1133">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="d00cb-1134">Correção de 'Update-AzADApplication' quando o parâmetro 'AvailableToOtherTenants' não estiver definido</span><span class="sxs-lookup"><span data-stu-id="d00cb-1134">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="d00cb-1135">Remoção de ApplicationObjectWithoutCredentialParameterSet para evitar AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1135">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="d00cb-1136">Regeneração dos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-1136">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1137">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1137">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1138">Adição de suporte para recuperação pontual entre assinaturas nas instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1138">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="d00cb-1139">Adição de suporte para alterar geração de hardware da Instância Gerenciada SQL existente</span><span class="sxs-lookup"><span data-stu-id="d00cb-1139">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="d00cb-1140">Correção dos exemplos de ajuda de 'Update-AzSqlServerVulnerabilityAssessmentSetting': parâmetro/propriedade de saída – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="d00cb-1140">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d00cb-1141">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d00cb-1141">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d00cb-1142">Adição de cmdlets ao ouvinte do grupo de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="d00cb-1142">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00cb-1143">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00cb-1143">Az.StorageSync</span></span>
* <span data-ttu-id="d00cb-1144">Atualização dos conjuntos de caracteres com suporte em 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1144">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="d00cb-1145">3.4.0 – fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-1145">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00cb-1146">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d00cb-1146">Highlights since the last major release</span></span>
* <span data-ttu-id="d00cb-1147">Lançamento da versão 0.1.0 inicial do Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d00cb-1147">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="d00cb-1148">Adição do suporte do ConnectionMonitor V2 do Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1148">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1149">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1150">Desabilite o salvamento automático de contexto quando AzureRmContext.json não estiver disponível</span><span class="sxs-lookup"><span data-stu-id="d00cb-1150">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="d00cb-1151">Atualize a referência ao Azure Powershell Common para 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="d00cb-1151">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-1152">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-1152">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-1153">**Get-AzApiManagementApiSchema** Correção da associação do Esquema Open-Api a uma API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="d00cb-1153">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="d00cb-1154">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="d00cb-1154">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="d00cb-1155">Corrigir a documentação de https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="d00cb-1155">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="d00cb-1156">**Set-AzApiManagementApi** Adição de exemplo para mostrar como atualizar ServiceUrl usando o cmdlet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1156">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1157">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1158">Limite o número de status de VM a 100 para evitar a limitação quando Get-AzVM -Status é executado sem o nome da VM.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1158">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="d00cb-1159">Adicionar o cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1159">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="d00cb-1160">Adicione os parâmetros EncryptionType and DiskEncryptionSetId aos seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1160">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="d00cb-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1161">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="d00cb-1162">Adicione o parâmetro ColocationStatus ao cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1162">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1163">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1163">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1164">Atualizar a versão do SDK do .NET do ADF para 4.7.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1164">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d00cb-1165">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d00cb-1165">Az.DeploymentManager</span></span>
* <span data-ttu-id="d00cb-1166">Adiciona operações LIST para recursos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1166">Adds LIST operations for resources</span></span>
* <span data-ttu-id="d00cb-1167">Adiciona a funcionalidade para executar operações em etapas de Verificação de Integridade</span><span class="sxs-lookup"><span data-stu-id="d00cb-1167">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-1168">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-1168">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-1169">Corrija o erro de documento de New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1169">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-1170">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-1170">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-1171">Adicione o alias de nome ao atributo VaultName para tornar Remove-AzureKeyVault consistente com New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1171">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1172">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1172">Az.Network</span></span>
* <span data-ttu-id="d00cb-1173">Adição de novo exemplo a Set-AzNetworkWatcherConfigFlowLog.md para demonstrar o cenário de desabilitação da Análise de Tráfego.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1173">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="d00cb-1174">Adicionar suporte para atribuir a configuração de IP de gerenciamento ao Firewall do Azure – uma sub-rede dedicada e um IP Público que o firewall usará para seu tráfego de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-1174">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="d00cb-1175">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1175">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d00cb-1176">Adição do parâmetro -ManagementPublicIpAddress (não obrigatório) que aceita um objeto de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="d00cb-1176">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="d00cb-1177">Adição do método SetManagementIpConfiguration no objeto de firewall – requer uma sub-rede e um endereço IP Público como entrada – o nome da sub-rede deve ser 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1177">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="d00cb-1178">Correção de exemplos Get-AzNetworkSecurityGroup para mostrar exemplos de NSGs em vez de adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1178">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="d00cb-1179">Correção de um erro de digitação no comando New-AzVpnSite que estava impedindo a conclusão de um parâmetro do completador de ID.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1179">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="d00cb-1180">Adição de suporte para a Configuração de URL na Ação de Regras de Reescrita no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1180">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="d00cb-1181">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1181">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-1182">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="d00cb-1183">Atualização de cmdlets com o parâmetro opcional – UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-1183">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="d00cb-1184">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1184">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="d00cb-1185">Adicionar suporte para recursos do NetworkWatcher ConnectionMonitor versão 2</span><span class="sxs-lookup"><span data-stu-id="d00cb-1185">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-1186">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-1186">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-1187">Dar suporte à conformidade de avaliação antes de determinar qual recurso corrigir</span><span class="sxs-lookup"><span data-stu-id="d00cb-1187">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="d00cb-1188">Adicionar o parâmetro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1188">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="d00cb-1189">Adicionar o cmdlet Get-AzPolicyMetadata para obter recursos de metadados de política</span><span class="sxs-lookup"><span data-stu-id="d00cb-1189">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="d00cb-1190">Atualização de Get-AzPolicyState e Get-AzPolicyStateSummary para a versão da API 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="d00cb-1190">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1191">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1191">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1192">Suporte do Azure Site Recovery para remover um disco replicado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1192">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="d00cb-1193">O Backup do Azure adicionou suporte para adicionar marcas ao criar um Cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1193">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1194">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1194">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1195">Torne -Scope opcional em cmdlets \*-AzPolicyAssignment com padrão para a assinatura de contexto</span><span class="sxs-lookup"><span data-stu-id="d00cb-1195">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="d00cb-1196">Adicionar exemplos da criação de ADServicePrincipal com credencial de senha e de chave</span><span class="sxs-lookup"><span data-stu-id="d00cb-1196">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1197">Az.Sql</span></span>
<span data-ttu-id="d00cb-1198">Corrija o cmdlet New-AzSqlDatabaseSecondary para verificar a existência de PartnerDatabaseName em vez da existência de DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1198">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1199">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1199">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1200">Dar suporte ao KeyType de Criptografia de Tabela/Fila do conjunto em Criar conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-1200">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="d00cb-1201">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-1201">New-AzStorageAccount</span></span>
* <span data-ttu-id="d00cb-1202">Mostrar RequestId quando StorageException não tiver ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1202">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="d00cb-1203">Corrigir o Exemplo 6 do cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1203">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-1204">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-1204">Az.Websites</span></span>
* <span data-ttu-id="d00cb-1205">Set-AzWebapp e Set-AzWebappSlot são compatíveis com as propriedades AlwaysOn, MinTls e FtpsState</span><span class="sxs-lookup"><span data-stu-id="d00cb-1205">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="d00cb-1206">Correção de um problema em que a definição de HttpsOnly juntamente com a alteração de AppservicePlan ao mesmo tempo em que o uso do comando individual Set-AzWebApp estava redefinindo HttpsOnly para o valor padrão</span><span class="sxs-lookup"><span data-stu-id="d00cb-1206">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="d00cb-1207">3.3.0 – Janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="d00cb-1207">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1208">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1208">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1209">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar os parâmetros AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d00cb-1209">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00cb-1210">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-1210">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-1211">Exibir detalhes de resposta de erro no cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00cb-1211">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1212">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1212">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1213">Corrigir o cmdlet Set-AzVMCustomScriptExtension para uma VM com um disco OD gerenciado que não tem o perfil de SO.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1213">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d00cb-1214">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-1214">Az.ContainerInstance</span></span>
* <span data-ttu-id="d00cb-1215">Nomes de parâmetros corrigidos usados pelo exemplo de New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1215">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d00cb-1216">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1216">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d00cb-1217">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1217">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d00cb-1218">Obter o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1218">Get the Edge Storage Container</span></span>
* <span data-ttu-id="d00cb-1219">Cmdlet adicionado 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1219">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d00cb-1220">Criar Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1220">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="d00cb-1221">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1221">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d00cb-1222">Remover o Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1222">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="d00cb-1223">Cmdlet adicionado 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1223">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="d00cb-1224">Invocar ação para atualizar dados no Contêiner de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1224">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="d00cb-1225">Cmdlet adicionado 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1225">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d00cb-1226">Obter a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1226">Get the Edge Storage Account</span></span>
* <span data-ttu-id="d00cb-1227">Cmdlet adicionado 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1227">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d00cb-1228">Criar uma Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1228">Create new Edge Storage Account</span></span>
* <span data-ttu-id="d00cb-1229">Cmdlet adicionado 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1229">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="d00cb-1230">Remover a Conta de armazenamento do Edge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1230">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="d00cb-1231">Invocar o cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1231">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="d00cb-1232">Invocar ação para atualizar dados no compartilhamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-1232">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="d00cb-1233">Cmdlet adicionado 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1233">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="d00cb-1234">Definir a credencial de conta de armazenamento az databoxedge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1234">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1235">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1235">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1236">Adicionar as propriedades AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus para o cmd Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d00cb-1236">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="d00cb-1237">Atualizar a versão do SDK do .NET do ADF para 4.6.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1237">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="d00cb-1238">Adicionar o parâmetro 'PublicIPs' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar a criação do Azure-SSIS IR com endereços IP públicos estáticos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1238">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="d00cb-1239">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="d00cb-1239">Az.DevTestLabs</span></span>
* <span data-ttu-id="d00cb-1240">Remova o link desfeito em Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="d00cb-1240">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-1241">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1241">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-1242">Correção do problema 10634: Corrigir a referência de objeto nulo para remover eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="d00cb-1242">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-1243">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-1243">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-1244">Corrigir o erro Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1244">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d00cb-1245">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d00cb-1245">Az.MachineLearning</span></span>
* <span data-ttu-id="d00cb-1246">Removidos abaixo dos cmdlets porque MachineLearningCompute não está mais disponível</span><span class="sxs-lookup"><span data-stu-id="d00cb-1246">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="d00cb-1247">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d00cb-1247">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="d00cb-1248">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="d00cb-1248">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="d00cb-1249">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d00cb-1249">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="d00cb-1250">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d00cb-1250">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="d00cb-1251">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d00cb-1251">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="d00cb-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="d00cb-1252">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="d00cb-1253">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="d00cb-1253">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1254">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1254">Az.Network</span></span>
* <span data-ttu-id="d00cb-1255">Atualizar a dependência do Microsoft.Azure.Management.Sql de 1.36-preview para 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="d00cb-1255">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1256">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1256">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1257">O Azure Site Recovery altera o suporte para VMs de disco gerenciado criptografadas em repouso com chaves gerenciadas pelo cliente do Azure para o provedor do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1257">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="d00cb-1258">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1258">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d00cb-1259">Suporte do Azure Site Recovery para entrada da ID do conjunto de criptografia de disco como entrada opcional no nível do disco para habilitar a proteção do VMware para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1259">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="d00cb-1260">Suporte do Azure Site Recovery para atualizar o item protegido de replicação com o mapa do conjunto de criptografia de disco do HyperV para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1260">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1261">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1262">Corrija um erro no documento de ajuda de 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1262">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1263">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1264">Corrija a funcionalidade de cmdlets de linha de base do conjunto de avaliação de vulnerabilidade para trabalhar no BD mestre para o banco de dados do Azure e limite-o em bancos de dados do sistema de instância.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1264">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="d00cb-1265">Corrija um erro ao criar um grupo de failover da instância do SQL</span><span class="sxs-lookup"><span data-stu-id="d00cb-1265">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="d00cb-1266">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d00cb-1266">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="d00cb-1267">Adicionar DR como um novo tipo de licença válida</span><span class="sxs-lookup"><span data-stu-id="d00cb-1267">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1268">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1268">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1269">Adicionar mensagem de aviso de alteração da falha para alteração do valor DefaultAction em uma versão futura</span><span class="sxs-lookup"><span data-stu-id="d00cb-1269">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="d00cb-1270">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1270">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="d00cb-1271">Suporte para obter a hora da última sincronização da conta de Armazenamento ao executar get-AzureRMStorageAccount com o parâmetro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="d00cb-1271">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="d00cb-1272">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-1272">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="d00cb-1273">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1273">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="d00cb-1274">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-1274">General</span></span>
* <span data-ttu-id="d00cb-1275">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1275">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1276">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1276">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1277">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="d00cb-1277">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="d00cb-1278">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="d00cb-1278">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00cb-1279">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-1279">Az.Batch</span></span>
* <span data-ttu-id="d00cb-1280">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1280">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1281">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1281">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1282">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1282">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-1283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1283">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-1284">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="d00cb-1284">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="d00cb-1285">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="d00cb-1285">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d00cb-1286">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d00cb-1286">Az.HealthcareApis</span></span>
* <span data-ttu-id="d00cb-1287">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="d00cb-1287">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-1288">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-1289">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="d00cb-1289">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="d00cb-1290">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="d00cb-1290">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="d00cb-1291">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1291">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-1292">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1292">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-1293">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1293">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="d00cb-1294">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="d00cb-1294">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="d00cb-1295">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="d00cb-1295">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1296">Az.Network</span></span>
* <span data-ttu-id="d00cb-1297">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1297">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1298">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1298">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1299">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1299">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="d00cb-1300">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1300">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1301">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1301">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1302">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="d00cb-1302">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1303">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1303">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1304">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="d00cb-1304">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="d00cb-1305">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d00cb-1305">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="d00cb-1306">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d00cb-1306">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="d00cb-1307">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1307">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="d00cb-1308">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="d00cb-1308">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="d00cb-1309">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1309">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="d00cb-1310">Suporte do QuotaGiB (compartilhar cota em Gibibye) para obter valores superiores a 5120 no plano de gerenciamento de cmdlets de compartilhamento de arquivos e alias de parâmetro 'Quota' adicionado ao parâmetro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1310">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="d00cb-1311">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-1311">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="d00cb-1312">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-1312">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="d00cb-1313">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1313">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="d00cb-1314">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="d00cb-1314">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="d00cb-1315">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="d00cb-1315">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="d00cb-1316">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="d00cb-1316">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="d00cb-1317">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1317">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00cb-1318">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d00cb-1318">Highlights since the last major release</span></span>
* <span data-ttu-id="d00cb-1319">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1319">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="d00cb-1320">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1320">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1321">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1321">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1322">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="d00cb-1322">VM Reapply feature</span></span>
    - <span data-ttu-id="d00cb-1323">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00cb-1323">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="d00cb-1324">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1324">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="d00cb-1325">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-1325">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="d00cb-1326">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00cb-1326">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="d00cb-1327">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-1327">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d00cb-1328">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="d00cb-1328">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="d00cb-1329">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="d00cb-1329">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="d00cb-1330">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d00cb-1330">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="d00cb-1331">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="d00cb-1331">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="d00cb-1332">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-1332">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="d00cb-1333">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="d00cb-1333">Az.DataBoxEdge</span></span>
* <span data-ttu-id="d00cb-1334">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1334">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d00cb-1335">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="d00cb-1335">Get the Order</span></span>
* <span data-ttu-id="d00cb-1336">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1336">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d00cb-1337">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="d00cb-1337">Create new Order</span></span>
* <span data-ttu-id="d00cb-1338">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1338">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="d00cb-1339">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="d00cb-1339">Remove the Order</span></span>
* <span data-ttu-id="d00cb-1340">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="d00cb-1340">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="d00cb-1341">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="d00cb-1341">Now creates Local Share</span></span>
* <span data-ttu-id="d00cb-1342">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1342">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="d00cb-1343">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="d00cb-1343">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="d00cb-1344">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1344">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="d00cb-1345">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1345">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="d00cb-1346">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1346">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d00cb-1347">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1347">Gets the information about Triggers</span></span>
* <span data-ttu-id="d00cb-1348">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1348">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d00cb-1349">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1349">Create new Triggers</span></span>
* <span data-ttu-id="d00cb-1350">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1350">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="d00cb-1351">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1351">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1352">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1353">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1353">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="d00cb-1354">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1354">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-1355">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-1355">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-1356">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="d00cb-1356">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-1357">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1357">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-1358">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="d00cb-1358">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-1359">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1359">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-1360">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-1360">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="d00cb-1361">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-1361">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="d00cb-1362">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="d00cb-1362">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="d00cb-1363">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-1363">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1364">Az.Network</span></span>
* <span data-ttu-id="d00cb-1365">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1365">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="d00cb-1366">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="d00cb-1366">Az.PrivateDns</span></span>
* <span data-ttu-id="d00cb-1367">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1367">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1368">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1368">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1369">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1369">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="d00cb-1370">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1370">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="d00cb-1371">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1371">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d00cb-1372">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d00cb-1372">Az.RedisCache</span></span>
* <span data-ttu-id="d00cb-1373">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1373">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="d00cb-1374">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1374">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="d00cb-1375">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1375">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1376">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1376">Az.Resources</span></span>
- <span data-ttu-id="d00cb-1377">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1377">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="d00cb-1378">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1378">Updated create policy definition help example</span></span>
- <span data-ttu-id="d00cb-1379">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1379">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="d00cb-1380">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1380">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="d00cb-1381">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1381">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1382">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1382">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1383">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1383">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="d00cb-1384">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="d00cb-1384">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="d00cb-1385">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1385">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="d00cb-1386">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-1386">General</span></span>
* <span data-ttu-id="d00cb-1387">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1387">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1388">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1388">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1389">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1389">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d00cb-1390">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1390">Az.Advisor</span></span>
* <span data-ttu-id="d00cb-1391">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1391">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00cb-1392">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-1392">Az.Batch</span></span>
* <span data-ttu-id="d00cb-1393">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1393">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="d00cb-1394">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1394">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="d00cb-1395">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1395">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="d00cb-1396">O parâmetro **New-AzBatchTask** `-ResourceFile` agora usa uma coleção de objetos `PSResourceFile`, que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1396">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="d00cb-1397">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1397">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="d00cb-1398">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1398">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="d00cb-1399">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1399">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="d00cb-1400">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1400">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="d00cb-1401">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1401">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="d00cb-1402">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1402">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d00cb-1403">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1403">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="d00cb-1404">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1404">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="d00cb-1405">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1405">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="d00cb-1406">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1406">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="d00cb-1407">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1407">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="d00cb-1408">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1408">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="d00cb-1409">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1409">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="d00cb-1410">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1410">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="d00cb-1411">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1411">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="d00cb-1412">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1412">This operation is no longer supported.</span></span>
* <span data-ttu-id="d00cb-1413">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1413">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d00cb-1414">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1414">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="d00cb-1415">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1415">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="d00cb-1416">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1416">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="d00cb-1417">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1417">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="d00cb-1418">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1418">New non-verified images are also now returned.</span></span> <span data-ttu-id="d00cb-1419">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1419">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="d00cb-1420">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1420">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="d00cb-1421">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1421">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="d00cb-1422">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1422">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="d00cb-1423">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1423">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="d00cb-1424">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1424">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="d00cb-1425">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1425">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="d00cb-1426">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1426">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="d00cb-1427">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="d00cb-1427">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="d00cb-1428">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="d00cb-1428">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00cb-1429">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-1429">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-1430">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1430">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="d00cb-1431">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1431">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1432">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1432">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1433">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="d00cb-1433">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="d00cb-1434">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1434">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="d00cb-1435">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d00cb-1435">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="d00cb-1436">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1436">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d00cb-1437">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1437">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="d00cb-1438">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="d00cb-1438">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="d00cb-1439">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-1439">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="d00cb-1440">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="d00cb-1440">Breaking changes</span></span>
    - <span data-ttu-id="d00cb-1441">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1441">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="d00cb-1442">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d00cb-1442">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1443">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1443">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1444">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1444">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-1445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-1445">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-1446">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="d00cb-1446">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="d00cb-1447">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1447">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="d00cb-1448">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="d00cb-1448">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="d00cb-1449">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="d00cb-1449">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="d00cb-1450">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="d00cb-1450">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="d00cb-1451">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="d00cb-1451">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-1452">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1452">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-1453">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1453">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-1454">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-1454">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-1455">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1455">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="d00cb-1456">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1456">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="d00cb-1457">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1457">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="d00cb-1458">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1458">Removed five cmdlets:</span></span>
    - <span data-ttu-id="d00cb-1459">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d00cb-1459">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d00cb-1460">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d00cb-1460">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d00cb-1461">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="d00cb-1461">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="d00cb-1462">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00cb-1462">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="d00cb-1463">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00cb-1463">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="d00cb-1464">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1464">Added three cmdlets:</span></span>
    - <span data-ttu-id="d00cb-1465">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1465">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d00cb-1466">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1466">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="d00cb-1467">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1467">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="d00cb-1468">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1468">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="d00cb-1469">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1469">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="d00cb-1470">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1470">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="d00cb-1471">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1471">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="d00cb-1472">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1472">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="d00cb-1473">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1473">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="d00cb-1474">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1474">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="d00cb-1475">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1475">Added some scenario test cases.</span></span>
* <span data-ttu-id="d00cb-1476">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1476">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-1477">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1477">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-1478">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1478">Breaking changes:</span></span>
    - <span data-ttu-id="d00cb-1479">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1479">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d00cb-1480">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1480">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d00cb-1481">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1481">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d00cb-1482">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1482">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d00cb-1483">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1483">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="d00cb-1484">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1484">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="d00cb-1485">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1485">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="d00cb-1486">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1486">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="d00cb-1487">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1487">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d00cb-1488">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1488">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="d00cb-1489">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1489">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="d00cb-1490">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1490">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1491">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1491">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1492">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1492">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="d00cb-1493">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1493">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="d00cb-1494">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1494">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="d00cb-1495">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1495">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="d00cb-1496">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1496">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="d00cb-1497">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1497">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="d00cb-1498">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1498">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="d00cb-1499">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1499">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="d00cb-1500">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="d00cb-1500">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1501">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1502">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="d00cb-1502">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1503">Az.Network</span></span>
* <span data-ttu-id="d00cb-1504">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1504">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="d00cb-1505">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1505">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00cb-1506">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1506">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1507">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1507">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1508">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1508">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1509">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1509">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1510">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1510">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d00cb-1511">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1511">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="d00cb-1512">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1512">New cmdlet:</span></span>
        - <span data-ttu-id="d00cb-1513">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="d00cb-1513">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="d00cb-1514">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1514">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="d00cb-1515">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00cb-1515">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="d00cb-1516">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1516">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="d00cb-1517">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1517">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="d00cb-1518">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1518">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="d00cb-1519">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-1519">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="d00cb-1520">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1520">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="d00cb-1521">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1521">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-1522">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1522">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="d00cb-1523">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-1523">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d00cb-1524">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-1524">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d00cb-1525">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-1525">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="d00cb-1526">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1526">Set-AzVirtualHub</span></span>
* <span data-ttu-id="d00cb-1527">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="d00cb-1527">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="d00cb-1528">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1528">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d00cb-1529">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1529">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d00cb-1530">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1530">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="d00cb-1531">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1531">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="d00cb-1532">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1532">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="d00cb-1533">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1533">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="d00cb-1534">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1534">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-1535">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1535">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="d00cb-1536">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1536">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d00cb-1537">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1537">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d00cb-1538">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1538">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d00cb-1539">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1539">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d00cb-1540">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1540">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="d00cb-1541">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1541">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="d00cb-1542">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="d00cb-1542">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="d00cb-1543">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1543">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-1544">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="d00cb-1544">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="d00cb-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="d00cb-1545">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="d00cb-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d00cb-1546">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="d00cb-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="d00cb-1547">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="d00cb-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-1548">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="d00cb-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1549">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="d00cb-1550">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1550">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d00cb-1551">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1551">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="d00cb-1552">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-1552">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="d00cb-1553">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="d00cb-1553">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="d00cb-1554">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="d00cb-1554">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="d00cb-1555">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1555">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="d00cb-1556">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1556">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="d00cb-1557">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1557">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="d00cb-1558">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="d00cb-1558">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="d00cb-1559">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-1559">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="d00cb-1560">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1560">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="d00cb-1561">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1561">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-1562">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1562">New-AzIpGroup</span></span>
        - <span data-ttu-id="d00cb-1563">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1563">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="d00cb-1564">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1564">Get-AzIpGroup</span></span>
        - <span data-ttu-id="d00cb-1565">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1565">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-1566">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-1566">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-1567">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1567">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1568">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1568">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1569">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1569">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="d00cb-1570">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1570">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="d00cb-1571">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1571">Removed deprecated aliases:</span></span>
* <span data-ttu-id="d00cb-1572">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="d00cb-1572">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="d00cb-1573">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="d00cb-1573">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="d00cb-1574">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1574">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d00cb-1575">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1575">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="d00cb-1576">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="d00cb-1576">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="d00cb-1577">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1577">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1578">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1578">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1579">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-1579">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="d00cb-1580">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-1580">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d00cb-1581">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-1581">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d00cb-1582">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="d00cb-1582">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="d00cb-1583">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d00cb-1583">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="d00cb-1584">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d00cb-1584">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="d00cb-1585">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1585">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="d00cb-1586">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-1586">General</span></span>
* <span data-ttu-id="d00cb-1587">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1587">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1588">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1589">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1589">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-1590">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-1590">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-1591">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1591">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="d00cb-1592">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="d00cb-1592">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-1593">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1593">Az.Automation</span></span>
* <span data-ttu-id="d00cb-1594">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1594">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00cb-1595">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-1595">Az.Batch</span></span>
* <span data-ttu-id="d00cb-1596">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1596">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1597">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1597">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1598">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-1598">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="d00cb-1599">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d00cb-1599">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="d00cb-1600">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1600">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="d00cb-1601">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1601">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1602">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1602">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1603">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1603">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="d00cb-1604">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1604">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="d00cb-1605">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1605">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-1606">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-1606">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-1607">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="d00cb-1607">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="d00cb-1608">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="d00cb-1608">Az.HealthcareApis</span></span>
* <span data-ttu-id="d00cb-1609">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1609">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="d00cb-1610">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="d00cb-1610">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="d00cb-1611">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="d00cb-1611">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="d00cb-1612">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1612">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-1613">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1613">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-1614">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="d00cb-1614">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="d00cb-1615">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="d00cb-1615">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-1616">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1616">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-1617">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="d00cb-1617">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="d00cb-1618">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1618">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="d00cb-1619">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="d00cb-1619">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="d00cb-1620">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1620">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1621">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1621">Az.Network</span></span>
* <span data-ttu-id="d00cb-1622">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1622">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="d00cb-1623">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d00cb-1623">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="d00cb-1624">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1624">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-1625">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1625">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="d00cb-1626">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1626">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d00cb-1627">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="d00cb-1627">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="d00cb-1628">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1628">Updated cmdlets:</span></span>
        - <span data-ttu-id="d00cb-1629">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1629">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00cb-1630">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1630">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00cb-1631">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1631">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d00cb-1632">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="d00cb-1632">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="d00cb-1633">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="d00cb-1633">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="d00cb-1634">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1634">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="d00cb-1635">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1635">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d00cb-1636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d00cb-1636">Az.RedisCache</span></span>
* <span data-ttu-id="d00cb-1637">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1637">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1638">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1639">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="d00cb-1639">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1640">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1640">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1641">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-1641">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="d00cb-1642">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="d00cb-1642">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d00cb-1643">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d00cb-1643">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="d00cb-1644">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="d00cb-1644">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="d00cb-1645">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-1645">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00cb-1646">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00cb-1646">Az.StorageSync</span></span>
* <span data-ttu-id="d00cb-1647">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1647">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-1648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-1648">Az.Websites</span></span>
* <span data-ttu-id="d00cb-1649">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="d00cb-1649">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="d00cb-1650">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1650">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-1651">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-1651">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-1652">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1652">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="d00cb-1653">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1653">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="d00cb-1654">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1654">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-1655">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1655">Az.Automation</span></span>
* <span data-ttu-id="d00cb-1656">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1656">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="d00cb-1657">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="d00cb-1657">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="d00cb-1658">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1658">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1659">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1659">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1660">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1660">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="d00cb-1661">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1661">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d00cb-1662">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1662">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="d00cb-1663">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1663">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="d00cb-1664">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1664">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="d00cb-1665">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1665">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="d00cb-1666">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1666">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="d00cb-1667">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1667">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="d00cb-1668">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1668">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1669">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1669">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1670">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="d00cb-1670">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="d00cb-1671">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="d00cb-1671">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-1672">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-1672">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-1673">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="d00cb-1673">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-1674">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1674">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-1675">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1675">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="d00cb-1676">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1676">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="d00cb-1677">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1677">New cmdlets are:</span></span>
    - <span data-ttu-id="d00cb-1678">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00cb-1678">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d00cb-1679">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00cb-1679">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d00cb-1680">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00cb-1680">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="d00cb-1681">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="d00cb-1681">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-1682">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1682">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-1683">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="d00cb-1683">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="d00cb-1684">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1684">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="d00cb-1685">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1685">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="d00cb-1686">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1686">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="d00cb-1687">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1687">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="d00cb-1688">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1688">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="d00cb-1689">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1689">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="d00cb-1690">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1690">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="d00cb-1691">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1691">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d00cb-1692">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1692">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="d00cb-1693">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1693">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="d00cb-1694">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1694">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="d00cb-1695">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="d00cb-1695">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="d00cb-1696">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="d00cb-1696">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="d00cb-1697">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="d00cb-1697">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="d00cb-1698">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="d00cb-1698">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="d00cb-1699">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="d00cb-1699">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="d00cb-1700">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-1700">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="d00cb-1701">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1701">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="d00cb-1702">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-1702">Overall improved help files</span></span>
* <span data-ttu-id="d00cb-1703">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1703">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1704">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1704">Az.Network</span></span>
* <span data-ttu-id="d00cb-1705">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1705">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="d00cb-1706">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="d00cb-1706">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="d00cb-1707">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="d00cb-1707">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="d00cb-1708">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="d00cb-1708">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="d00cb-1709">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="d00cb-1709">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="d00cb-1710">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="d00cb-1710">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="d00cb-1711">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1711">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="d00cb-1712">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d00cb-1712">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="d00cb-1713">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-1713">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="d00cb-1714">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1714">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="d00cb-1715">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-1715">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="d00cb-1716">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="d00cb-1716">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="d00cb-1717">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d00cb-1717">New cmdlets</span></span>
        - <span data-ttu-id="d00cb-1718">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d00cb-1718">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="d00cb-1719">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1719">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="d00cb-1720">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1720">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00cb-1721">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d00cb-1721">New-VpnSite</span></span>
        - <span data-ttu-id="d00cb-1722">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="d00cb-1722">Update-VpnSite</span></span>
        - <span data-ttu-id="d00cb-1723">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1723">New-VpnConnection</span></span>
        - <span data-ttu-id="d00cb-1724">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1724">Update-VpnConnection</span></span>
* <span data-ttu-id="d00cb-1725">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="d00cb-1725">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1726">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1726">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1727">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="d00cb-1727">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="d00cb-1728">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="d00cb-1728">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1729">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1730">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1730">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-1731">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-1731">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-1732">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1732">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="d00cb-1733">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1733">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="d00cb-1734">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00cb-1734">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00cb-1735">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d00cb-1735">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d00cb-1736">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d00cb-1736">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d00cb-1737">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d00cb-1737">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="d00cb-1738">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00cb-1738">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00cb-1739">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00cb-1739">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00cb-1740">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d00cb-1740">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d00cb-1741">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d00cb-1741">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d00cb-1742">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="d00cb-1742">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="d00cb-1743">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="d00cb-1743">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="d00cb-1744">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d00cb-1744">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="d00cb-1745">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="d00cb-1745">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="d00cb-1746">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="d00cb-1746">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="d00cb-1747">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1747">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d00cb-1748">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d00cb-1748">Az.SignalR</span></span>
* <span data-ttu-id="d00cb-1749">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1749">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1750">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1750">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1751">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1751">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="d00cb-1752">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="d00cb-1752">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="d00cb-1753">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1753">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="d00cb-1754">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1754">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="d00cb-1755">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="d00cb-1755">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1756">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1756">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1757">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1757">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="d00cb-1758">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="d00cb-1758">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="d00cb-1759">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-1759">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="d00cb-1760">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-1760">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="d00cb-1761">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1761">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="d00cb-1762">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-1762">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="d00cb-1763">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-1763">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="d00cb-1764">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-1764">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d00cb-1765">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-1765">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d00cb-1766">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-1766">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="d00cb-1767">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-1767">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-1768">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-1768">Az.Websites</span></span>
* <span data-ttu-id="d00cb-1769">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="d00cb-1769">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="d00cb-1770">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="d00cb-1770">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="d00cb-1771">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1771">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="d00cb-1772">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1772">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="d00cb-1773">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-1773">General</span></span>
* <span data-ttu-id="d00cb-1774">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1774">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1775">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1775">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1776">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="d00cb-1776">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00cb-1777">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00cb-1777">Az.Aks</span></span>
* <span data-ttu-id="d00cb-1778">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1778">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="d00cb-1779">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="d00cb-1779">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-1780">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-1780">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-1781">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="d00cb-1781">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="d00cb-1782">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="d00cb-1782">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="d00cb-1783">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1783">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="d00cb-1784">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="d00cb-1784">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="d00cb-1785">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1785">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00cb-1786">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-1786">Az.Batch</span></span>
* <span data-ttu-id="d00cb-1787">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="d00cb-1787">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00cb-1788">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-1788">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-1789">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="d00cb-1789">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1790">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1790">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1791">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1791">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="d00cb-1792">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-1792">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="d00cb-1793">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="d00cb-1793">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="d00cb-1794">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1794">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="d00cb-1795">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="d00cb-1795">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="d00cb-1796">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00cb-1796">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="d00cb-1797">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="d00cb-1797">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="d00cb-1798">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1798">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1799">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1800">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1800">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="d00cb-1801">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="d00cb-1801">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="d00cb-1802">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="d00cb-1802">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="d00cb-1803">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="d00cb-1803">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-1804">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-1804">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-1805">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1805">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-1806">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1806">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-1807">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1807">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="d00cb-1808">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="d00cb-1808">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="d00cb-1809">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d00cb-1809">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="d00cb-1810">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="d00cb-1810">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="d00cb-1811">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d00cb-1811">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d00cb-1812">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="d00cb-1812">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-1813">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1813">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-1814">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-1814">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1815">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1815">Az.Network</span></span>
* <span data-ttu-id="d00cb-1816">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1816">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="d00cb-1817">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1817">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="d00cb-1818">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1818">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="d00cb-1819">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="d00cb-1819">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="d00cb-1820">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1820">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="d00cb-1821">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1821">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="d00cb-1822">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d00cb-1822">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-1823">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-1823">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-1824">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1824">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="d00cb-1825">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1825">Added example</span></span>
    - <span data-ttu-id="d00cb-1826">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1826">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="d00cb-1827">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d00cb-1827">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="d00cb-1828">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="d00cb-1828">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1829">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1830">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1830">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1831">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1831">Az.Resources</span></span>
* <span data-ttu-id="d00cb-1832">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="d00cb-1832">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="d00cb-1833">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="d00cb-1833">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="d00cb-1834">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="d00cb-1834">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="d00cb-1835">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-1835">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00cb-1836">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00cb-1836">Az.ServiceBus</span></span>
* <span data-ttu-id="d00cb-1837">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-1837">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="d00cb-1838">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="d00cb-1838">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="d00cb-1839">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="d00cb-1839">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-1840">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-1840">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-1841">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1841">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="d00cb-1842">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1842">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="d00cb-1843">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="d00cb-1843">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="d00cb-1844">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1844">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="d00cb-1845">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="d00cb-1845">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="d00cb-1846">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="d00cb-1846">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1847">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1848">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1848">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1849">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1849">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1850">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="d00cb-1850">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="d00cb-1851">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="d00cb-1851">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="d00cb-1852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-1852">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="d00cb-1853">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1853">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="d00cb-1854">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="d00cb-1854">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="d00cb-1855">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1855">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-1856">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-1856">Az.Websites</span></span>
* <span data-ttu-id="d00cb-1857">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d00cb-1857">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="d00cb-1858">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1858">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1859">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1859">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1860">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00cb-1860">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="d00cb-1861">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-1861">Az.ApplicationInsights</span></span>
* <span data-ttu-id="d00cb-1862">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1862">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-1863">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1863">Az.Automation</span></span>
* <span data-ttu-id="d00cb-1864">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="d00cb-1864">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-1865">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1865">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-1866">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1866">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1867">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1868">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1868">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d00cb-1869">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d00cb-1869">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d00cb-1870">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="d00cb-1870">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="d00cb-1871">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="d00cb-1871">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1872">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1872">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1873">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-1873">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="d00cb-1874">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="d00cb-1874">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-1875">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1875">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-1876">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d00cb-1876">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d00cb-1877">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="d00cb-1877">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-1878">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-1878">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-1879">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1879">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00cb-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-1880">Az.LogicApp</span></span>
* <span data-ttu-id="d00cb-1881">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="d00cb-1881">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="d00cb-1882">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="d00cb-1882">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="d00cb-1883">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1883">Az.ManagedServices</span></span>
* <span data-ttu-id="d00cb-1884">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="d00cb-1884">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1885">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1885">Az.Network</span></span>
* <span data-ttu-id="d00cb-1886">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1886">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="d00cb-1887">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d00cb-1887">New cmdlets</span></span>
        - <span data-ttu-id="d00cb-1888">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00cb-1888">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00cb-1889">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00cb-1889">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d00cb-1890">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1890">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1891">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1891">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1892">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1892">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1893">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1893">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="d00cb-1894">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="d00cb-1894">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="d00cb-1895">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00cb-1895">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="d00cb-1896">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="d00cb-1896">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="d00cb-1897">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="d00cb-1897">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="d00cb-1898">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1898">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="d00cb-1899">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1899">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="d00cb-1900">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="d00cb-1900">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="d00cb-1901">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="d00cb-1901">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="d00cb-1902">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1902">Updated cmdlets</span></span>
        - <span data-ttu-id="d00cb-1903">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1903">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00cb-1904">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1904">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="d00cb-1905">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1905">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="d00cb-1906">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-1906">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="d00cb-1907">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-1907">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="d00cb-1908">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d00cb-1908">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00cb-1909">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1909">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d00cb-1910">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1910">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="d00cb-1911">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1911">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="d00cb-1912">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="d00cb-1912">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="d00cb-1913">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1913">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="d00cb-1914">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1914">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-1915">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-1915">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-1916">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1916">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="d00cb-1917">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="d00cb-1917">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1918">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1918">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1919">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1919">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d00cb-1920">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1920">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="d00cb-1921">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1921">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="d00cb-1922">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1922">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="d00cb-1923">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1923">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="d00cb-1924">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1924">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d00cb-1925">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1925">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="d00cb-1926">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1926">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="d00cb-1927">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-1927">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="d00cb-1928">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1928">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1929">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1929">Az.Resources</span></span>
- <span data-ttu-id="d00cb-1930">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1930">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="d00cb-1931">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d00cb-1931">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00cb-1932">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00cb-1932">Az.ServiceBus</span></span>
* <span data-ttu-id="d00cb-1933">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="d00cb-1933">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="d00cb-1934">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="d00cb-1934">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1935">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1935">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1936">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d00cb-1936">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="d00cb-1937">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="d00cb-1937">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="d00cb-1938">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1938">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-1939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-1939">Az.Storage</span></span>
* <span data-ttu-id="d00cb-1940">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="d00cb-1940">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00cb-1941">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00cb-1941">Az.StorageSync</span></span>
* <span data-ttu-id="d00cb-1942">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1942">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="d00cb-1943">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="d00cb-1943">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-1944">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-1944">Az.Websites</span></span>
* <span data-ttu-id="d00cb-1945">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-1945">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="d00cb-1946">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-1946">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="d00cb-1947">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="d00cb-1947">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="d00cb-1948">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-1948">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-1949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-1949">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-1950">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="d00cb-1950">Add support for profile cmdlets</span></span>
* <span data-ttu-id="d00cb-1951">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="d00cb-1951">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="d00cb-1952">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d00cb-1952">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="d00cb-1953">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1953">Az.Advisor</span></span>
* <span data-ttu-id="d00cb-1954">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="d00cb-1954">GA release of Az.Advisor</span></span>
* <span data-ttu-id="d00cb-1955">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="d00cb-1955">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-1956">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-1956">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-1957">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="d00cb-1957">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="d00cb-1958">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d00cb-1958">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="d00cb-1959">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="d00cb-1959">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="d00cb-1960">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1960">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="d00cb-1961">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="d00cb-1961">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="d00cb-1962">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00cb-1962">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="d00cb-1963">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="d00cb-1963">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-1964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-1964">Az.Automation</span></span>
* <span data-ttu-id="d00cb-1965">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1965">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-1966">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-1966">Az.Compute</span></span>
* <span data-ttu-id="d00cb-1967">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-1967">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-1968">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-1968">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-1969">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1969">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00cb-1970">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00cb-1970">Az.EventGrid</span></span>
* <span data-ttu-id="d00cb-1971">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1971">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-1972">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-1972">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-1973">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1973">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-1974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-1974">Az.Network</span></span>
* <span data-ttu-id="d00cb-1975">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="d00cb-1975">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="d00cb-1976">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="d00cb-1976">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-1977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-1977">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-1978">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="d00cb-1978">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="d00cb-1979">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="d00cb-1979">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-1980">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-1980">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-1981">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="d00cb-1981">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-1983">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="d00cb-1983">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-1984">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-1984">Az.Resources</span></span>
    - <span data-ttu-id="d00cb-1985">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="d00cb-1985">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="d00cb-1986">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="d00cb-1986">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="d00cb-1987">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-1987">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="d00cb-1988">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="d00cb-1988">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00cb-1989">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00cb-1989">Az.ServiceBus</span></span>
* <span data-ttu-id="d00cb-1990">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="d00cb-1990">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-1991">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-1991">Az.Sql</span></span>
* <span data-ttu-id="d00cb-1992">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="d00cb-1992">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="d00cb-1993">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d00cb-1993">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="d00cb-1994">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d00cb-1994">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d00cb-1995">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d00cb-1995">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d00cb-1996">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="d00cb-1996">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="d00cb-1997">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d00cb-1997">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d00cb-1998">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d00cb-1998">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="d00cb-1999">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="d00cb-1999">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="d00cb-2000">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="d00cb-2000">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2001">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2001">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2002">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2002">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="d00cb-2003">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d00cb-2003">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="d00cb-2004">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2004">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="d00cb-2005">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="d00cb-2005">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="d00cb-2006">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2006">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="d00cb-2007">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2007">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="d00cb-2008">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2008">Set-AzStorageAccount</span></span>
* <span data-ttu-id="d00cb-2009">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2009">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="d00cb-2010">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d00cb-2010">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="d00cb-2011">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="d00cb-2011">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="d00cb-2012">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="d00cb-2012">Az.StorageSync</span></span>
* <span data-ttu-id="d00cb-2013">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="d00cb-2013">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="d00cb-2014">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2014">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2015">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2015">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2016">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="d00cb-2016">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="d00cb-2017">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="d00cb-2017">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="d00cb-2018">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="d00cb-2018">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="d00cb-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d00cb-2019">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="d00cb-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="d00cb-2020">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2021">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2021">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2022">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2022">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="d00cb-2023">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2023">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="d00cb-2024">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d00cb-2024">Az.Dns</span></span>
* <span data-ttu-id="d00cb-2025">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2025">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00cb-2026">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00cb-2026">Az.EventGrid</span></span>
* <span data-ttu-id="d00cb-2027">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2027">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="d00cb-2028">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2028">New cmdlets:</span></span>
    - <span data-ttu-id="d00cb-2029">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d00cb-2029">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d00cb-2030">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2030">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d00cb-2031">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d00cb-2031">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d00cb-2032">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2032">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="d00cb-2033">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="d00cb-2033">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="d00cb-2034">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2034">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d00cb-2035">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d00cb-2035">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d00cb-2036">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2036">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="d00cb-2037">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="d00cb-2037">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="d00cb-2038">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2038">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="d00cb-2039">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2039">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d00cb-2040">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2040">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="d00cb-2041">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="d00cb-2041">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="d00cb-2042">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="d00cb-2042">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="d00cb-2043">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2043">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="d00cb-2044">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2044">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="d00cb-2045">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2045">Updated cmdlets:</span></span>
    - <span data-ttu-id="d00cb-2046">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2046">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="d00cb-2047">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2047">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d00cb-2048">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2048">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="d00cb-2049">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="d00cb-2049">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="d00cb-2050">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2050">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="d00cb-2051">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="d00cb-2051">Event subscription expiration date,</span></span>
            - <span data-ttu-id="d00cb-2052">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2052">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="d00cb-2053">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2053">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="d00cb-2054">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="d00cb-2054">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="d00cb-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2055">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="d00cb-2056">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2056">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="d00cb-2057">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="d00cb-2057">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="d00cb-2058">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2058">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="d00cb-2059">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2059">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-2060">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2060">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-2061">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-2061">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="d00cb-2062">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="d00cb-2062">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="d00cb-2063">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-2063">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="d00cb-2064">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="d00cb-2064">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2065">Az.Network</span></span>
* <span data-ttu-id="d00cb-2066">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="d00cb-2066">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="d00cb-2067">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d00cb-2067">New cmdlets</span></span>
        - <span data-ttu-id="d00cb-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="d00cb-2068">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="d00cb-2069">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d00cb-2069">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="d00cb-2070">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d00cb-2070">New cmdlets</span></span>
        - <span data-ttu-id="d00cb-2071">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d00cb-2071">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="d00cb-2072">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00cb-2072">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="d00cb-2073">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d00cb-2073">New cmdlets</span></span>
        - <span data-ttu-id="d00cb-2074">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00cb-2074">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d00cb-2075">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00cb-2075">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d00cb-2076">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d00cb-2076">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="d00cb-2077">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2077">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="d00cb-2078">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-2078">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="d00cb-2079">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00cb-2079">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="d00cb-2080">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d00cb-2080">New cmdlets</span></span>
        - <span data-ttu-id="d00cb-2081">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00cb-2081">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00cb-2082">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00cb-2082">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00cb-2083">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="d00cb-2083">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="d00cb-2084">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-2084">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="d00cb-2085">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="d00cb-2085">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="d00cb-2086">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2086">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="d00cb-2087">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2087">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="d00cb-2088">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2088">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="d00cb-2089">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2089">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="d00cb-2090">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d00cb-2090">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="d00cb-2091">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2091">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="d00cb-2092">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2092">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="d00cb-2093">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2093">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="d00cb-2094">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2094">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="d00cb-2095">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d00cb-2095">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="d00cb-2096">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="d00cb-2096">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="d00cb-2097">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="d00cb-2097">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="d00cb-2098">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2098">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="d00cb-2099">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2099">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="d00cb-2100">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="d00cb-2100">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="d00cb-2101">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d00cb-2101">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="d00cb-2102">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="d00cb-2102">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="d00cb-2103">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d00cb-2103">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="d00cb-2104">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2104">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="d00cb-2105">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2105">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d00cb-2106">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2106">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="d00cb-2107">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2107">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-2108">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2108">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-2109">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2109">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2110">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2110">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2111">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2111">Support for additional Template Export options</span></span>
    - <span data-ttu-id="d00cb-2112">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-2112">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d00cb-2113">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-2113">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="d00cb-2114">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2114">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-2115">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2115">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-2116">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2116">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2117">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2117">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2118">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d00cb-2118">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="d00cb-2119">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d00cb-2119">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="d00cb-2120">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2120">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="d00cb-2121">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d00cb-2121">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d00cb-2122">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d00cb-2122">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d00cb-2123">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d00cb-2123">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="d00cb-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d00cb-2124">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="d00cb-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="d00cb-2125">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2126">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2126">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2127">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-2127">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="d00cb-2128">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2128">New-AzStorageAccount</span></span>
* <span data-ttu-id="d00cb-2129">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="d00cb-2129">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="d00cb-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2130">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2131">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2131">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2132">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="d00cb-2132">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="d00cb-2133">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="d00cb-2133">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="d00cb-2134">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2134">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="d00cb-2135">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-2135">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-2136">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2136">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2137">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2137">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2138">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2138">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="d00cb-2139">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00cb-2139">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-2140">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2140">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-2141">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2141">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="d00cb-2142">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00cb-2142">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2143">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2143">Az.Network</span></span>
* <span data-ttu-id="d00cb-2144">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="d00cb-2144">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="d00cb-2145">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="d00cb-2145">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-2146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2146">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-2147">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="d00cb-2147">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2148">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-2149">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="d00cb-2149">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00cb-2150">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00cb-2150">Az.ServiceBus</span></span>
* <span data-ttu-id="d00cb-2151">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d00cb-2151">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-2152">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2152">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-2153">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2153">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="d00cb-2154">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2154">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2155">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2155">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2156">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2156">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="d00cb-2157">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2157">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="d00cb-2158">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="d00cb-2158">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="d00cb-2159">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2159">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2160">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2160">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2161">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2161">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="d00cb-2162">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2162">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="d00cb-2163">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-2163">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-2164">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2164">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="d00cb-2165">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2165">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="d00cb-2166">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2166">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="d00cb-2167">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2167">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="d00cb-2168">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2168">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="d00cb-2169">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="d00cb-2169">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="d00cb-2170">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2170">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="d00cb-2171">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2171">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="d00cb-2172">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-2172">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="d00cb-2173">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="d00cb-2173">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="d00cb-2174">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2174">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="d00cb-2175">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="d00cb-2175">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="d00cb-2176">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="d00cb-2176">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="d00cb-2177">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2177">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="d00cb-2178">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2178">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="d00cb-2179">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2179">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="d00cb-2180">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2180">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="d00cb-2181">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="d00cb-2181">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="d00cb-2182">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2182">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="d00cb-2183">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="d00cb-2183">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="d00cb-2184">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="d00cb-2184">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="d00cb-2185">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2185">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="d00cb-2186">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2186">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="d00cb-2187">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-2187">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="d00cb-2188">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2188">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="d00cb-2189">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2189">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="d00cb-2190">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2190">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="d00cb-2191">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2191">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="d00cb-2192">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2192">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="d00cb-2193">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="d00cb-2193">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="d00cb-2194">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2194">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="d00cb-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="d00cb-2195">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="d00cb-2196">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2196">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="d00cb-2197">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00cb-2197">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d00cb-2198">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2198">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="d00cb-2199">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="d00cb-2199">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="d00cb-2200">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2200">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="d00cb-2201">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2201">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="d00cb-2202">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2202">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="d00cb-2203">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00cb-2203">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d00cb-2204">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2204">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d00cb-2205">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2205">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d00cb-2206">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2206">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="d00cb-2207">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2207">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d00cb-2208">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="d00cb-2208">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="d00cb-2209">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2209">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="d00cb-2210">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2210">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="d00cb-2211">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2211">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="d00cb-2212">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="d00cb-2212">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="d00cb-2213">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2213">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="d00cb-2214">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2214">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="d00cb-2215">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2215">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="d00cb-2216">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2216">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="d00cb-2217">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="d00cb-2217">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="d00cb-2218">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2218">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="d00cb-2219">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2219">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="d00cb-2220">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d00cb-2220">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d00cb-2221">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2221">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d00cb-2222">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2222">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d00cb-2223">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2223">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d00cb-2224">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="d00cb-2224">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="d00cb-2225">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2225">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="d00cb-2226">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2226">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="d00cb-2227">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2227">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="d00cb-2228">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="d00cb-2228">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="d00cb-2229">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2229">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="d00cb-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="d00cb-2230">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="d00cb-2231">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2231">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="d00cb-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="d00cb-2232">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="d00cb-2233">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2233">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="d00cb-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="d00cb-2234">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="d00cb-2235">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2235">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="d00cb-2236">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2236">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="d00cb-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2237">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="d00cb-2238">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2238">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="d00cb-2239">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2239">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="d00cb-2240">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2240">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-2241">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2241">Az.Automation</span></span>
* <span data-ttu-id="d00cb-2242">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2242">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="d00cb-2243">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="d00cb-2243">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="d00cb-2244">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="d00cb-2244">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="d00cb-2245">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2245">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="d00cb-2246">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="d00cb-2246">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="d00cb-2247">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2247">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="d00cb-2248">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2248">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2249">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2250">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2250">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="d00cb-2251">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2251">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2252">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-2253">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2253">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-2254">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2254">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-2255">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-2255">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2256">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2256">Az.Network</span></span>
* <span data-ttu-id="d00cb-2257">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2257">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="d00cb-2258">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2258">Updated cmdlet:</span></span>
        - <span data-ttu-id="d00cb-2259">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-2259">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="d00cb-2260">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d00cb-2260">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2261">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2261">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2262">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="d00cb-2262">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2263">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2263">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2264">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="d00cb-2264">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="d00cb-2265">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2265">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2266">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2266">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2267">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="d00cb-2267">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-2268">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2268">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-2269">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2269">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="d00cb-2270">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2270">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2271">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2271">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2272">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2272">Proximity placement group feature.</span></span>
    - <span data-ttu-id="d00cb-2273">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-2273">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="d00cb-2274">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2274">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="d00cb-2275">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2275">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="d00cb-2276">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2276">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="d00cb-2277">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-2277">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="d00cb-2278">Alterações de quebra</span><span class="sxs-lookup"><span data-stu-id="d00cb-2278">Breaking changes</span></span>
    - <span data-ttu-id="d00cb-2279">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2279">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="d00cb-2280">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2280">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="d00cb-2281">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="d00cb-2281">Az.DeploymentManager</span></span>
* <span data-ttu-id="d00cb-2282">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2282">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="d00cb-2283">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="d00cb-2283">Az.Dns</span></span>
* <span data-ttu-id="d00cb-2284">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="d00cb-2284">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="d00cb-2285">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2285">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="d00cb-2286">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2286">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-2287">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2287">Az.FrontDoor</span></span>
* <span data-ttu-id="d00cb-2288">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2288">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="d00cb-2289">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2289">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-2290">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-2290">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-2291">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2291">Removed two cmdlets:</span></span>
    - <span data-ttu-id="d00cb-2292">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00cb-2292">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="d00cb-2293">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00cb-2293">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d00cb-2294">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d00cb-2294">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="d00cb-2295">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2295">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="d00cb-2296">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2296">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="d00cb-2297">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2297">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-2298">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2298">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-2299">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="d00cb-2299">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="d00cb-2300">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="d00cb-2300">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="d00cb-2301">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-2301">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="d00cb-2302">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="d00cb-2302">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="d00cb-2303">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2303">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="d00cb-2304">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="d00cb-2304">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="d00cb-2305">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="d00cb-2305">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="d00cb-2306">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2306">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00cb-2307">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2307">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00cb-2308">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2308">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00cb-2309">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2309">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00cb-2310">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2310">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="d00cb-2311">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="d00cb-2311">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="d00cb-2312">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d00cb-2312">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2313">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2313">Az.Network</span></span>
* <span data-ttu-id="d00cb-2314">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="d00cb-2314">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="d00cb-2315">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="d00cb-2315">New cmdlets</span></span>
        - <span data-ttu-id="d00cb-2316">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00cb-2316">New-AzNatGateway</span></span>
        - <span data-ttu-id="d00cb-2317">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00cb-2317">Get-AzNatGateway</span></span>
        - <span data-ttu-id="d00cb-2318">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00cb-2318">Set-AzNatGateway</span></span>
        - <span data-ttu-id="d00cb-2319">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d00cb-2319">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="d00cb-2320">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2320">Updated cmdlets</span></span>
        - <span data-ttu-id="d00cb-2321">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d00cb-2321">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="d00cb-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="d00cb-2322">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="d00cb-2323">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2323">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="d00cb-2324">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2324">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="d00cb-2325">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2325">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-2326">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2326">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-2327">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2327">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="d00cb-2328">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2328">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="d00cb-2329">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2329">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2330">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2330">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-2331">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2331">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="d00cb-2332">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2332">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="d00cb-2333">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2333">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="d00cb-2334">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2334">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="d00cb-2335">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2335">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="d00cb-2336">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2336">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="d00cb-2337">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d00cb-2337">Az.Relay</span></span>
* <span data-ttu-id="d00cb-2338">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="d00cb-2338">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00cb-2339">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00cb-2339">Az.ServiceBus</span></span>
* <span data-ttu-id="d00cb-2340">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d00cb-2340">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2341">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2342">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="d00cb-2342">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="d00cb-2343">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2343">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="d00cb-2344">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2344">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="d00cb-2345">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2345">New-AzStorageAccount</span></span>
* <span data-ttu-id="d00cb-2346">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2346">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="d00cb-2347">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2347">New-AzStorageAccount</span></span>
    - <span data-ttu-id="d00cb-2348">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2348">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="d00cb-2349">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2349">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2350">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2350">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2351">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-2351">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="d00cb-2352">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2352">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="d00cb-2353">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2353">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00cb-2354">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d00cb-2354">Highlights since the last major release</span></span>
* <span data-ttu-id="d00cb-2355">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d00cb-2355">General availability of `Az` module</span></span>
* <span data-ttu-id="d00cb-2356">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d00cb-2356">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d00cb-2357">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d00cb-2357">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d00cb-2358">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2358">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d00cb-2359">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d00cb-2359">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00cb-2360">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2360">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d00cb-2361">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d00cb-2361">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2362">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2362">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2363">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="d00cb-2363">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="d00cb-2364">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-2364">Az.Batch</span></span>
* <span data-ttu-id="d00cb-2365">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00cb-2366">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-2366">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-2367">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-2368">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2368">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-2369">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2370">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2370">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2371">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2371">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="d00cb-2372">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00cb-2373">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d00cb-2373">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-2374">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-2374">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-2375">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2375">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2376">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2376">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-2377">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2377">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00cb-2378">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00cb-2378">Az.EventGrid</span></span>
* <span data-ttu-id="d00cb-2379">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2379">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-2380">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2380">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-2381">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="d00cb-2381">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="d00cb-2382">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="d00cb-2382">Az.HDInsight</span></span>
* <span data-ttu-id="d00cb-2383">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-2384">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2384">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-2385">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2385">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-2386">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-2386">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-2387">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00cb-2388">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d00cb-2388">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="d00cb-2389">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d00cb-2389">Az.MachineLearning</span></span>
* <span data-ttu-id="d00cb-2390">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2390">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="d00cb-2391">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d00cb-2391">Az.Media</span></span>
* <span data-ttu-id="d00cb-2392">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-2393">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2393">Az.Monitor</span></span>
  * <span data-ttu-id="d00cb-2394">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="d00cb-2394">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="d00cb-2395">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d00cb-2395">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="d00cb-2396">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d00cb-2396">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="d00cb-2397">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d00cb-2397">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d00cb-2398">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d00cb-2398">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="d00cb-2399">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="d00cb-2399">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="d00cb-2400">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="d00cb-2400">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2401">Az.Network</span></span>
* <span data-ttu-id="d00cb-2402">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00cb-2403">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d00cb-2403">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="d00cb-2404">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="d00cb-2404">Az.NotificationHubs</span></span>
* <span data-ttu-id="d00cb-2405">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-2406">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2406">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-2407">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="d00cb-2408">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="d00cb-2408">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="d00cb-2409">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2409">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2410">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2410">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-2411">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2411">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00cb-2412">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2412">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="d00cb-2413">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="d00cb-2413">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="d00cb-2414">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="d00cb-2414">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d00cb-2415">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d00cb-2415">Az.RedisCache</span></span>
* <span data-ttu-id="d00cb-2416">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2416">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2417">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2417">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2418">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d00cb-2418">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2419">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2419">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2420">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="d00cb-2420">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="d00cb-2421">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2421">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00cb-2422">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2422">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="d00cb-2423">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2423">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="d00cb-2424">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2424">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="d00cb-2425">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2425">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="d00cb-2426">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="d00cb-2426">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2427">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2427">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2428">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="d00cb-2428">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="d00cb-2429">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="d00cb-2430">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2430">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="d00cb-2431">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2431">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="d00cb-2432">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2432">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00cb-2433">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d00cb-2433">Highlights since the last major release</span></span>
* <span data-ttu-id="d00cb-2434">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d00cb-2434">General availability of `Az` module</span></span>
* <span data-ttu-id="d00cb-2435">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d00cb-2435">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d00cb-2436">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d00cb-2436">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d00cb-2437">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2437">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d00cb-2438">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d00cb-2438">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00cb-2439">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2439">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d00cb-2440">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d00cb-2440">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2441">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2441">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2442">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d00cb-2442">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00cb-2443">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2443">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00cb-2444">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="d00cb-2444">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="d00cb-2445">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="d00cb-2445">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-2446">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2446">Az.Automation</span></span>
* <span data-ttu-id="d00cb-2447">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2447">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="d00cb-2448">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2448">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="d00cb-2449">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2449">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2450">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2450">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2451">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2451">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="d00cb-2452">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2452">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="d00cb-2453">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-2453">Az.ContainerInstance</span></span>
* <span data-ttu-id="d00cb-2454">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="d00cb-2454">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-2455">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-2455">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-2456">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="d00cb-2456">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="d00cb-2457">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2457">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2458">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2459">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="d00cb-2459">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="d00cb-2460">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2460">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="d00cb-2461">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="d00cb-2461">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="d00cb-2462">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d00cb-2462">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="d00cb-2463">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="d00cb-2463">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="d00cb-2464">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="d00cb-2464">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2465">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2465">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2466">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2466">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2467">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2467">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2468">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2468">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="d00cb-2469">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d00cb-2469">New-AzStorageContext</span></span>
* <span data-ttu-id="d00cb-2470">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-2470">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="d00cb-2471">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d00cb-2471">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d00cb-2472">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d00cb-2472">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="d00cb-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2473">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="d00cb-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2474">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="d00cb-2475">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2475">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="d00cb-2476">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-2476">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d00cb-2477">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-2477">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="d00cb-2478">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-2478">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="d00cb-2479">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d00cb-2479">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="d00cb-2480">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2480">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="d00cb-2481">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="d00cb-2481">Highlights since the last major release</span></span>
* <span data-ttu-id="d00cb-2482">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="d00cb-2482">General availability of `Az` module</span></span>
* <span data-ttu-id="d00cb-2483">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="d00cb-2483">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="d00cb-2484">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="d00cb-2484">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="d00cb-2485">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2485">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="d00cb-2486">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d00cb-2486">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00cb-2487">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2487">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="d00cb-2488">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="d00cb-2488">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-2489">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2489">Az.Automation</span></span>
* <span data-ttu-id="d00cb-2490">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2490">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="d00cb-2491">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="d00cb-2491">Dynamic grouping</span></span>
    * <span data-ttu-id="d00cb-2492">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="d00cb-2492">Pre-Post script</span></span>
    * <span data-ttu-id="d00cb-2493">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="d00cb-2493">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2494">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2494">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2495">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="d00cb-2495">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="d00cb-2496">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2496">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-2497">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-2497">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-2498">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-2498">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2499">Az.Network</span></span>
* <span data-ttu-id="d00cb-2500">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2500">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="d00cb-2501">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2501">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2502">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-2503">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2503">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="d00cb-2504">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="d00cb-2504">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2505">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2506">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d00cb-2506">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="d00cb-2507">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="d00cb-2507">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2508">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2508">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2509">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2509">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2510">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2510">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2511">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-2511">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="d00cb-2512">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2512">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d00cb-2513">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2513">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d00cb-2514">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2514">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="d00cb-2515">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="d00cb-2515">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="d00cb-2516">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d00cb-2516">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="d00cb-2517">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2517">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2518">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2519">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="d00cb-2519">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="d00cb-2520">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2520">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2521">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2521">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2522">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="d00cb-2522">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="d00cb-2523">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2523">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-2524">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2524">Az.Automation</span></span>
* <span data-ttu-id="d00cb-2525">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2525">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="d00cb-2526">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2526">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="d00cb-2527">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="d00cb-2527">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00cb-2528">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-2528">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-2529">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2529">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2530">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2531">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="d00cb-2531">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-2532">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-2532">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-2533">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="d00cb-2533">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00cb-2534">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-2534">Az.LogicApp</span></span>
* <span data-ttu-id="d00cb-2535">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2535">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2536">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2536">Az.Network</span></span>
* <span data-ttu-id="d00cb-2537">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2537">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2538">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2538">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-2539">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-2539">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="d00cb-2540">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="d00cb-2540">SDK Update</span></span>
* <span data-ttu-id="d00cb-2541">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d00cb-2541">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="d00cb-2542">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d00cb-2542">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2543">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2543">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2544">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="d00cb-2544">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="d00cb-2545">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="d00cb-2545">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="d00cb-2546">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d00cb-2546">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="d00cb-2547">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="d00cb-2547">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="d00cb-2548">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="d00cb-2548">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="d00cb-2549">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="d00cb-2549">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2550">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2550">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2551">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2551">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="d00cb-2552">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2552">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2553">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2553">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2554">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2554">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="d00cb-2555">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2555">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="d00cb-2556">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2556">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00cb-2557">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2557">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-2558">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2558">Az.Automation</span></span>
* <span data-ttu-id="d00cb-2559">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2559">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="d00cb-2560">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2560">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="d00cb-2561">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2561">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-2562">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2562">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-2563">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2563">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2564">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2565">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="d00cb-2565">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="d00cb-2566">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="d00cb-2566">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="d00cb-2567">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2567">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="d00cb-2568">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2568">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2569">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2569">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-2570">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2570">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="d00cb-2571">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2571">Az.EventHub</span></span>
* <span data-ttu-id="d00cb-2572">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2572">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-2573">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-2573">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-2574">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d00cb-2574">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00cb-2575">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-2575">Az.LogicApp</span></span>
* <span data-ttu-id="d00cb-2576">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="d00cb-2576">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="d00cb-2577">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="d00cb-2577">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="d00cb-2578">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="d00cb-2578">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="d00cb-2579">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00cb-2579">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d00cb-2580">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00cb-2580">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d00cb-2581">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00cb-2581">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="d00cb-2582">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d00cb-2582">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="d00cb-2583">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="d00cb-2583">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="d00cb-2584">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2584">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d00cb-2585">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2585">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d00cb-2586">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2586">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="d00cb-2587">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2587">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="d00cb-2588">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-2588">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="d00cb-2589">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2589">Az.Monitor</span></span>
* <span data-ttu-id="d00cb-2590">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2590">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2591">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2591">Az.Network</span></span>
* <span data-ttu-id="d00cb-2592">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d00cb-2592">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-2593">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2593">Az.OperationalInsights</span></span>
* <span data-ttu-id="d00cb-2594">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2594">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="d00cb-2595">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2595">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="d00cb-2596">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2596">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2597">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2598">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d00cb-2598">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d00cb-2599">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d00cb-2599">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="d00cb-2600">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="d00cb-2600">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="d00cb-2601">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="d00cb-2601">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2602">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2602">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2603">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="d00cb-2603">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="d00cb-2604">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="d00cb-2604">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2605">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2605">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2606">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="d00cb-2606">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="d00cb-2607">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2607">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2608">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2608">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2609">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00cb-2609">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00cb-2610">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2610">Az.AnalysisServices</span></span>
<span data-ttu-id="d00cb-2611">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2611">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2612">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2613">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="d00cb-2613">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="d00cb-2614">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d00cb-2614">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="d00cb-2615">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2615">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2616">Az.RecoveryServices</span></span>
<span data-ttu-id="d00cb-2617">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2617">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2618">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2619">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2619">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="d00cb-2620">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="d00cb-2620">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="d00cb-2621">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="d00cb-2621">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="d00cb-2622">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="d00cb-2622">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2623">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2623">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2624">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2624">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="d00cb-2625">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="d00cb-2625">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="d00cb-2626">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="d00cb-2626">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="d00cb-2627">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2627">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2628">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2628">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2629">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="d00cb-2629">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="d00cb-2630">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2630">Az.AnalysisServices</span></span>
* <span data-ttu-id="d00cb-2631">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-2631">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2632">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2632">Az.RecoveryServices</span></span>
* <span data-ttu-id="d00cb-2633">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-2633">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="d00cb-2634">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2634">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2635">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2635">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2636">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="d00cb-2636">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="d00cb-2637">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2637">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00cb-2638">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="d00cb-2638">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="d00cb-2639">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d00cb-2639">Az.Aks</span></span>
* <span data-ttu-id="d00cb-2640">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2640">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="d00cb-2641">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2641">Az.Automation</span></span>
* <span data-ttu-id="d00cb-2642">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="d00cb-2642">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="d00cb-2643">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2643">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="d00cb-2644">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="d00cb-2644">Az.Cdn</span></span>
* <span data-ttu-id="d00cb-2645">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2645">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2646">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2646">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2647">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2647">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="d00cb-2648">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="d00cb-2648">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="d00cb-2649">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="d00cb-2649">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="d00cb-2650">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d00cb-2650">Az.ContainerRegistry</span></span>
* <span data-ttu-id="d00cb-2651">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2651">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="d00cb-2652">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="d00cb-2652">Az.DataFactory</span></span>
* <span data-ttu-id="d00cb-2653">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="d00cb-2653">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2654">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2654">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-2655">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d00cb-2655">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="d00cb-2656">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="d00cb-2656">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="d00cb-2657">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2657">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-2658">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2658">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-2659">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2659">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="d00cb-2660">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-2660">Az.KeyVault</span></span>
* <span data-ttu-id="d00cb-2661">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2661">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2662">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2662">Az.Network</span></span>
* <span data-ttu-id="d00cb-2663">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2663">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2664">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2664">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2665">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2665">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="d00cb-2666">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2666">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="d00cb-2667">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="d00cb-2667">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="d00cb-2668">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="d00cb-2668">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="d00cb-2669">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="d00cb-2669">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="d00cb-2670">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2670">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="d00cb-2671">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="d00cb-2671">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-2672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2672">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-2673">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="d00cb-2673">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="d00cb-2674">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2674">Fix some error messages.</span></span>
* <span data-ttu-id="d00cb-2675">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2675">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="d00cb-2676">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2676">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d00cb-2677">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d00cb-2677">Az.SignalR</span></span>
* <span data-ttu-id="d00cb-2678">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2678">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2679">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2679">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2680">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2680">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00cb-2681">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d00cb-2681">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="d00cb-2682">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="d00cb-2682">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="d00cb-2683">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2683">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2684">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2684">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2685">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2685">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00cb-2686">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2686">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="d00cb-2687">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="d00cb-2687">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="d00cb-2688">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="d00cb-2688">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="d00cb-2689">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="d00cb-2689">Az.TrafficManager</span></span>
* <span data-ttu-id="d00cb-2690">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2690">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2691">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2691">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2692">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="d00cb-2692">Update incorrect online help URLs</span></span>
* <span data-ttu-id="d00cb-2693">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2693">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="d00cb-2694">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2694">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="d00cb-2695">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="d00cb-2695">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="d00cb-2696">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2696">Az.Accounts</span></span>
* <span data-ttu-id="d00cb-2697">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="d00cb-2697">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2698">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2699">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2699">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="d00cb-2700">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="d00cb-2700">Updated the description of ID in help files</span></span>
* <span data-ttu-id="d00cb-2701">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2701">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2702">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-2703">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2703">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="d00cb-2704">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="d00cb-2704">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="d00cb-2705">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="d00cb-2705">Az.EventGrid</span></span>
* <span data-ttu-id="d00cb-2706">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2706">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="d00cb-2707">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="d00cb-2707">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="d00cb-2708">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2708">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d00cb-2709">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d00cb-2709">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d00cb-2710">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2710">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d00cb-2711">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2711">Dead letter endpoint.</span></span>
    - <span data-ttu-id="d00cb-2712">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2712">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="d00cb-2713">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="d00cb-2713">Event Time-To-Live,</span></span>
        - <span data-ttu-id="d00cb-2714">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2714">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="d00cb-2715">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="d00cb-2715">Dead letter endpoint.</span></span>
* <span data-ttu-id="d00cb-2716">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2716">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="d00cb-2717">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2717">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="d00cb-2718">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2718">Az.IotHub</span></span>
* <span data-ttu-id="d00cb-2719">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="d00cb-2719">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="d00cb-2720">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="d00cb-2720">Az.LogicApp</span></span>
* <span data-ttu-id="d00cb-2721">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="d00cb-2721">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2722">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2723">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2723">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="d00cb-2724">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="d00cb-2724">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="d00cb-2725">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d00cb-2725">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d00cb-2726">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d00cb-2726">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="d00cb-2727">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2727">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="d00cb-2728">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="d00cb-2728">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="d00cb-2729">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="d00cb-2729">Az.SignalR</span></span>
* <span data-ttu-id="d00cb-2730">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2730">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-2731">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2731">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2732">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2732">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="d00cb-2733">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2733">Az.Storage</span></span>
* <span data-ttu-id="d00cb-2734">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="d00cb-2734">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="d00cb-2735">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d00cb-2735">New-AzStorageContext</span></span>
* <span data-ttu-id="d00cb-2736">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2736">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="d00cb-2737">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d00cb-2737">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-2738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2738">Az.Websites</span></span>
* <span data-ttu-id="d00cb-2739">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="d00cb-2739">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="d00cb-2740">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2740">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="d00cb-2741">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d00cb-2741">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="d00cb-2742">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-2742">General</span></span>

- <span data-ttu-id="d00cb-2743">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="d00cb-2743">General Availability of Az Module</span></span>
- <span data-ttu-id="d00cb-2744">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2744">Online help for each module</span></span>
- <span data-ttu-id="d00cb-2745">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="d00cb-2745">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="d00cb-2746">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="d00cb-2746">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="d00cb-2747">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2747">Az.Accounts</span></span>
- <span data-ttu-id="d00cb-2748">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2748">Changed from Az.Profile</span></span>
- <span data-ttu-id="d00cb-2749">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="d00cb-2749">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d00cb-2750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-2750">Az.ApiManagement</span></span>
- <span data-ttu-id="d00cb-2751">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="d00cb-2751">Fixes for #7002</span></span>
- <span data-ttu-id="d00cb-2752">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2752">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="d00cb-2753">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="d00cb-2753">Az.Batch</span></span>
- <span data-ttu-id="d00cb-2754">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2754">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="d00cb-2755">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2755">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="d00cb-2756">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2756">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="d00cb-2757">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="d00cb-2757">Az.Billing</span></span>
- <span data-ttu-id="d00cb-2758">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2758">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="d00cb-2759">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2759">Az.CognitivServices</span></span>
- <span data-ttu-id="d00cb-2760">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2760">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="d00cb-2761">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="d00cb-2761">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d00cb-2762">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-2762">Az.ContainerInstance</span></span>
- <span data-ttu-id="d00cb-2763">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="d00cb-2763">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="d00cb-2764">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="d00cb-2764">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="d00cb-2765">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2766">Az.DataLakeStore</span></span>
- <span data-ttu-id="d00cb-2767">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="d00cb-2768">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2768">Az.Monitor</span></span>
- <span data-ttu-id="d00cb-2769">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2769">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="d00cb-2770">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d00cb-2770">Az.KeyVault</span></span>
- <span data-ttu-id="d00cb-2771">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="d00cb-2771">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="d00cb-2772">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="d00cb-2772">Az.MachineLearning</span></span>
- <span data-ttu-id="d00cb-2773">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2773">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="d00cb-2774">Az.Media</span><span class="sxs-lookup"><span data-stu-id="d00cb-2774">Az.Media</span></span>
- <span data-ttu-id="d00cb-2775">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d00cb-2775">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d00cb-2776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2776">Az.Network</span></span>
<span data-ttu-id="d00cb-2777">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2777">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="d00cb-2778">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="d00cb-2778">New cmdlets added:</span></span>
        - <span data-ttu-id="d00cb-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2779">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00cb-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2780">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00cb-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2781">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00cb-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2782">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00cb-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2783">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="d00cb-2784">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2784">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="d00cb-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2785">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="d00cb-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d00cb-2786">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="d00cb-2787">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2787">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="d00cb-2788">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d00cb-2788">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="d00cb-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2789">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d00cb-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d00cb-2790">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="d00cb-2791">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2791">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="d00cb-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2792">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="d00cb-2793">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2793">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="d00cb-2794">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d00cb-2794">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="d00cb-2795">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d00cb-2795">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d00cb-2796">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d00cb-2796">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="d00cb-2797">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d00cb-2797">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="d00cb-2798">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d00cb-2798">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="d00cb-2799">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2799">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="d00cb-2800">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2800">Az.OperationalInsights</span></span>
- <span data-ttu-id="d00cb-2801">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2801">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="d00cb-2802">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2802">Az.Profile</span></span>
- <span data-ttu-id="d00cb-2803">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="d00cb-2803">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2804">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2804">Az.RecoveryServices</span></span>
- <span data-ttu-id="d00cb-2805">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2805">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="d00cb-2806">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2806">Az.Resources</span></span>
- <span data-ttu-id="d00cb-2807">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2807">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d00cb-2808">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2808">Az.ServiceFabric</span></span>
- <span data-ttu-id="d00cb-2809">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="d00cb-2809">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="d00cb-2810">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2810">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="d00cb-2811">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d00cb-2811">Az.SIgnalR</span></span>
- <span data-ttu-id="d00cb-2812">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="d00cb-2812">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="d00cb-2813">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2813">Az.Sql</span></span>
- <span data-ttu-id="d00cb-2814">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="d00cb-2814">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="d00cb-2815">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="d00cb-2815">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="d00cb-2816">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="d00cb-2817">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2817">Az.Storage</span></span>
- <span data-ttu-id="d00cb-2818">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2818">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d00cb-2819">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2819">Az.Websites</span></span>
- <span data-ttu-id="d00cb-2820">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="d00cb-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="d00cb-2821">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d00cb-2821">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="d00cb-2822">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-2822">General</span></span>

* <span data-ttu-id="d00cb-2823">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d00cb-2823">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="d00cb-2824">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2824">Az.Compute</span></span>

* <span data-ttu-id="d00cb-2825">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2825">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2826">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2826">Az.DataLakeStore</span></span>

* <span data-ttu-id="d00cb-2827">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="d00cb-2827">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="d00cb-2828">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d00cb-2828">Az.FrontDoor</span></span>

* <span data-ttu-id="d00cb-2829">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="d00cb-2829">Fixed some broken links</span></span>
    - <span data-ttu-id="d00cb-2830">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2830">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="d00cb-2831">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2831">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="d00cb-2832">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2832">Az.RecoveryServices</span></span>

* <span data-ttu-id="d00cb-2833">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2833">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="d00cb-2834">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2834">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="d00cb-2835">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2835">Az.Resources</span></span>

* <span data-ttu-id="d00cb-2836">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="d00cb-2836">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="d00cb-2837">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2837">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="d00cb-2838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2838">Az.Sql</span></span>

* <span data-ttu-id="d00cb-2839">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="d00cb-2839">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="d00cb-2840">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="d00cb-2840">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="d00cb-2841">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2841">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="d00cb-2842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2842">Az.Storage</span></span>

* <span data-ttu-id="d00cb-2843">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2843">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="d00cb-2844">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="d00cb-2844">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="d00cb-2845">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2845">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d00cb-2846">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="d00cb-2846">Support Static Website configuration</span></span>
    - <span data-ttu-id="d00cb-2847">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d00cb-2847">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="d00cb-2848">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="d00cb-2848">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="d00cb-2849">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-2849">Az.Websites</span></span>

* <span data-ttu-id="d00cb-2850">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="d00cb-2850">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="d00cb-2851">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2851">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="d00cb-2852">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2852">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="d00cb-2853">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d00cb-2853">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="d00cb-2854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="d00cb-2854">Az.ApiManagement</span></span>
* <span data-ttu-id="d00cb-2855">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2855">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="d00cb-2856">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="d00cb-2856">Az.Automation</span></span>
* <span data-ttu-id="d00cb-2857">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="d00cb-2857">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="d00cb-2858">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2858">Added Update Management cmdlets</span></span>
* <span data-ttu-id="d00cb-2859">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2859">Added Source Control cmdlets</span></span>
* <span data-ttu-id="d00cb-2860">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="d00cb-2860">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="d00cb-2861">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="d00cb-2861">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="d00cb-2862">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2862">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2863">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="d00cb-2863">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="d00cb-2864">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2864">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="d00cb-2865">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-2865">Az.ContainerInstance</span></span>
* <span data-ttu-id="d00cb-2866">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2866">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="d00cb-2867">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d00cb-2867">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="d00cb-2868">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="d00cb-2868">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="d00cb-2869">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2869">Az.Network</span></span>
* <span data-ttu-id="d00cb-2870">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2870">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="d00cb-2871">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="d00cb-2871">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="d00cb-2872">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2872">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="d00cb-2873">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d00cb-2873">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="d00cb-2874">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="d00cb-2874">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="d00cb-2875">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2875">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="d00cb-2876">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2876">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="d00cb-2877">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d00cb-2877">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="d00cb-2878">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d00cb-2878">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="d00cb-2879">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="d00cb-2879">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="d00cb-2880">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="d00cb-2880">Az.Relay</span></span>
* <span data-ttu-id="d00cb-2881">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2881">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="d00cb-2882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2882">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2883">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="d00cb-2883">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="d00cb-2884">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="d00cb-2884">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="d00cb-2885">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="d00cb-2885">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="d00cb-2886">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2886">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-2887">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="d00cb-2887">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="d00cb-2888">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-2888">Az.Sql</span></span>
* <span data-ttu-id="d00cb-2889">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="d00cb-2889">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="d00cb-2890">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-2890">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00cb-2891">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-2891">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00cb-2892">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-2892">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00cb-2893">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d00cb-2893">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="d00cb-2894">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00cb-2894">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d00cb-2895">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00cb-2895">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d00cb-2896">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00cb-2896">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="d00cb-2897">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d00cb-2897">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="d00cb-2898">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2898">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="d00cb-2899">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2899">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="d00cb-2900">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2900">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="d00cb-2901">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2901">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d00cb-2902">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2902">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="d00cb-2903">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2903">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="d00cb-2904">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2904">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="d00cb-2905">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d00cb-2905">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="d00cb-2906">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d00cb-2906">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="d00cb-2907">Geral</span><span class="sxs-lookup"><span data-stu-id="d00cb-2907">General</span></span>
* <span data-ttu-id="d00cb-2908">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="d00cb-2908">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="d00cb-2909">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2909">Az.Profile</span></span>
* <span data-ttu-id="d00cb-2910">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00cb-2910">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="d00cb-2911">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="d00cb-2911">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="d00cb-2912">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="d00cb-2912">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="d00cb-2913">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="d00cb-2913">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="d00cb-2914">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="d00cb-2914">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="d00cb-2915">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="d00cb-2915">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="d00cb-2916">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="d00cb-2916">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-2917">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2917">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-2918">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2918">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2919">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2920">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d00cb-2920">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="d00cb-2921">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="d00cb-2921">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="d00cb-2922">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2922">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-2924">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2924">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="d00cb-2925">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2925">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="d00cb-2926">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2926">Az.Insights</span></span>
* <span data-ttu-id="d00cb-2927">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="d00cb-2927">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="d00cb-2928">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="d00cb-2928">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="d00cb-2929">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="d00cb-2929">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="d00cb-2930">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="d00cb-2930">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2931">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2931">Az.Network</span></span>
* <span data-ttu-id="d00cb-2932">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="d00cb-2932">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="d00cb-2933">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-2933">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="d00cb-2934">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-2934">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="d00cb-2935">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d00cb-2935">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="d00cb-2936">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-2936">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="d00cb-2937">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="d00cb-2937">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="d00cb-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="d00cb-2938">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="d00cb-2939">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="d00cb-2939">Az.PolicyInsights</span></span>
* <span data-ttu-id="d00cb-2940">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="d00cb-2940">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2941">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2942">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="d00cb-2942">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="d00cb-2943">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="d00cb-2943">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="d00cb-2944">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="d00cb-2944">Az.ServiceBus</span></span>
* <span data-ttu-id="d00cb-2945">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2945">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="d00cb-2946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d00cb-2946">Az.ServiceFabric</span></span>
* <span data-ttu-id="d00cb-2947">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2947">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="d00cb-2948">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="d00cb-2948">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="d00cb-2949">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="d00cb-2949">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="d00cb-2950">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="d00cb-2950">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="d00cb-2951">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2951">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="d00cb-2952">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d00cb-2952">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="d00cb-2953">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2953">Az.Profile</span></span>
* <span data-ttu-id="d00cb-2954">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="d00cb-2954">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="d00cb-2955">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="d00cb-2955">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2956">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2956">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2957">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="d00cb-2957">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="d00cb-2958">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2958">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="d00cb-2959">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="d00cb-2959">Az.DataLakeStore</span></span>
* <span data-ttu-id="d00cb-2960">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="d00cb-2960">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="d00cb-2961">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2961">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="d00cb-2962">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2962">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d00cb-2963">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2963">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="d00cb-2964">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2964">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2965">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2965">Az.Network</span></span>
* <span data-ttu-id="d00cb-2966">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2966">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="d00cb-2967">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2967">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-2968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-2968">Az.Resources</span></span>
* <span data-ttu-id="d00cb-2969">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2969">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="d00cb-2970">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2970">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="d00cb-2971">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="d00cb-2971">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="d00cb-2972">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2972">Azure.Storage</span></span>
* <span data-ttu-id="d00cb-2973">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2973">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="d00cb-2974">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2974">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="d00cb-2975">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d00cb-2975">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="d00cb-2976">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2976">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="d00cb-2977">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="d00cb-2977">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="d00cb-2978">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="d00cb-2978">Az.CognitiveServices</span></span>
* <span data-ttu-id="d00cb-2979">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2979">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="d00cb-2980">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="d00cb-2980">Az.Compute</span></span>
* <span data-ttu-id="d00cb-2981">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="d00cb-2981">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="d00cb-2982">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2982">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="d00cb-2983">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="d00cb-2983">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="d00cb-2984">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="d00cb-2984">Az.DataFactoryV2</span></span>
* <span data-ttu-id="d00cb-2985">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2985">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="d00cb-2986">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d00cb-2986">Az.Network</span></span>
* <span data-ttu-id="d00cb-2987">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2987">Added NetworkProfile functionality.</span></span> <span data-ttu-id="d00cb-2988">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="d00cb-2988">new cmdlets added</span></span>
    - <span data-ttu-id="d00cb-2989">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2989">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00cb-2990">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2990">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00cb-2991">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2991">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00cb-2992">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d00cb-2992">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="d00cb-2993">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2993">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="d00cb-2994">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2994">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="d00cb-2995">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="d00cb-2995">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="d00cb-2996">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d00cb-2996">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="d00cb-2997">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d00cb-2997">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="d00cb-2998">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="d00cb-2998">Az.RedisCache</span></span>
* <span data-ttu-id="d00cb-2999">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="d00cb-2999">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="d00cb-3000">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="d00cb-3000">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="d00cb-3001">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="d00cb-3001">Az.Resources</span></span>
* <span data-ttu-id="d00cb-3002">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d00cb-3002">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="d00cb-3003">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="d00cb-3003">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="d00cb-3004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d00cb-3004">Az.Sql</span></span>
* <span data-ttu-id="d00cb-3005">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="d00cb-3005">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="d00cb-3006">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="d00cb-3006">Az.Websites</span></span>
* <span data-ttu-id="d00cb-3007">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="d00cb-3007">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="d00cb-3008">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="d00cb-3008">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="d00cb-3009">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="d00cb-3009">0.2.0 - September 2018</span></span>
 <span data-ttu-id="d00cb-3010">Versão inicial</span><span class="sxs-lookup"><span data-stu-id="d00cb-3010">Initial Release</span></span>
