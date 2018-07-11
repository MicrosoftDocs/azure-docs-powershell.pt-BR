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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406123"
---
# <a name="release-notes"></a><span data-ttu-id="cd686-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="cd686-103">Release notes</span></span>

<span data-ttu-id="cd686-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cd686-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="cd686-105">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="cd686-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cd686-106">Geral</span><span class="sxs-lookup"><span data-stu-id="cd686-106">General</span></span>
* <span data-ttu-id="cd686-107">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="cd686-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="cd686-108">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="cd686-108">AzureRM.Profile</span></span>
* <span data-ttu-id="cd686-109">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="cd686-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cd686-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cd686-110">AzureRM.Compute</span></span>
* <span data-ttu-id="cd686-111">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="cd686-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="cd686-112">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="cd686-113">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="cd686-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="cd686-114">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="cd686-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="cd686-115">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd686-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="cd686-116">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="cd686-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="cd686-117">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd686-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="cd686-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cd686-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="cd686-119">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="cd686-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="cd686-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cd686-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="cd686-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cd686-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="cd686-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cd686-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="cd686-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd686-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="cd686-124">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="cd686-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="cd686-125">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="cd686-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="cd686-126">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="cd686-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="cd686-127">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="cd686-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="cd686-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="cd686-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="cd686-129">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="cd686-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="cd686-130">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="cd686-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="cd686-131">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="cd686-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="cd686-132">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="cd686-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="cd686-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd686-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cd686-134">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="cd686-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="cd686-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cd686-135">AzureRM.Network</span></span>
* <span data-ttu-id="cd686-136">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="cd686-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="cd686-137">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="cd686-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="cd686-138">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="cd686-139">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="cd686-140">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="cd686-141">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="cd686-142">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="cd686-143">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cd686-144">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cd686-145">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="cd686-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="cd686-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cd686-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cd686-147">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="cd686-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="cd686-148">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="cd686-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="cd686-149">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="cd686-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cd686-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cd686-150">AzureRM.Resources</span></span>
* <span data-ttu-id="cd686-151">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="cd686-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="cd686-152">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="cd686-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="cd686-153">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="cd686-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="cd686-154">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd686-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="cd686-155">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cd686-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="cd686-156">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="cd686-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="cd686-157">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="cd686-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="cd686-158">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="cd686-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="cd686-159">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="cd686-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="cd686-160">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="cd686-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="cd686-161">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="cd686-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="cd686-162">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="cd686-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="cd686-163">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="cd686-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="cd686-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cd686-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="cd686-165">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="cd686-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cd686-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cd686-166">AzureRM.Sql</span></span>
* <span data-ttu-id="cd686-167">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="cd686-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="cd686-168">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="cd686-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="cd686-169">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="cd686-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cd686-170">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="cd686-170">AzureRM.Profile</span></span>
* <span data-ttu-id="cd686-171">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="cd686-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="cd686-172">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="cd686-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="cd686-173">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="cd686-173">Azure.Storage</span></span>
* <span data-ttu-id="cd686-174">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="cd686-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cd686-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cd686-175">AzureRM.Compute</span></span>
* <span data-ttu-id="cd686-176">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="cd686-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="cd686-177">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="cd686-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="cd686-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="cd686-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="cd686-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="cd686-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="cd686-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="cd686-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="cd686-181">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="cd686-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="cd686-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd686-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="cd686-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd686-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="cd686-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd686-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="cd686-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd686-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="cd686-186">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cd686-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="cd686-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd686-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="cd686-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="cd686-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="cd686-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="cd686-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="cd686-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd686-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="cd686-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd686-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="cd686-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd686-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="cd686-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="cd686-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="cd686-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="cd686-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="cd686-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="cd686-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="cd686-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="cd686-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="cd686-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="cd686-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="cd686-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="cd686-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="cd686-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="cd686-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="cd686-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="cd686-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="cd686-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cd686-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="cd686-202">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="cd686-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="cd686-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd686-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cd686-204">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="cd686-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="cd686-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cd686-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="cd686-206">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="cd686-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="cd686-207">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="cd686-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="cd686-208">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="cd686-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="cd686-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cd686-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cd686-210">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="cd686-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="cd686-211">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="cd686-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cd686-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cd686-212">AzureRM.Sql</span></span>
* <span data-ttu-id="cd686-213">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="cd686-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="cd686-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cd686-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="cd686-215">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="cd686-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cd686-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cd686-216">AzureRM.Websites</span></span>
* <span data-ttu-id="cd686-217">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cd686-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="cd686-218">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="cd686-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="cd686-219">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="cd686-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="cd686-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cd686-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="cd686-221">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd686-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="cd686-222">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="cd686-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cd686-223">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="cd686-223">AzureRM.Profile</span></span>
* <span data-ttu-id="cd686-224">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="cd686-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="cd686-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="cd686-225">AzureRM.Compute</span></span>
* <span data-ttu-id="cd686-226">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="cd686-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="cd686-227">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="cd686-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="cd686-228">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="cd686-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="cd686-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cd686-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="cd686-230">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="cd686-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="cd686-231">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="cd686-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="cd686-232">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="cd686-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="cd686-233">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="cd686-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="cd686-234">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="cd686-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="cd686-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cd686-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="cd686-236">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="cd686-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="cd686-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cd686-237">AzureRM.Network</span></span>
* <span data-ttu-id="cd686-238">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="cd686-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="cd686-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="cd686-239">AzureRM.Resources</span></span>
* <span data-ttu-id="cd686-240">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="cd686-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="cd686-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="cd686-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="cd686-242">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="cd686-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="cd686-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cd686-243">AzureRM.Sql</span></span>
* <span data-ttu-id="cd686-244">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="cd686-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="cd686-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd686-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="cd686-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cd686-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="cd686-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cd686-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="cd686-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cd686-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="cd686-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd686-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="cd686-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="cd686-250">AzureRM.Websites</span></span>
* <span data-ttu-id="cd686-251">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="cd686-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="cd686-252">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="cd686-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="cd686-253">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="cd686-253">AzureRM.Profile</span></span>
* <span data-ttu-id="cd686-254">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="cd686-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="cd686-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cd686-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="cd686-256">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="cd686-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="cd686-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cd686-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="cd686-258">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="cd686-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="cd686-259">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd686-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="cd686-260">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="cd686-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="cd686-261">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="cd686-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="cd686-262">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="cd686-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="cd686-263">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="cd686-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="cd686-264">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="cd686-264">Added support for MSI identity</span></span>
* <span data-ttu-id="cd686-265">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="cd686-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="cd686-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="cd686-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="cd686-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd686-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="cd686-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="cd686-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="cd686-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="cd686-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="cd686-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="cd686-270">AzureRM.Batch</span></span>
* <span data-ttu-id="cd686-271">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="cd686-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="cd686-272">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="cd686-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="cd686-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="cd686-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="cd686-274">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="cd686-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="cd686-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cd686-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="cd686-276">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="cd686-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="cd686-277">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cd686-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="cd686-278">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="cd686-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="cd686-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="cd686-279">AzureRM.Network</span></span>
* <span data-ttu-id="cd686-280">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="cd686-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="cd686-281">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="cd686-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="cd686-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd686-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="cd686-283">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="cd686-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="cd686-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cd686-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="cd686-285">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="cd686-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="cd686-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cd686-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="cd686-287">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="cd686-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="cd686-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="cd686-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="cd686-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cd686-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="cd686-290">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="cd686-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="cd686-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="cd686-291">AzureRM.Sql</span></span>
* <span data-ttu-id="cd686-292">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="cd686-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="cd686-293">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="cd686-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="cd686-294">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="cd686-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="cd686-295">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="cd686-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="cd686-296">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="cd686-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="cd686-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd686-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="cd686-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="cd686-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="cd686-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cd686-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="cd686-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cd686-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="cd686-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cd686-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="cd686-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cd686-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="cd686-303">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="cd686-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>