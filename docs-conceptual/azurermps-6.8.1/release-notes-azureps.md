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
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383831"
---
# <a name="release-notes"></a><span data-ttu-id="b3bc1-103">Notas de versão</span><span class="sxs-lookup"><span data-stu-id="b3bc1-103">Release notes</span></span>

<span data-ttu-id="b3bc1-104">É uma lista das alterações feitas nesta versão do Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="b3bc1-105">6.8.1 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b3bc1-106">Geral</span><span class="sxs-lookup"><span data-stu-id="b3bc1-106">General</span></span>
* <span data-ttu-id="b3bc1-107">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b3bc1-108">Assemblies de tempo de execução comum atualizados</span><span class="sxs-lookup"><span data-stu-id="b3bc1-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b3bc1-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3bc1-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b3bc1-110">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b3bc1-111">Problema corrigido https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="b3bc1-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="b3bc1-112">Os cmdlets Importar-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate podem agora lidar com caminhos relativos</span><span class="sxs-lookup"><span data-stu-id="b3bc1-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="b3bc1-113">Problema corrigido https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="b3bc1-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="b3bc1-114">O CertificateInformation é uma propriedade configurável, permitindo que o cmdlet Set-AzureRmApiManagement funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="b3bc1-115">Corrigida pela atualização para o nuget 4.0.4-nuget de prévia</span><span class="sxs-lookup"><span data-stu-id="b3bc1-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="b3bc1-116">Problema corrigido https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="b3bc1-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="b3bc1-117">Corrigido o filtro Odata para pesquisar por nome no produto</span><span class="sxs-lookup"><span data-stu-id="b3bc1-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="b3bc1-118">Problema corrigido https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="b3bc1-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="b3bc1-119">Corrigido o filtro Odata para pesquisar por nome na API</span><span class="sxs-lookup"><span data-stu-id="b3bc1-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="b3bc1-120">Adicionado suporte para o agente de AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="b3bc1-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-121">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-122">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="b3bc1-123">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="b3bc1-124">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="b3bc1-125">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="b3bc1-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-126">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-127">Alterada a representação de saída de cmdlet para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="b3bc1-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b3bc1-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b3bc1-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b3bc1-129">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="b3bc1-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="b3bc1-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b3bc1-130">AzureRM.Resources</span></span>
* <span data-ttu-id="b3bc1-131">Corrigido o problema com a criação de aplicativos gerenciados do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b3bc1-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3bc1-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b3bc1-133">Problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="b3bc1-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b3bc1-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b3bc1-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b3bc1-135">Suporte adicionado para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="b3bc1-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="b3bc1-136">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="b3bc1-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="b3bc1-137">Suporte adicionado para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="b3bc1-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="b3bc1-138">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="b3bc1-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="b3bc1-139">Suporte adicionado para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="b3bc1-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="b3bc1-140">Suporte adicionado para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="b3bc1-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="b3bc1-141">Suporte adicionado para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="b3bc1-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="b3bc1-142">6.8.0 - Agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b3bc1-143">Geral</span><span class="sxs-lookup"><span data-stu-id="b3bc1-143">General</span></span>
* <span data-ttu-id="b3bc1-144">Corrigido o problema com os grupos de recursos padrão não sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-145">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-145">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-146">Adicionada a propriedade de expiração aos tokens retornados durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="b3bc1-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-147">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-148">Corrigido o problema onde o destino está ausente na saída de erro.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="b3bc1-149">Corrigido o problema com o tipo de conta de armazenamento para VM com disco gerenciado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="b3bc1-150">Corrigidos os cmdlets da extensão do AEM para outros ambientes, por exemplo, Azure China</span><span class="sxs-lookup"><span data-stu-id="b3bc1-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="b3bc1-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b3bc1-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="b3bc1-152">Corrigidos os exemplos para New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="b3bc1-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-153">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-154">Alterada a representação dos modelos padrão para exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="b3bc1-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b3bc1-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b3bc1-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b3bc1-156">Corrigida a falha em atualização-AzureRmPowerBIEmbeddedCapacity durante uma tentativa de escalar a capacidade em pausa</span><span class="sxs-lookup"><span data-stu-id="b3bc1-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b3bc1-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b3bc1-157">AzureRM.Resources</span></span>
* <span data-ttu-id="b3bc1-158">Corrigido o problema com a criação de aplicativo gerenciado do MarketPlace.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b3bc1-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3bc1-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b3bc1-160">Correção de problemas</span><span class="sxs-lookup"><span data-stu-id="b3bc1-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b3bc1-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b3bc1-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b3bc1-162">Suporte para o método de roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="b3bc1-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="b3bc1-163">Novo parâmetro “MaxReturn” para o roteamento de vários valores</span><span class="sxs-lookup"><span data-stu-id="b3bc1-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="b3bc1-164">Suporte para o método de roteamento de sub-rede</span><span class="sxs-lookup"><span data-stu-id="b3bc1-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="b3bc1-165">Suporte para intervalos de endereços IP (sub-redes) em pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="b3bc1-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="b3bc1-166">Suporte para cabeçalhos personalizados nos perfis</span><span class="sxs-lookup"><span data-stu-id="b3bc1-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="b3bc1-167">Suporte para intervalos de código de status esperados em perfis</span><span class="sxs-lookup"><span data-stu-id="b3bc1-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="b3bc1-168">Suporte para cabeçalhos personalizados nos pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="b3bc1-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b3bc1-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b3bc1-169">AzureRM.Websites</span></span>
* <span data-ttu-id="b3bc1-170">Corrigido o problema com o grupo de recurso padrão sendo definido incorretamente.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="b3bc1-171">6.7.0 - agosto de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-172">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-172">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-173">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b3bc1-174">Adicionar id de usuário ao nome de contexto padrão para evitar conflitos entre contextos</span><span class="sxs-lookup"><span data-stu-id="b3bc1-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="b3bc1-175">Corrigir problemas com o Clear-AzureRmContext que causou problemas ao selecionar um contexto 6398</span><span class="sxs-lookup"><span data-stu-id="b3bc1-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="b3bc1-176">Habilitar o domínio do locatário a ser passado para o parâmetro “-TenantId” de “Connect-AzureRmAccount”</span><span class="sxs-lookup"><span data-stu-id="b3bc1-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="b3bc1-177">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-177">Azure.Storage</span></span>
* <span data-ttu-id="b3bc1-178">Remover a limitação de 5TB para a cota de Compartilhamento de Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="b3bc1-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="b3bc1-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="b3bc1-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b3bc1-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3bc1-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b3bc1-181">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="b3bc1-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3bc1-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="b3bc1-183">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b3bc1-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3bc1-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b3bc1-185">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="b3bc1-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="b3bc1-187">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b3bc1-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b3bc1-188">AzureRM.Automation</span></span>
* <span data-ttu-id="b3bc1-189">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="b3bc1-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="b3bc1-190">AzureRM.Backup</span></span>
* <span data-ttu-id="b3bc1-191">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b3bc1-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b3bc1-192">AzureRM.Batch</span></span>
* <span data-ttu-id="b3bc1-193">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="b3bc1-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="b3bc1-194">AzureRM.Billing</span></span>
* <span data-ttu-id="b3bc1-195">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="b3bc1-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="b3bc1-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="b3bc1-197">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="b3bc1-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="b3bc1-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="b3bc1-199">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-200">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-201">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b3bc1-202">Adicionar parâmetro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b3bc1-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="b3bc1-203">Use o local padrão no DiskFileParameterSet de New-AzureRmVm se nenhum local for especificado.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="b3bc1-204">Corrigir a descrição do parâmetro em Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b3bc1-205">Corrigir o cmdlet Get-AzureRmVMDiskEncryptionStatus para certos cenários relacionados a uma fase</span><span class="sxs-lookup"><span data-stu-id="b3bc1-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b3bc1-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b3bc1-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="b3bc1-207">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="b3bc1-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="b3bc1-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="b3bc1-209">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="b3bc1-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b3bc1-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="b3bc1-211">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="b3bc1-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="b3bc1-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="b3bc1-213">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b3bc1-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b3bc1-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b3bc1-215">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b3bc1-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b3bc1-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b3bc1-217">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b3bc1-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3bc1-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b3bc1-219">Corrigir depuração quando DebugPreference for definido na linha de comando do powershell</span><span class="sxs-lookup"><span data-stu-id="b3bc1-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="b3bc1-220">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b3bc1-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b3bc1-221">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b3bc1-222">Atualizar exemplo para Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b3bc1-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="b3bc1-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="b3bc1-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="b3bc1-224">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="b3bc1-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="b3bc1-225">AzureRM.Dns</span></span>
* <span data-ttu-id="b3bc1-226">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b3bc1-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b3bc1-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b3bc1-228">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b3bc1-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3bc1-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="b3bc1-230">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="b3bc1-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="b3bc1-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="b3bc1-232">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b3bc1-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-233">AzureRM.Insights</span></span>
* <span data-ttu-id="b3bc1-234">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="b3bc1-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="b3bc1-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="b3bc1-236">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b3bc1-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3bc1-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b3bc1-238">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b3bc1-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b3bc1-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b3bc1-240">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="b3bc1-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="b3bc1-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="b3bc1-242">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="b3bc1-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="b3bc1-244">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="b3bc1-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="b3bc1-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="b3bc1-246">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="b3bc1-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="b3bc1-247">AzureRM.Media</span></span>
* <span data-ttu-id="b3bc1-248">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-249">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-250">Exemplo adicionado para Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3bc1-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="b3bc1-251">Exemplos adicionados e descrições para Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b3bc1-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b3bc1-252">Exemplos adicionados para Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b3bc1-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="b3bc1-253">Exemplo adicionado para Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b3bc1-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b3bc1-254">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b3bc1-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="b3bc1-255">Exemplo adicionado para Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b3bc1-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="b3bc1-256">Cmdlets gerado novamente para ApplicationSecurityGroup, RouteTable e Uso usando o gerador de código mais recente</span><span class="sxs-lookup"><span data-stu-id="b3bc1-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="b3bc1-257">Mensagem de erro esclarecida para Get-AzureRmVirtualNetworkSubnetConfig ao tentar obter uma sub-rede que não existe</span><span class="sxs-lookup"><span data-stu-id="b3bc1-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="b3bc1-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="b3bc1-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="b3bc1-259">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="b3bc1-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b3bc1-261">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b3bc1-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b3bc1-263">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="b3bc1-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="b3bc1-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="b3bc1-265">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="b3bc1-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b3bc1-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="b3bc1-267">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b3bc1-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b3bc1-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b3bc1-269">Filtro de política adicionado ao cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="b3bc1-270">O comando retorna a lista de itens de backup protegidos pela id de política dada.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="b3bc1-271">Microsoft.Azure.Management.RecoveryServices.Backup atualizado para a versão 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="b3bc1-272">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="b3bc1-273">Parâmetro TargetResourceGroupName adicionado a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="b3bc1-274">O grupo de recursos para o qual os discos gerenciados são restaurados.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="b3bc1-275">Aplicável ao backup da VM com discos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="b3bc1-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b3bc1-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="b3bc1-277">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="b3bc1-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="b3bc1-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="b3bc1-279">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b3bc1-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b3bc1-280">AzureRM.Relay</span></span>
* <span data-ttu-id="b3bc1-281">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b3bc1-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b3bc1-282">AzureRM.Resources</span></span>
* <span data-ttu-id="b3bc1-283">Suporte à implantação de modelos no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="b3bc1-284">Adicione novos Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="b3bc1-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="b3bc1-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="b3bc1-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="b3bc1-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="b3bc1-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="b3bc1-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b3bc1-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="b3bc1-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="b3bc1-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="b3bc1-292">Corrigir o problema onde o erro é gerado ao passar um contexto para Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b3bc1-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="b3bc1-293">Corrigir exemplo em New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="b3bc1-294">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b3bc1-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b3bc1-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b3bc1-296">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b3bc1-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3bc1-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b3bc1-298">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b3bc1-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3bc1-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b3bc1-300">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b3bc1-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b3bc1-301">AzureRM.Sql</span></span>
* <span data-ttu-id="b3bc1-302">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b3bc1-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-303">AzureRM.Storage</span></span>
* <span data-ttu-id="b3bc1-304">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="b3bc1-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="b3bc1-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="b3bc1-306">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b3bc1-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b3bc1-307">AzureRM.Tags</span></span>
* <span data-ttu-id="b3bc1-308">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b3bc1-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b3bc1-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b3bc1-310">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="b3bc1-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="b3bc1-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="b3bc1-312">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b3bc1-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b3bc1-313">AzureRM.Websites</span></span>
* <span data-ttu-id="b3bc1-314">Atualização para a versão mais recente do Azure ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="b3bc1-315">6.6.0 – Julho de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b3bc1-316">Geral</span><span class="sxs-lookup"><span data-stu-id="b3bc1-316">General</span></span>
* <span data-ttu-id="b3bc1-317">Todos os arquivos de ajuda atualizados para incluir tipos corretos de entrada/saída e tipos de parâmetro completos.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-318">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-318">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-319">Biblioteca Common.Strategy atualizada para poder validar se a configuração atual de um recurso é compatível com o recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="b3bc1-320">Tipos de ps1xml adicionados a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b3bc1-321">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-321">Azure.Storage</span></span>
* <span data-ttu-id="b3bc1-322">Suporte adicionado para obter o Contexto de Armazenamento em DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="b3bc1-323">Ps1XmlAttribute adicionado às propriedades dos tipos de saída dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b3bc1-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3bc1-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b3bc1-325">Problema corrigido https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="b3bc1-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="b3bc1-326">Corrigido o bug no Automapper para traduzir PsApiManagementApi em ApiContract</span><span class="sxs-lookup"><span data-stu-id="b3bc1-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="b3bc1-327">Problema corrigido https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="b3bc1-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="b3bc1-328">Corrigido o bug File.Save para não ficar sobrecarregado com o tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="b3bc1-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="b3bc1-329">Problema corrigido https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="b3bc1-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="b3bc1-330">Atualizado para a versão 4.0.3 NuGet que corrige a exceção de padrão em apiId</span><span class="sxs-lookup"><span data-stu-id="b3bc1-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-331">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-332">Corrigido o problema com a criação de uma VM usando DiskFileParameterSet em New-AzureRmVm com falha devido à renomeação do tipo de conta de armazenamento PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="b3bc1-333">Corrigir o cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="b3bc1-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="b3bc1-334">Atualizar Get-AzureRmAvailabilitySet para habilitar a lista de todos os conjuntos de disponibilidade em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="b3bc1-335">(O parâmetro ResouceGroupName agora é opcional.)</span><span class="sxs-lookup"><span data-stu-id="b3bc1-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="b3bc1-336">Atualizar SimpleParameterSet de 'New-AzureRmVm' para habilitar rede acelerada em VMs qualificadas.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="b3bc1-337">Atualizar o parâmetro simples New-AzureRmVmss configurado para falhar na criação de vmss quando o balanceador de carga especificado pelo usuário já existir.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="b3bc1-338">Atualizar exemplo de New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b3bc1-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="b3bc1-339">Adicionar exemplo de 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="b3bc1-340">Atualizar descrição de Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="b3bc1-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="b3bc1-341">Atualizar exemplo 1 de Set-AzureRmVMBginfoExtension para corrigir a ortografia e o prefixo.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b3bc1-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b3bc1-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b3bc1-343">Atualizado a versão do SDK do .NET do ADF para 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="b3bc1-344">Suporte ao compartilhamento de tempo de execução da integração auto-hospedada entre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="b3bc1-345">Adicionar novo parâmetro -SharedIntegrationRuntimeResourceId ao cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="b3bc1-346">Adicionar novo parâmetro opcional -LinkedDataFactoryName ao cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b3bc1-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3bc1-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b3bc1-348">Atualizada a versão do SDK do DataPlane (Microsoft.Azure.DataLake.Store) para 1.1.9</span><span class="sxs-lookup"><span data-stu-id="b3bc1-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b3bc1-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3bc1-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="b3bc1-350">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="b3bc1-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b3bc1-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-351">AzureRM.Insights</span></span>
* <span data-ttu-id="b3bc1-352">Formatação corrigida do OutputType nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="b3bc1-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="b3bc1-353">Usando o SDK Microsoft.Azure.Management.Monitor 0.19.1-preview</span><span class="sxs-lookup"><span data-stu-id="b3bc1-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b3bc1-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3bc1-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b3bc1-355">Corrigir o problema de tubulação em Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3bc1-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-356">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-357">Exemplos adicionados para cmdlets LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b3bc1-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b3bc1-358">AzureRM.Resources</span></span>
* <span data-ttu-id="b3bc1-359">Corrigir problema ao fornecer nome e valor da marca para 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="b3bc1-360">Corrigir o cenário de tubulação com 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b3bc1-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3bc1-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b3bc1-362">Tubulação atualizada para InputObject e ResourceId em Remover cmdlets</span><span class="sxs-lookup"><span data-stu-id="b3bc1-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="b3bc1-363">alguns problemas corrigidos</span><span class="sxs-lookup"><span data-stu-id="b3bc1-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="b3bc1-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b3bc1-364">AzureRM.Sql</span></span>
* <span data-ttu-id="b3bc1-365">Adicionando suporte à Proteção Avançada contra Ameaças do Server com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="b3bc1-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3bc1-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b3bc1-367">Adicionando suporte à Avaliação de Vulnerabilidade com os seguintes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="b3bc1-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="b3bc1-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="b3bc1-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="b3bc1-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="b3bc1-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="b3bc1-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="b3bc1-371">Corrigido o exemplo em Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3bc1-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="b3bc1-372">Corrigir tratamento de data e hora incorreto para cultura de base não EUA em Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="b3bc1-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b3bc1-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-373">AzureRM.Storage</span></span>
* <span data-ttu-id="b3bc1-374">Adicionar Ps1XmlAttribute às propriedades de tipos de saída de cmdlets</span><span class="sxs-lookup"><span data-stu-id="b3bc1-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="b3bc1-375">Mostrar a saída do cmdlet StorageAccount no modo de exibição de tabela</span><span class="sxs-lookup"><span data-stu-id="b3bc1-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="b3bc1-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3bc1-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b3bc1-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3bc1-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b3bc1-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b3bc1-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b3bc1-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b3bc1-379">AzureRM.Tags</span></span>
* <span data-ttu-id="b3bc1-380">Remover instrução incorreta de ajuda de cmdlet de marca</span><span class="sxs-lookup"><span data-stu-id="b3bc1-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="b3bc1-381">6.5.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-382">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-382">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-383">Ajuda atualizada para 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b3bc1-384">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-384">Azure.Storage</span></span>
* <span data-ttu-id="b3bc1-385">Suporte ao carregar o blob ou o arquivo com o token de Sas somente gravação</span><span class="sxs-lookup"><span data-stu-id="b3bc1-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="b3bc1-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b3bc1-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="b3bc1-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b3bc1-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b3bc1-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3bc1-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b3bc1-389">Adicione a propriedade necessária ResourceGroupName ao AS.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b3bc1-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b3bc1-390">AzureRM.Automation</span></span>
* <span data-ttu-id="b3bc1-391">Atualizar a ajuda e adicionar exemplo do 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-392">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-393">Adicionar parâmetro -Tag ao New/Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b3bc1-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="b3bc1-394">Adicionar exemplo do 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b3bc1-395">Adicionar exemplos do 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b3bc1-396">Atualizar ajuda do 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="b3bc1-397">Atualize SimpleParameterSet do New-AzureRmVmss para definir SinglePlacementGroup como false por padrão e adicionar o parâmetro de opção 'SinglePlacementGroup', que permite ao usuário criar VMSS em um único grupo de posicionamento.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b3bc1-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3bc1-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="b3bc1-399">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSEventHubDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="b3bc1-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b3bc1-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3bc1-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b3bc1-401">Mensagem de erro de atualização para Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3bc1-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b3bc1-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b3bc1-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b3bc1-403">Corrigido o erro de "conjunto de parâmetros não pôde ser resolvido" no New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b3bc1-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-404">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-405">Habilitar o emparelhamento entre redes virtuais em vários locatários para o Add/Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b3bc1-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="b3bc1-406">Atualizados os cmdlets abaixo para o Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="b3bc1-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="b3bc1-407">New-AzureRmApplicationGateway: Adicionado o sinalizador EnableFIPS e suporte a Zonas</span><span class="sxs-lookup"><span data-stu-id="b3bc1-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="b3bc1-408">New-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b3bc1-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="b3bc1-409">Set-AzureRmApplicationGatewaySku: Adicionados novos skus Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b3bc1-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="b3bc1-410">Cmdlets de RouteTable regenerados com a versão mais recente do gerador</span><span class="sxs-lookup"><span data-stu-id="b3bc1-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b3bc1-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b3bc1-411">AzureRM.Relay</span></span>
* <span data-ttu-id="b3bc1-412">Arquivos markdown atualizados, correção para o problema de nome de parâmetro no exemplo</span><span class="sxs-lookup"><span data-stu-id="b3bc1-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b3bc1-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b3bc1-413">AzureRM.Resources</span></span>
* <span data-ttu-id="b3bc1-414">Atualize os cmdlets Roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="b3bc1-415">Remova chamadas extras roledefinition feitas como parte da paginação.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="b3bc1-416">Corrigir cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="b3bc1-417">Corrigir funcionalidade de parâmetro de comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="b3bc1-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="b3bc1-418">Corrigir problema com 'Get-AzureRmResource', no qual o parâmetro '-ResourceType' diferencia maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="b3bc1-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b3bc1-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3bc1-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b3bc1-420">Adicionado o parâmetro top e skip aos cmdlets de lista</span><span class="sxs-lookup"><span data-stu-id="b3bc1-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="b3bc1-421">Adicionados os cmdlets de migração de NameSpace Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="b3bc1-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b3bc1-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b3bc1-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b3bc1-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b3bc1-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b3bc1-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b3bc1-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b3bc1-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b3bc1-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b3bc1-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="b3bc1-427">Adicionada uma propriedade readonly 'PendingReplicationOperationsCount' à classe PSServiceBusDRConfigurationAttributes, que fornece a contagem de operações pendentes de replicação durante a replicação em andamento</span><span class="sxs-lookup"><span data-stu-id="b3bc1-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b3bc1-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3bc1-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b3bc1-429">Exemplo de atualização para 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b3bc1-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b3bc1-430">AzureRM.Sql</span></span>
* <span data-ttu-id="b3bc1-431">Adicionar novos Cmdlets ao Management.Sql para permitir que os clientes adicionem o certificado TDE à instância do SQL Server ou uma Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="b3bc1-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="b3bc1-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b3bc1-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="b3bc1-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b3bc1-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b3bc1-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b3bc1-434">AzureRM.Websites</span></span>
* <span data-ttu-id="b3bc1-435">`Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` quando definidos como false agora também removerão a propriedade de identidade da marca de visualização object.Removing do site.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="b3bc1-436">Exemplos `Get-AzureRmWebAppMetrics` e `Get-AzureRmAppServicePlanMetrics` atualizados</span><span class="sxs-lookup"><span data-stu-id="b3bc1-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="b3bc1-437">`Set-AzureRmWebApp -PhpVersion` dá suporte como uma versão do PHP válida</span><span class="sxs-lookup"><span data-stu-id="b3bc1-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="b3bc1-438">6.4.0 - julho de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b3bc1-439">Geral</span><span class="sxs-lookup"><span data-stu-id="b3bc1-439">General</span></span>
* <span data-ttu-id="b3bc1-440">Formatação corrigida do OutputType nos arquivos de ajuda para a maioria dos módulos</span><span class="sxs-lookup"><span data-stu-id="b3bc1-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-441">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-441">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-442">Atributo Ps1Xml adicionado aos tipos de saída básicos</span><span class="sxs-lookup"><span data-stu-id="b3bc1-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-443">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-444">Recurso de Marca do IP para VMSS</span><span class="sxs-lookup"><span data-stu-id="b3bc1-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="b3bc1-445">O cmdlet “New-AzureRmVmssIpTagConfig” foi adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="b3bc1-446">O parâmetro IpTag foi adicionado a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="b3bc1-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b3bc1-447">Recurso de Reversão Automática do SO para VMSS</span><span class="sxs-lookup"><span data-stu-id="b3bc1-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="b3bc1-448">Os parâmetros DisableAutoRollback são adicionados a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="b3bc1-449">Recurso do Histórico de Atualizações do SO para Vmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="b3bc1-450">O parâmetro com argumento OSUpgradeHistory foi adicionado ao Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b3bc1-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b3bc1-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b3bc1-452">Adicione suporte para as ACLs de Catálogo com os comandos a seguir:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="b3bc1-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b3bc1-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b3bc1-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b3bc1-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b3bc1-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b3bc1-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b3bc1-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3bc1-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b3bc1-457">Adicionar suporte a cancelamento e acompanhamento do progresso para Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b3bc1-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b3bc1-458">Adicionar suporte a cancelamento para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b3bc1-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b3bc1-459">Corrigir liberação das mensagens de depuração para cmdlets que fazem operações recursivas</span><span class="sxs-lookup"><span data-stu-id="b3bc1-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="b3bc1-460">Corrigir local de teste dos cmdlets DataLake</span><span class="sxs-lookup"><span data-stu-id="b3bc1-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b3bc1-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b3bc1-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="b3bc1-462">Parâmetro MaxCount Opcional adicionado aos cmdlets da Lista de Operações Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b3bc1-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="b3bc1-463">Problema corrigido no cmdlet New-AzureRmEventHub onde pelo menos um parâmetro é necessário durante a criação do Novo EventHub.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="b3bc1-464">Conjunto de Parâmetros Padrão fornecido.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="b3bc1-465">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmEventHubKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b3bc1-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3bc1-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b3bc1-467">Problema corrigido onde todos os recursos foram retornados por Get-AzureRmKeyVault-Tag</span><span class="sxs-lookup"><span data-stu-id="b3bc1-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-468">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-469">Expor novas Skus para Zone-Redundant VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="b3bc1-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="b3bc1-470">Novos comandos adicionados do recurso: APIs de Parceiro do ExpressRoute via ARM</span><span class="sxs-lookup"><span data-stu-id="b3bc1-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="b3bc1-471">Get-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b3bc1-472">Set-AzureRmExpressRouteCrossConnection adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b3bc1-473">Add-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b3bc1-474">Get-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b3bc1-475">Remove-AzureRmExpressRouteCrossConnectionPeering adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b3bc1-476">Get-AzureRMExpressRouteCrossConnectionArpTable adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b3bc1-477">Get-AzureRMExpressRouteCrossConnectionRouteTable adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b3bc1-478">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary adicionado</span><span class="sxs-lookup"><span data-stu-id="b3bc1-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b3bc1-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b3bc1-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b3bc1-480">Cmdlet Get-AzureRmRecoveryServicesBackupStatus adicionado.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="b3bc1-481">Esse cmdlet usa uma ID de VM e verifica se a VM está protegida por algum cofre na assinatura.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="b3bc1-482">Se houver tal cofre, o cmdlet produzirá detalhes dele.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b3bc1-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b3bc1-483">AzureRM.Resources</span></span>
* <span data-ttu-id="b3bc1-484">Atualize os cmdlets Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="b3bc1-485">Adicionar suporte para listar valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="b3bc1-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="b3bc1-486">Adicionar suporte para recuperar as atribuições individuais com valores -Scope no nível do grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="b3bc1-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="b3bc1-487">Adicionar argumentos -Effective e -All para controlar  parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3bc1-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="b3bc1-488">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b3bc1-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="b3bc1-489">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="b3bc1-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b3bc1-490">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="b3bc1-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b3bc1-491">Atualizar cmdlets Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b3bc1-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="b3bc1-492">Adicionar parâmetro -ManagementGroupName para aplicar as operações a um determinado grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="b3bc1-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b3bc1-493">Adicionar parâmetro -SubscriptionId para aplicar as operações a uma determinada assinatura</span><span class="sxs-lookup"><span data-stu-id="b3bc1-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b3bc1-494">Adicionar suporte de referência do segredo KeyVault nos parâmetros ao usar “TemplateParameterObject” em “New-AzureRmResourceGroupDeployment”</span><span class="sxs-lookup"><span data-stu-id="b3bc1-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="b3bc1-495">Corrigir problema onde o parâmetro “-EndDate” foi ignorado para “New-AzureRmADAppCredential”</span><span class="sxs-lookup"><span data-stu-id="b3bc1-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="b3bc1-496">Corrigir problema onde “Add-AzureRmADGroupMember” usou a URL incorreta para fazer a solicitação</span><span class="sxs-lookup"><span data-stu-id="b3bc1-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="b3bc1-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b3bc1-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b3bc1-498">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmServiceBusKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b3bc1-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b3bc1-499">AzureRM.Sql</span></span>
* <span data-ttu-id="b3bc1-500">Pontos de Restauração Definidos pelo Usuário e Esclarecidos para SQLDW na ajuda do New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b3bc1-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="b3bc1-501">Documentação atualizada do parâmetro -ComputeGeneration em vários cmdlets</span><span class="sxs-lookup"><span data-stu-id="b3bc1-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="b3bc1-502">6.3.0 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-503">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-503">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-504">Mensagens de erro atualizadas para Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="b3bc1-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="b3bc1-505">Criar contexto para cada assinatura ao executar “Connect-AzureRmAccount” sem contexto anterior</span><span class="sxs-lookup"><span data-stu-id="b3bc1-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b3bc1-506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-506">Azure.Storage</span></span>
* <span data-ttu-id="b3bc1-507">Outras informações adicionadas sobre o parâmetro -Permissions nos arquivos de ajuda.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-508">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-509">“Get-AzureRmVmDiskEncryptionStatus” corrige um problema observado por VMs sem discos de dados</span><span class="sxs-lookup"><span data-stu-id="b3bc1-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="b3bc1-510">Atualizar versão da Biblioteca do cliente de computação para corrigir os cmdlets a seguir</span><span class="sxs-lookup"><span data-stu-id="b3bc1-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="b3bc1-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b3bc1-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b3bc1-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b3bc1-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b3bc1-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b3bc1-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b3bc1-514">Cmdlets corrigidos a seguir para mostrar corretamente a "ID da operação" e o "status da operação":</span><span class="sxs-lookup"><span data-stu-id="b3bc1-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="b3bc1-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b3bc1-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="b3bc1-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b3bc1-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="b3bc1-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b3bc1-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="b3bc1-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b3bc1-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="b3bc1-519">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b3bc1-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="b3bc1-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="b3bc1-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b3bc1-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="b3bc1-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b3bc1-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="b3bc1-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="b3bc1-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="b3bc1-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="b3bc1-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3bc1-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="b3bc1-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b3bc1-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="b3bc1-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b3bc1-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b3bc1-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b3bc1-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="b3bc1-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b3bc1-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b3bc1-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b3bc1-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="b3bc1-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b3bc1-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="b3bc1-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b3bc1-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b3bc1-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b3bc1-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b3bc1-535">Remova as condições de validação ValidateNotNullOrEmpty para SubjectBeginsWith/SubjectEndsWith no cmdlet Update-AzureRmEventGridSubscription e permita a mudança desses parâmetros para uma cadeia de caracteres vazia, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b3bc1-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3bc1-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b3bc1-537">Corrigir problema onde nenhuma marca retorna ao executar Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="b3bc1-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b3bc1-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b3bc1-539">Versão pública dos cmdlets de Informações sobre a Política</span><span class="sxs-lookup"><span data-stu-id="b3bc1-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="b3bc1-540">Usar versão da API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="b3bc1-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="b3bc1-541">Adicionar PolicyDefinitionReferenceId aos resultados de Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="b3bc1-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b3bc1-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b3bc1-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b3bc1-543">Parâmetro -Vault adicionado aos cmdlets RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="b3bc1-544">Quando passado, substituirá o cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b3bc1-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b3bc1-545">AzureRM.Sql</span></span>
* <span data-ttu-id="b3bc1-546">Exemplo atualizado no arquivo de ajuda para Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="b3bc1-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b3bc1-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b3bc1-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b3bc1-548">Arquivo de ajuda atualizado para Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b3bc1-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b3bc1-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b3bc1-549">AzureRM.Websites</span></span>
* <span data-ttu-id="b3bc1-550">"Set-AzureRmWebApp" foi atualizado para não substituir AppSettings ao usar -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b3bc1-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="b3bc1-551">"New-AzureRmWebAppSlot" foi atualizado para aceitar AppServicePlan como um parâmetro opcional</span><span class="sxs-lookup"><span data-stu-id="b3bc1-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="b3bc1-552">6.2.1 - junho de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="b3bc1-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b3bc1-554">Modelo PSWorkspace atualizado para permitir que a Rede use o tipo como um parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3bc1-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="b3bc1-555">6.2.0 - Junho de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-556">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-556">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-557">Corrija o problema em que a versão 10.0.3 do Newtonsoft.Json não estava sendo carregado na importação do módulo</span><span class="sxs-lookup"><span data-stu-id="b3bc1-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b3bc1-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b3bc1-558">AzureRM.Compute</span></span>
* <span data-ttu-id="b3bc1-559">Recurso de atualização de VM VMSS</span><span class="sxs-lookup"><span data-stu-id="b3bc1-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="b3bc1-560">Os cmdlets 'Update-AzureRmVmssVM' e 'New-AzureRmVMDataDisk' foram adicionados</span><span class="sxs-lookup"><span data-stu-id="b3bc1-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="b3bc1-561">Adicione o parâmetro VirtualMachineScaleSetVM ao cmdlet 'Add-AzureRmVMDataDisk' para dar suporte à adição de um disco de dados para a VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b3bc1-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b3bc1-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b3bc1-563">A versão do SDK do .Net ADF foi atualizada para a versão prévia 0.8.0 que contém as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="b3bc1-564">A operação para Configurar o repositório de fábrica foi adicionada</span><span class="sxs-lookup"><span data-stu-id="b3bc1-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="b3bc1-565">O LinkedService QuickBooks foi atualizado para expor as propriedades consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="b3bc1-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="b3bc1-566">Vários tipos de modelo atualizados de SecretBase para Object</span><span class="sxs-lookup"><span data-stu-id="b3bc1-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="b3bc1-567">Foram adicionados gatilho de eventos de blob</span><span class="sxs-lookup"><span data-stu-id="b3bc1-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="b3bc1-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b3bc1-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b3bc1-569">Atualizar documentação com a saída de exemplo</span><span class="sxs-lookup"><span data-stu-id="b3bc1-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-570">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-571">Habilitar parâmetros de Análise de Tráfego nos cmdlets do Observador de Rede</span><span class="sxs-lookup"><span data-stu-id="b3bc1-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b3bc1-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b3bc1-572">AzureRM.Resources</span></span>
* <span data-ttu-id="b3bc1-573">Corrigir o problema com a propriedade 'Properties' dos objetos 'PSResource' retornados de 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="b3bc1-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b3bc1-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b3bc1-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b3bc1-575">Corrigir o problema com a atualização de ServiceBusQueueJob não definindo novos valores de Autenticação</span><span class="sxs-lookup"><span data-stu-id="b3bc1-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="b3bc1-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b3bc1-576">AzureRM.Sql</span></span>
* <span data-ttu-id="b3bc1-577">Os seguintes cmdlets foram atualizados com o parâmetro LicenseType opcional</span><span class="sxs-lookup"><span data-stu-id="b3bc1-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="b3bc1-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b3bc1-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b3bc1-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b3bc1-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b3bc1-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b3bc1-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b3bc1-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b3bc1-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b3bc1-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b3bc1-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b3bc1-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b3bc1-583">AzureRM.Websites</span></span>
* <span data-ttu-id="b3bc1-584">'New-AzureRMWebApp' será atualizado para usar os algoritmos comuns da biblioteca de Estratégia.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="b3bc1-585">6.1.0 - maio de 2018</span><span class="sxs-lookup"><span data-stu-id="b3bc1-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b3bc1-586">AzureRM.profile</span><span class="sxs-lookup"><span data-stu-id="b3bc1-586">AzureRM.Profile</span></span>
* <span data-ttu-id="b3bc1-587">Corrija o problema onde executar “Clear-AzureRmContext” manteria um contexto vazio com o nome do contexto padrão anterior, o que impediu o usuário de criar um novo contexto com o antigo nome</span><span class="sxs-lookup"><span data-stu-id="b3bc1-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b3bc1-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b3bc1-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b3bc1-589">Habilite as operações de associação/desassociação do Gateway no sistema autônomo.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b3bc1-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b3bc1-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b3bc1-591">Suporte adicionado para ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="b3bc1-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="b3bc1-592">Suporte adicionado para Back-end do ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3bc1-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="b3bc1-593">Suporte adicionado para Agente do Application Insights</span><span class="sxs-lookup"><span data-stu-id="b3bc1-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="b3bc1-594">Suporte adicionado para reconhecer a sku “Básica” como uma sku válida do serviço de Gerenciamento da Api</span><span class="sxs-lookup"><span data-stu-id="b3bc1-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="b3bc1-595">Suporte adicionado para instalar os Certificados emitidos pela autoridade de certificação privada como Raiz ou CA</span><span class="sxs-lookup"><span data-stu-id="b3bc1-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="b3bc1-596">Suporte adicionado para aceitar certificados SSL Personalizados via KeyVault e vários nomes de host do proxy</span><span class="sxs-lookup"><span data-stu-id="b3bc1-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="b3bc1-597">Suporte adicionado para a identidade MSI</span><span class="sxs-lookup"><span data-stu-id="b3bc1-597">Added support for MSI identity</span></span>
* <span data-ttu-id="b3bc1-598">Suporte adicionado para aceitar Políticas via Url OBSERVAÇÃO: os cmdlets a seguir serão preteridos na futura versão</span><span class="sxs-lookup"><span data-stu-id="b3bc1-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="b3bc1-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="b3bc1-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="b3bc1-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3bc1-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="b3bc1-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="b3bc1-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="b3bc1-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b3bc1-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b3bc1-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b3bc1-603">AzureRM.Batch</span></span>
* <span data-ttu-id="b3bc1-604">Versão do novo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b3bc1-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="b3bc1-605">Versão novo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="b3bc1-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b3bc1-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b3bc1-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="b3bc1-607">Adicionar os novos parâmetros Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top no cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="b3bc1-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b3bc1-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b3bc1-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b3bc1-609">Corrigir exemplo para Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b3bc1-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b3bc1-610">Corrigir exceção do parâmetro nulo para Recurse, caso esteja em Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b3bc1-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="b3bc1-611">Corrigir arquivos de ajuda para Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b3bc1-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="b3bc1-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b3bc1-612">AzureRM.Network</span></span>
* <span data-ttu-id="b3bc1-613">Aumentar a versão do SDK de Rede de 18.0.0-preview para 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="b3bc1-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="b3bc1-614">Cmdlet adicionado para criar a configuração de protocolo</span><span class="sxs-lookup"><span data-stu-id="b3bc1-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="b3bc1-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3bc1-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="b3bc1-616">Cmdlet adicionado para acrescentar uma nova conexão de circuito a um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="b3bc1-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b3bc1-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b3bc1-618">Cmdlet adicionado para remover uma conexão de circuito de um circuito de rota expressa existente.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="b3bc1-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b3bc1-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b3bc1-620">Cmdlet adicionado para recuperar uma conexão de circuito</span><span class="sxs-lookup"><span data-stu-id="b3bc1-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="b3bc1-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b3bc1-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b3bc1-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b3bc1-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b3bc1-623">Uso da autenticação do servidor corrigido com certificados gerados (problema 5998)</span><span class="sxs-lookup"><span data-stu-id="b3bc1-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b3bc1-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b3bc1-624">AzureRM.Sql</span></span>
* <span data-ttu-id="b3bc1-625">Cmdlets de auditoria atualizados para permitir a remoção de AuditActions ou AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="b3bc1-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="b3bc1-626">Problema corrigido com Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy ao definir uma nova política de retenção flexível onde o comando falharia com “Configurar política de retenção de longo prazo com o cofre de serviços de recuperação do azure e não há mais suporte para a política.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="b3bc1-627">Envie a solicitação com a nova política de retenção flexível”.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="b3bc1-628">Atualizar todos os cmdlets relacionados ao Banco de Dados Sql do Azure/Criação do ElasticPool/Atualização para usar a nova API do Banco de Dados, que suporta a propriedade Sku para o dimensionamento e as propriedades relacionadas à camada.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="b3bc1-629">Os cmdlets atualizados, incluindo:</span><span class="sxs-lookup"><span data-stu-id="b3bc1-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="b3bc1-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b3bc1-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b3bc1-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b3bc1-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b3bc1-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b3bc1-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b3bc1-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b3bc1-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b3bc1-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b3bc1-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b3bc1-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b3bc1-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b3bc1-636">Atualize os parâmetros para “Get-AzureRmTrafficManagerProfile” para que o parâmetro -ResourceGroupName seja requerido ao usar o parâmetro -Name.</span><span class="sxs-lookup"><span data-stu-id="b3bc1-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
