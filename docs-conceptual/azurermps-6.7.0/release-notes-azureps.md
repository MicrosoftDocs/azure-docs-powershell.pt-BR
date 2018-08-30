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
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018512"
---
# <a name="release-notes"></a><span data-ttu-id="92745-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="92745-103">Release notes</span></span>

<span data-ttu-id="92745-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="92745-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="92745-105">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="92745-106">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="92745-106">AzureRM.Profile</span></span>
* <span data-ttu-id="92745-107">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="92745-108">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="92745-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="92745-109">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="92745-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="92745-110">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="92745-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="92745-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="92745-111">Azure.Storage</span></span>
* <span data-ttu-id="92745-112">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="92745-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="92745-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="92745-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="92745-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92745-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="92745-115">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="92745-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92745-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="92745-117">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="92745-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="92745-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="92745-119">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="92745-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="92745-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="92745-121">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="92745-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="92745-122">AzureRM.Automation</span></span>
* <span data-ttu-id="92745-123">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="92745-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="92745-124">AzureRM.Backup</span></span>
* <span data-ttu-id="92745-125">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="92745-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="92745-126">AzureRM.Batch</span></span>
* <span data-ttu-id="92745-127">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="92745-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="92745-128">AzureRM.Billing</span></span>
* <span data-ttu-id="92745-129">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="92745-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="92745-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="92745-131">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="92745-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="92745-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="92745-133">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="92745-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="92745-134">AzureRM.Compute</span></span>
* <span data-ttu-id="92745-135">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="92745-136">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="92745-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="92745-137">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="92745-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="92745-138">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="92745-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="92745-139">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="92745-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="92745-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="92745-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="92745-141">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="92745-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="92745-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="92745-143">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="92745-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="92745-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="92745-145">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="92745-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="92745-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="92745-147">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="92745-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="92745-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="92745-149">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="92745-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="92745-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="92745-151">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="92745-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92745-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="92745-153">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="92745-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="92745-154">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="92745-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="92745-155">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="92745-156">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="92745-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="92745-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="92745-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="92745-158">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="92745-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="92745-159">AzureRM.Dns</span></span>
* <span data-ttu-id="92745-160">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="92745-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="92745-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="92745-162">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="92745-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="92745-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="92745-164">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="92745-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="92745-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="92745-166">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="92745-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="92745-167">AzureRM.Insights</span></span>
* <span data-ttu-id="92745-168">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="92745-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="92745-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="92745-170">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="92745-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92745-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="92745-172">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="92745-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="92745-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="92745-174">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="92745-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="92745-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="92745-176">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="92745-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="92745-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="92745-178">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="92745-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="92745-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="92745-180">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="92745-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="92745-181">AzureRM.Media</span></span>
* <span data-ttu-id="92745-182">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="92745-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="92745-183">AzureRM.Network</span></span>
* <span data-ttu-id="92745-184">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92745-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="92745-185">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="92745-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="92745-186">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="92745-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="92745-187">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="92745-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="92745-188">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="92745-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="92745-189">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="92745-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="92745-190">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="92745-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="92745-191">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="92745-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="92745-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="92745-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="92745-193">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="92745-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="92745-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="92745-195">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="92745-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="92745-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="92745-197">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="92745-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="92745-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="92745-199">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="92745-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="92745-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="92745-201">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="92745-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="92745-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="92745-203">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="92745-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="92745-204">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="92745-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="92745-205">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="92745-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="92745-206">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="92745-207">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="92745-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="92745-208">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="92745-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="92745-209">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="92745-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="92745-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="92745-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="92745-211">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="92745-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="92745-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="92745-213">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="92745-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="92745-214">AzureRM.Relay</span></span>
* <span data-ttu-id="92745-215">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="92745-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="92745-216">AzureRM.Resources</span></span>
* <span data-ttu-id="92745-217">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="92745-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="92745-218">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="92745-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="92745-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="92745-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="92745-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="92745-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="92745-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="92745-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="92745-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="92745-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="92745-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="92745-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="92745-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="92745-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="92745-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="92745-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="92745-226">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="92745-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="92745-227">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92745-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="92745-228">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="92745-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="92745-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="92745-230">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="92745-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="92745-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="92745-232">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="92745-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92745-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="92745-234">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="92745-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="92745-235">AzureRM.Sql</span></span>
* <span data-ttu-id="92745-236">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="92745-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="92745-237">AzureRM.Storage</span></span>
* <span data-ttu-id="92745-238">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="92745-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="92745-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="92745-240">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="92745-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="92745-241">AzureRM.Tags</span></span>
* <span data-ttu-id="92745-242">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="92745-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="92745-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="92745-244">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="92745-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="92745-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="92745-246">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="92745-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="92745-247">AzureRM.Websites</span></span>
* <span data-ttu-id="92745-248">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="92745-249">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="92745-250">Geral</span><span class="sxs-lookup"><span data-stu-id="92745-250">General</span></span>
* <span data-ttu-id="92745-251">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="92745-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="92745-252">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="92745-252">AzureRM.Profile</span></span>
* <span data-ttu-id="92745-253">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="92745-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="92745-254">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="92745-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="92745-255">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="92745-255">Azure.Storage</span></span>
* <span data-ttu-id="92745-256">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92745-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="92745-257">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="92745-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="92745-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="92745-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="92745-259">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="92745-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="92745-260">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="92745-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="92745-261">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="92745-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="92745-262">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="92745-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="92745-263">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="92745-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="92745-264">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="92745-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="92745-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="92745-265">AzureRM.Compute</span></span>
* <span data-ttu-id="92745-266">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="92745-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="92745-267">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="92745-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="92745-268">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="92745-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="92745-269">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="92745-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="92745-270">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="92745-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="92745-271">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="92745-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="92745-272">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="92745-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="92745-273">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="92745-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="92745-274">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="92745-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="92745-275">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="92745-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="92745-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="92745-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="92745-277">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="92745-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="92745-278">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="92745-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="92745-279">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="92745-280">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="92745-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="92745-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92745-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="92745-282">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="92745-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="92745-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="92745-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="92745-284">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="92745-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="92745-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="92745-285">AzureRM.Insights</span></span>
* <span data-ttu-id="92745-286">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="92745-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="92745-287">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="92745-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="92745-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92745-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="92745-289">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92745-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="92745-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="92745-290">AzureRM.Network</span></span>
* <span data-ttu-id="92745-291">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="92745-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="92745-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="92745-292">AzureRM.Resources</span></span>
* <span data-ttu-id="92745-293">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="92745-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="92745-294">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="92745-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="92745-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="92745-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="92745-296">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="92745-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="92745-297">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="92745-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="92745-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="92745-298">AzureRM.Sql</span></span>
* <span data-ttu-id="92745-299">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="92745-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="92745-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="92745-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="92745-301">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="92745-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="92745-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="92745-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="92745-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="92745-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="92745-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="92745-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="92745-305">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="92745-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="92745-306">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="92745-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="92745-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="92745-307">AzureRM.Storage</span></span>
* <span data-ttu-id="92745-308">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="92745-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="92745-309">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="92745-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="92745-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92745-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="92745-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92745-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="92745-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="92745-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="92745-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="92745-313">AzureRM.Tags</span></span>
* <span data-ttu-id="92745-314">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="92745-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="92745-315">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="92745-316">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="92745-316">AzureRM.Profile</span></span>
* <span data-ttu-id="92745-317">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="92745-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="92745-318">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="92745-318">Azure.Storage</span></span>
* <span data-ttu-id="92745-319">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="92745-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="92745-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="92745-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="92745-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="92745-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="92745-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92745-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="92745-323">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="92745-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="92745-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="92745-324">AzureRM.Automation</span></span>
* <span data-ttu-id="92745-325">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="92745-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="92745-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="92745-326">AzureRM.Compute</span></span>
* <span data-ttu-id="92745-327">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92745-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="92745-328">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="92745-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="92745-329">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="92745-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="92745-330">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="92745-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="92745-331">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="92745-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="92745-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="92745-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="92745-333">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="92745-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="92745-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92745-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="92745-335">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="92745-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="92745-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="92745-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="92745-337">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="92745-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="92745-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="92745-338">AzureRM.Network</span></span>
* <span data-ttu-id="92745-339">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="92745-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="92745-340">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="92745-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="92745-341">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="92745-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="92745-342">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="92745-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="92745-343">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="92745-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="92745-344">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="92745-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="92745-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="92745-345">AzureRM.Relay</span></span>
* <span data-ttu-id="92745-346">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="92745-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="92745-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="92745-347">AzureRM.Resources</span></span>
* <span data-ttu-id="92745-348">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="92745-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="92745-349">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="92745-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="92745-350">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="92745-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="92745-351">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="92745-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="92745-352">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="92745-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="92745-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="92745-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="92745-354">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="92745-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="92745-355">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="92745-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="92745-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="92745-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="92745-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="92745-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="92745-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="92745-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="92745-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="92745-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="92745-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="92745-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="92745-361">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="92745-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="92745-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92745-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="92745-363">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="92745-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="92745-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="92745-364">AzureRM.Sql</span></span>
* <span data-ttu-id="92745-365">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="92745-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="92745-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="92745-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="92745-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="92745-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="92745-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="92745-368">AzureRM.Websites</span></span>
* <span data-ttu-id="92745-369">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="92745-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="92745-370">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="92745-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="92745-371">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="92745-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="92745-372">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="92745-373">Geral</span><span class="sxs-lookup"><span data-stu-id="92745-373">General</span></span>
* <span data-ttu-id="92745-374">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="92745-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="92745-375">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="92745-375">AzureRM.Profile</span></span>
* <span data-ttu-id="92745-376">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="92745-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="92745-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="92745-377">AzureRM.Compute</span></span>
* <span data-ttu-id="92745-378">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="92745-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="92745-379">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="92745-380">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="92745-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="92745-381">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="92745-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="92745-382">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92745-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="92745-383">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="92745-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="92745-384">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92745-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="92745-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="92745-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="92745-386">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="92745-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="92745-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="92745-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="92745-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="92745-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="92745-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="92745-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="92745-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92745-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="92745-391">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="92745-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="92745-392">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="92745-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="92745-393">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="92745-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="92745-394">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="92745-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="92745-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="92745-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="92745-396">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="92745-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="92745-397">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="92745-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="92745-398">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="92745-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="92745-399">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="92745-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="92745-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92745-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="92745-401">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="92745-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="92745-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="92745-402">AzureRM.Network</span></span>
* <span data-ttu-id="92745-403">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="92745-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="92745-404">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="92745-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="92745-405">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="92745-406">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="92745-407">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="92745-408">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="92745-409">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="92745-410">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="92745-411">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="92745-412">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="92745-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="92745-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="92745-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="92745-414">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="92745-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="92745-415">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="92745-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="92745-416">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="92745-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="92745-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="92745-417">AzureRM.Resources</span></span>
* <span data-ttu-id="92745-418">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="92745-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="92745-419">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="92745-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="92745-420">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="92745-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="92745-421">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="92745-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="92745-422">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="92745-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="92745-423">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="92745-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="92745-424">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="92745-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="92745-425">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="92745-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="92745-426">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="92745-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="92745-427">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="92745-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="92745-428">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="92745-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="92745-429">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="92745-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="92745-430">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="92745-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="92745-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="92745-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="92745-432">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="92745-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="92745-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="92745-433">AzureRM.Sql</span></span>
* <span data-ttu-id="92745-434">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="92745-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="92745-435">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="92745-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="92745-436">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="92745-437">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="92745-437">AzureRM.Profile</span></span>
* <span data-ttu-id="92745-438">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="92745-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="92745-439">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="92745-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="92745-440">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="92745-440">Azure.Storage</span></span>
* <span data-ttu-id="92745-441">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="92745-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="92745-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="92745-442">AzureRM.Compute</span></span>
* <span data-ttu-id="92745-443">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="92745-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="92745-444">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="92745-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="92745-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="92745-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="92745-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="92745-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="92745-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="92745-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="92745-448">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="92745-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="92745-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92745-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="92745-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92745-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="92745-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92745-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="92745-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92745-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="92745-453">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="92745-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="92745-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92745-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="92745-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="92745-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="92745-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="92745-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="92745-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92745-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="92745-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92745-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="92745-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92745-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="92745-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="92745-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="92745-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="92745-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="92745-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="92745-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="92745-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="92745-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="92745-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="92745-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="92745-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="92745-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="92745-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="92745-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="92745-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="92745-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="92745-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="92745-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="92745-469">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="92745-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="92745-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92745-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="92745-471">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="92745-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="92745-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="92745-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="92745-473">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="92745-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="92745-474">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="92745-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="92745-475">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="92745-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="92745-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="92745-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="92745-477">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="92745-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="92745-478">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="92745-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="92745-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="92745-479">AzureRM.Sql</span></span>
* <span data-ttu-id="92745-480">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="92745-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="92745-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="92745-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="92745-482">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="92745-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="92745-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="92745-483">AzureRM.Websites</span></span>
* <span data-ttu-id="92745-484">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="92745-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="92745-485">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="92745-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="92745-486">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="92745-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="92745-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="92745-488">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="92745-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="92745-489">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="92745-490">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="92745-490">AzureRM.Profile</span></span>
* <span data-ttu-id="92745-491">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="92745-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="92745-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="92745-492">AzureRM.Compute</span></span>
* <span data-ttu-id="92745-493">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="92745-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="92745-494">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="92745-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="92745-495">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="92745-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="92745-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="92745-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="92745-497">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="92745-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="92745-498">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="92745-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="92745-499">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="92745-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="92745-500">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="92745-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="92745-501">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="92745-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="92745-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="92745-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="92745-503">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="92745-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="92745-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="92745-504">AzureRM.Network</span></span>
* <span data-ttu-id="92745-505">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="92745-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="92745-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="92745-506">AzureRM.Resources</span></span>
* <span data-ttu-id="92745-507">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="92745-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="92745-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="92745-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="92745-509">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="92745-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="92745-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="92745-510">AzureRM.Sql</span></span>
* <span data-ttu-id="92745-511">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="92745-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="92745-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="92745-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="92745-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="92745-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="92745-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="92745-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="92745-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="92745-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="92745-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="92745-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="92745-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="92745-517">AzureRM.Websites</span></span>
* <span data-ttu-id="92745-518">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="92745-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="92745-519">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="92745-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="92745-520">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="92745-520">AzureRM.Profile</span></span>
* <span data-ttu-id="92745-521">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="92745-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="92745-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="92745-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="92745-523">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="92745-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="92745-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="92745-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="92745-525">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="92745-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="92745-526">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92745-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="92745-527">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="92745-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="92745-528">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="92745-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="92745-529">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="92745-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="92745-530">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="92745-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="92745-531">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="92745-531">Added support for MSI identity</span></span>
* <span data-ttu-id="92745-532">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="92745-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="92745-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="92745-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="92745-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="92745-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="92745-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="92745-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="92745-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="92745-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="92745-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="92745-537">AzureRM.Batch</span></span>
* <span data-ttu-id="92745-538">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="92745-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="92745-539">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="92745-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="92745-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="92745-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="92745-541">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="92745-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="92745-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="92745-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="92745-543">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="92745-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="92745-544">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="92745-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="92745-545">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="92745-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="92745-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="92745-546">AzureRM.Network</span></span>
* <span data-ttu-id="92745-547">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="92745-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="92745-548">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="92745-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="92745-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="92745-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="92745-550">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="92745-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="92745-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="92745-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="92745-552">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="92745-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="92745-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="92745-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="92745-554">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="92745-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="92745-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="92745-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="92745-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="92745-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="92745-557">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="92745-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="92745-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="92745-558">AzureRM.Sql</span></span>
* <span data-ttu-id="92745-559">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="92745-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="92745-560">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="92745-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="92745-561">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="92745-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="92745-562">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="92745-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="92745-563">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="92745-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="92745-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="92745-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="92745-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="92745-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="92745-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="92745-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="92745-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="92745-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="92745-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="92745-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="92745-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="92745-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="92745-570">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="92745-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
