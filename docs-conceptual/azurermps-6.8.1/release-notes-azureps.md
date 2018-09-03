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
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250312"
---
# <a name="release-notes"></a><span data-ttu-id="fc2ca-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="fc2ca-103">Release notes</span></span>

<span data-ttu-id="fc2ca-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="fc2ca-105">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fc2ca-106">Geral</span><span class="sxs-lookup"><span data-stu-id="fc2ca-106">General</span></span>
* <span data-ttu-id="fc2ca-107">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-108">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-108">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-109">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="fc2ca-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fc2ca-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-110">AzureRM.Compute</span></span>
* <span data-ttu-id="fc2ca-111">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="fc2ca-112">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="fc2ca-113">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="fc2ca-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="fc2ca-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="fc2ca-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="fc2ca-115">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="fc2ca-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fc2ca-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fc2ca-116">AzureRM.Network</span></span>
* <span data-ttu-id="fc2ca-117">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="fc2ca-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fc2ca-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fc2ca-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fc2ca-119">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="fc2ca-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fc2ca-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fc2ca-120">AzureRM.Resources</span></span>
* <span data-ttu-id="fc2ca-121">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fc2ca-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fc2ca-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fc2ca-123">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="fc2ca-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fc2ca-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fc2ca-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fc2ca-125">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="fc2ca-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="fc2ca-126">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="fc2ca-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="fc2ca-127">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="fc2ca-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="fc2ca-128">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="fc2ca-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="fc2ca-129">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="fc2ca-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="fc2ca-130">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="fc2ca-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="fc2ca-131">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="fc2ca-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fc2ca-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fc2ca-132">AzureRM.Websites</span></span>
* <span data-ttu-id="fc2ca-133">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="fc2ca-134">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-135">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-135">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-136">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fc2ca-137">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="fc2ca-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="fc2ca-138">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="fc2ca-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="fc2ca-139">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="fc2ca-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="fc2ca-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-140">Azure.Storage</span></span>
* <span data-ttu-id="fc2ca-141">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="fc2ca-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="fc2ca-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="fc2ca-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fc2ca-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fc2ca-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fc2ca-144">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="fc2ca-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fc2ca-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="fc2ca-146">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fc2ca-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fc2ca-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fc2ca-148">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="fc2ca-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="fc2ca-150">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fc2ca-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fc2ca-151">AzureRM.Automation</span></span>
* <span data-ttu-id="fc2ca-152">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="fc2ca-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="fc2ca-153">AzureRM.Backup</span></span>
* <span data-ttu-id="fc2ca-154">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="fc2ca-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fc2ca-155">AzureRM.Batch</span></span>
* <span data-ttu-id="fc2ca-156">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="fc2ca-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="fc2ca-157">AzureRM.Billing</span></span>
* <span data-ttu-id="fc2ca-158">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="fc2ca-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="fc2ca-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="fc2ca-160">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="fc2ca-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="fc2ca-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="fc2ca-162">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fc2ca-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-163">AzureRM.Compute</span></span>
* <span data-ttu-id="fc2ca-164">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fc2ca-165">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="fc2ca-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="fc2ca-166">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="fc2ca-167">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="fc2ca-168">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="fc2ca-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="fc2ca-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="fc2ca-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="fc2ca-170">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="fc2ca-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="fc2ca-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="fc2ca-172">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="fc2ca-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fc2ca-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="fc2ca-174">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="fc2ca-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="fc2ca-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="fc2ca-176">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fc2ca-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fc2ca-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fc2ca-178">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fc2ca-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fc2ca-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fc2ca-180">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fc2ca-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fc2ca-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fc2ca-182">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="fc2ca-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="fc2ca-183">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fc2ca-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="fc2ca-184">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fc2ca-185">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc2ca-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="fc2ca-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="fc2ca-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="fc2ca-187">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="fc2ca-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="fc2ca-188">AzureRM.Dns</span></span>
* <span data-ttu-id="fc2ca-189">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="fc2ca-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fc2ca-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fc2ca-191">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fc2ca-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fc2ca-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="fc2ca-193">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="fc2ca-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="fc2ca-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="fc2ca-195">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fc2ca-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-196">AzureRM.Insights</span></span>
* <span data-ttu-id="fc2ca-197">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="fc2ca-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="fc2ca-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="fc2ca-199">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fc2ca-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc2ca-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fc2ca-201">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="fc2ca-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fc2ca-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="fc2ca-203">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="fc2ca-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="fc2ca-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="fc2ca-205">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="fc2ca-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="fc2ca-207">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="fc2ca-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="fc2ca-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="fc2ca-209">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="fc2ca-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="fc2ca-210">AzureRM.Media</span></span>
* <span data-ttu-id="fc2ca-211">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fc2ca-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fc2ca-212">AzureRM.Network</span></span>
* <span data-ttu-id="fc2ca-213">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fc2ca-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="fc2ca-214">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fc2ca-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fc2ca-215">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fc2ca-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="fc2ca-216">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fc2ca-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="fc2ca-217">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fc2ca-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="fc2ca-218">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fc2ca-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="fc2ca-219">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="fc2ca-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="fc2ca-220">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="fc2ca-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="fc2ca-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fc2ca-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="fc2ca-222">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="fc2ca-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fc2ca-224">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="fc2ca-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="fc2ca-226">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="fc2ca-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="fc2ca-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="fc2ca-228">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="fc2ca-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="fc2ca-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="fc2ca-230">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fc2ca-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fc2ca-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fc2ca-232">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="fc2ca-233">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="fc2ca-234">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="fc2ca-235">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="fc2ca-236">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="fc2ca-237">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="fc2ca-238">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="fc2ca-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="fc2ca-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="fc2ca-240">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="fc2ca-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="fc2ca-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="fc2ca-242">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fc2ca-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fc2ca-243">AzureRM.Relay</span></span>
* <span data-ttu-id="fc2ca-244">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fc2ca-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fc2ca-245">AzureRM.Resources</span></span>
* <span data-ttu-id="fc2ca-246">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="fc2ca-247">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="fc2ca-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="fc2ca-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="fc2ca-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="fc2ca-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="fc2ca-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="fc2ca-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="fc2ca-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="fc2ca-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="fc2ca-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="fc2ca-255">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc2ca-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="fc2ca-256">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="fc2ca-257">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="fc2ca-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="fc2ca-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="fc2ca-259">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fc2ca-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fc2ca-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fc2ca-261">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fc2ca-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fc2ca-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fc2ca-263">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fc2ca-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fc2ca-264">AzureRM.Sql</span></span>
* <span data-ttu-id="fc2ca-265">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fc2ca-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-266">AzureRM.Storage</span></span>
* <span data-ttu-id="fc2ca-267">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="fc2ca-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="fc2ca-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="fc2ca-269">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="fc2ca-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="fc2ca-270">AzureRM.Tags</span></span>
* <span data-ttu-id="fc2ca-271">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fc2ca-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fc2ca-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fc2ca-273">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="fc2ca-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="fc2ca-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="fc2ca-275">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fc2ca-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fc2ca-276">AzureRM.Websites</span></span>
* <span data-ttu-id="fc2ca-277">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="fc2ca-278">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fc2ca-279">Geral</span><span class="sxs-lookup"><span data-stu-id="fc2ca-279">General</span></span>
* <span data-ttu-id="fc2ca-280">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-281">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-281">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-282">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="fc2ca-283">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fc2ca-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-284">Azure.Storage</span></span>
* <span data-ttu-id="fc2ca-285">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="fc2ca-286">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fc2ca-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fc2ca-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fc2ca-288">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="fc2ca-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="fc2ca-289">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="fc2ca-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="fc2ca-290">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="fc2ca-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="fc2ca-291">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="fc2ca-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="fc2ca-292">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="fc2ca-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="fc2ca-293">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="fc2ca-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fc2ca-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-294">AzureRM.Compute</span></span>
* <span data-ttu-id="fc2ca-295">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="fc2ca-296">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="fc2ca-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="fc2ca-297">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="fc2ca-298">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="fc2ca-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="fc2ca-299">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="fc2ca-300">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="fc2ca-301">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="fc2ca-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="fc2ca-302">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="fc2ca-303">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="fc2ca-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="fc2ca-304">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fc2ca-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fc2ca-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fc2ca-306">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="fc2ca-307">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="fc2ca-308">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="fc2ca-309">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fc2ca-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fc2ca-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fc2ca-311">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="fc2ca-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fc2ca-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fc2ca-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="fc2ca-313">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="fc2ca-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="fc2ca-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-314">AzureRM.Insights</span></span>
* <span data-ttu-id="fc2ca-315">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="fc2ca-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="fc2ca-316">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="fc2ca-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fc2ca-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc2ca-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fc2ca-318">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fc2ca-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fc2ca-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fc2ca-319">AzureRM.Network</span></span>
* <span data-ttu-id="fc2ca-320">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fc2ca-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fc2ca-321">AzureRM.Resources</span></span>
* <span data-ttu-id="fc2ca-322">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="fc2ca-323">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fc2ca-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fc2ca-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fc2ca-325">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="fc2ca-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="fc2ca-326">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="fc2ca-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="fc2ca-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fc2ca-327">AzureRM.Sql</span></span>
* <span data-ttu-id="fc2ca-328">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="fc2ca-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="fc2ca-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="fc2ca-330">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="fc2ca-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="fc2ca-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="fc2ca-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="fc2ca-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="fc2ca-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="fc2ca-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="fc2ca-334">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fc2ca-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="fc2ca-335">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="fc2ca-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="fc2ca-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-336">AzureRM.Storage</span></span>
* <span data-ttu-id="fc2ca-337">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="fc2ca-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="fc2ca-338">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="fc2ca-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="fc2ca-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc2ca-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fc2ca-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc2ca-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="fc2ca-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc2ca-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="fc2ca-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="fc2ca-342">AzureRM.Tags</span></span>
* <span data-ttu-id="fc2ca-343">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="fc2ca-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="fc2ca-344">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-345">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-345">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-346">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fc2ca-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-347">Azure.Storage</span></span>
* <span data-ttu-id="fc2ca-348">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="fc2ca-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="fc2ca-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fc2ca-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="fc2ca-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fc2ca-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fc2ca-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fc2ca-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fc2ca-352">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="fc2ca-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="fc2ca-353">AzureRM.Automation</span></span>
* <span data-ttu-id="fc2ca-354">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fc2ca-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-355">AzureRM.Compute</span></span>
* <span data-ttu-id="fc2ca-356">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fc2ca-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="fc2ca-357">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="fc2ca-358">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="fc2ca-359">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="fc2ca-360">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fc2ca-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fc2ca-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="fc2ca-362">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="fc2ca-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fc2ca-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc2ca-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fc2ca-364">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fc2ca-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="fc2ca-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="fc2ca-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="fc2ca-366">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="fc2ca-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fc2ca-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fc2ca-367">AzureRM.Network</span></span>
* <span data-ttu-id="fc2ca-368">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fc2ca-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="fc2ca-369">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="fc2ca-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="fc2ca-370">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="fc2ca-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="fc2ca-371">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="fc2ca-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="fc2ca-372">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="fc2ca-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="fc2ca-373">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="fc2ca-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="fc2ca-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="fc2ca-374">AzureRM.Relay</span></span>
* <span data-ttu-id="fc2ca-375">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="fc2ca-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fc2ca-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fc2ca-376">AzureRM.Resources</span></span>
* <span data-ttu-id="fc2ca-377">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="fc2ca-378">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="fc2ca-379">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="fc2ca-380">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="fc2ca-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="fc2ca-381">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="fc2ca-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="fc2ca-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fc2ca-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fc2ca-383">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="fc2ca-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="fc2ca-384">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="fc2ca-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fc2ca-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fc2ca-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fc2ca-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fc2ca-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fc2ca-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fc2ca-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fc2ca-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="fc2ca-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fc2ca-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="fc2ca-390">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="fc2ca-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fc2ca-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fc2ca-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fc2ca-392">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fc2ca-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fc2ca-393">AzureRM.Sql</span></span>
* <span data-ttu-id="fc2ca-394">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="fc2ca-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="fc2ca-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="fc2ca-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="fc2ca-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="fc2ca-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fc2ca-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fc2ca-397">AzureRM.Websites</span></span>
* <span data-ttu-id="fc2ca-398">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="fc2ca-399">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="fc2ca-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="fc2ca-400">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="fc2ca-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="fc2ca-401">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="fc2ca-402">Geral</span><span class="sxs-lookup"><span data-stu-id="fc2ca-402">General</span></span>
* <span data-ttu-id="fc2ca-403">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="fc2ca-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-404">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-404">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-405">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="fc2ca-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fc2ca-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-406">AzureRM.Compute</span></span>
* <span data-ttu-id="fc2ca-407">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="fc2ca-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="fc2ca-408">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="fc2ca-409">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc2ca-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="fc2ca-410">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="fc2ca-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="fc2ca-411">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="fc2ca-412">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="fc2ca-413">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="fc2ca-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="fc2ca-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="fc2ca-415">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="fc2ca-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc2ca-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="fc2ca-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc2ca-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="fc2ca-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc2ca-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fc2ca-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fc2ca-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fc2ca-420">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fc2ca-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="fc2ca-421">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="fc2ca-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="fc2ca-422">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="fc2ca-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="fc2ca-423">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="fc2ca-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="fc2ca-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="fc2ca-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="fc2ca-425">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="fc2ca-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="fc2ca-426">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="fc2ca-427">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="fc2ca-428">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fc2ca-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc2ca-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fc2ca-430">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="fc2ca-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="fc2ca-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fc2ca-431">AzureRM.Network</span></span>
* <span data-ttu-id="fc2ca-432">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="fc2ca-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="fc2ca-433">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="fc2ca-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="fc2ca-434">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="fc2ca-435">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="fc2ca-436">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fc2ca-437">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fc2ca-438">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="fc2ca-439">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="fc2ca-440">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="fc2ca-441">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="fc2ca-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fc2ca-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fc2ca-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fc2ca-443">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="fc2ca-444">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="fc2ca-445">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fc2ca-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fc2ca-446">AzureRM.Resources</span></span>
* <span data-ttu-id="fc2ca-447">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="fc2ca-448">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fc2ca-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="fc2ca-449">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fc2ca-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="fc2ca-450">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc2ca-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="fc2ca-451">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fc2ca-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="fc2ca-452">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fc2ca-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="fc2ca-453">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="fc2ca-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="fc2ca-454">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="fc2ca-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="fc2ca-455">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="fc2ca-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="fc2ca-456">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="fc2ca-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="fc2ca-457">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="fc2ca-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="fc2ca-458">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="fc2ca-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="fc2ca-459">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="fc2ca-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="fc2ca-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fc2ca-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="fc2ca-461">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fc2ca-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fc2ca-462">AzureRM.Sql</span></span>
* <span data-ttu-id="fc2ca-463">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="fc2ca-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="fc2ca-464">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="fc2ca-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="fc2ca-465">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-466">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-466">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-467">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="fc2ca-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="fc2ca-468">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="fc2ca-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="fc2ca-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-469">Azure.Storage</span></span>
* <span data-ttu-id="fc2ca-470">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fc2ca-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-471">AzureRM.Compute</span></span>
* <span data-ttu-id="fc2ca-472">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="fc2ca-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="fc2ca-473">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="fc2ca-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="fc2ca-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fc2ca-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="fc2ca-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fc2ca-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="fc2ca-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fc2ca-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="fc2ca-477">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="fc2ca-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="fc2ca-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fc2ca-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="fc2ca-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fc2ca-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="fc2ca-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fc2ca-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="fc2ca-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fc2ca-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="fc2ca-482">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fc2ca-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="fc2ca-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="fc2ca-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="fc2ca-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="fc2ca-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="fc2ca-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="fc2ca-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="fc2ca-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="fc2ca-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="fc2ca-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fc2ca-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="fc2ca-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="fc2ca-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="fc2ca-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fc2ca-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="fc2ca-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="fc2ca-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="fc2ca-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="fc2ca-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="fc2ca-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="fc2ca-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="fc2ca-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="fc2ca-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="fc2ca-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fc2ca-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="fc2ca-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="fc2ca-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="fc2ca-498">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="fc2ca-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc2ca-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fc2ca-500">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="fc2ca-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="fc2ca-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="fc2ca-502">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="fc2ca-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="fc2ca-503">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="fc2ca-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="fc2ca-504">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="fc2ca-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="fc2ca-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="fc2ca-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="fc2ca-506">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="fc2ca-507">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fc2ca-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fc2ca-508">AzureRM.Sql</span></span>
* <span data-ttu-id="fc2ca-509">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="fc2ca-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fc2ca-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fc2ca-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fc2ca-511">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="fc2ca-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fc2ca-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fc2ca-512">AzureRM.Websites</span></span>
* <span data-ttu-id="fc2ca-513">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="fc2ca-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="fc2ca-514">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="fc2ca-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="fc2ca-515">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="fc2ca-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="fc2ca-517">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc2ca-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="fc2ca-518">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-519">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-519">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-520">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="fc2ca-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="fc2ca-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="fc2ca-521">AzureRM.Compute</span></span>
* <span data-ttu-id="fc2ca-522">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="fc2ca-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="fc2ca-523">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="fc2ca-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="fc2ca-524">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="fc2ca-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fc2ca-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="fc2ca-526">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="fc2ca-527">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="fc2ca-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="fc2ca-528">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="fc2ca-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="fc2ca-529">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="fc2ca-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="fc2ca-530">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="fc2ca-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="fc2ca-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="fc2ca-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="fc2ca-532">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="fc2ca-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="fc2ca-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fc2ca-533">AzureRM.Network</span></span>
* <span data-ttu-id="fc2ca-534">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="fc2ca-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="fc2ca-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="fc2ca-535">AzureRM.Resources</span></span>
* <span data-ttu-id="fc2ca-536">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="fc2ca-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="fc2ca-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="fc2ca-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="fc2ca-538">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="fc2ca-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="fc2ca-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fc2ca-539">AzureRM.Sql</span></span>
* <span data-ttu-id="fc2ca-540">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="fc2ca-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="fc2ca-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc2ca-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fc2ca-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fc2ca-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="fc2ca-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fc2ca-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="fc2ca-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fc2ca-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="fc2ca-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc2ca-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="fc2ca-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="fc2ca-546">AzureRM.Websites</span></span>
* <span data-ttu-id="fc2ca-547">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="fc2ca-548">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="fc2ca-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="fc2ca-549">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="fc2ca-549">AzureRM.Profile</span></span>
* <span data-ttu-id="fc2ca-550">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="fc2ca-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="fc2ca-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="fc2ca-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="fc2ca-552">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="fc2ca-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fc2ca-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="fc2ca-554">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="fc2ca-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="fc2ca-555">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fc2ca-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="fc2ca-556">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="fc2ca-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="fc2ca-557">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="fc2ca-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="fc2ca-558">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="fc2ca-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="fc2ca-559">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="fc2ca-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="fc2ca-560">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="fc2ca-560">Added support for MSI identity</span></span>
* <span data-ttu-id="fc2ca-561">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="fc2ca-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="fc2ca-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="fc2ca-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="fc2ca-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc2ca-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="fc2ca-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="fc2ca-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="fc2ca-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fc2ca-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="fc2ca-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="fc2ca-566">AzureRM.Batch</span></span>
* <span data-ttu-id="fc2ca-567">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="fc2ca-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="fc2ca-568">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="fc2ca-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="fc2ca-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="fc2ca-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="fc2ca-570">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="fc2ca-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="fc2ca-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="fc2ca-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="fc2ca-572">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="fc2ca-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="fc2ca-573">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc2ca-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="fc2ca-574">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fc2ca-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="fc2ca-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="fc2ca-575">AzureRM.Network</span></span>
* <span data-ttu-id="fc2ca-576">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="fc2ca-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="fc2ca-577">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="fc2ca-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="fc2ca-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc2ca-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="fc2ca-579">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="fc2ca-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fc2ca-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="fc2ca-581">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="fc2ca-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fc2ca-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="fc2ca-583">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="fc2ca-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="fc2ca-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="fc2ca-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="fc2ca-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="fc2ca-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="fc2ca-586">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="fc2ca-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="fc2ca-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="fc2ca-587">AzureRM.Sql</span></span>
* <span data-ttu-id="fc2ca-588">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="fc2ca-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="fc2ca-589">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="fc2ca-590">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="fc2ca-591">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="fc2ca-592">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="fc2ca-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="fc2ca-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc2ca-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="fc2ca-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fc2ca-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="fc2ca-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fc2ca-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="fc2ca-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fc2ca-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="fc2ca-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fc2ca-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="fc2ca-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="fc2ca-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="fc2ca-599">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="fc2ca-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
