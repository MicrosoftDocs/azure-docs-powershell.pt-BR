---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: f77d901169b0d98b2425a2e50d33a1789150b770
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182546"
---
## <a name="320---december-2019"></a><span data-ttu-id="3a8fe-103">3.2.0 – Dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-103">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="3a8fe-104">Geral</span><span class="sxs-lookup"><span data-stu-id="3a8fe-104">General</span></span>
* <span data-ttu-id="3a8fe-105">Atualizar referências no .psd1 para usar o caminho relativo para todos os módulos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-105">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-106">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-107">Definir o UserAgent correto para telemetria do lado do cliente para o AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="3a8fe-107">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="3a8fe-108">Exibir mensagem de erro amigável do usuário quando o contexto é nulo no AZ 4.0 versão prévia</span><span class="sxs-lookup"><span data-stu-id="3a8fe-108">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3a8fe-109">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a8fe-109">Az.Batch</span></span>
* <span data-ttu-id="3a8fe-110">Correção do problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), no qual **New-AzBatchPool** não enviava corretamente 'VirtualMachineConfiguration.ContainerConfiguration' ou 'VirtualMachineConfiguration.DataDisks' ao servidor.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-110">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-111">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-111">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-112">Atualizar a versão do SDK do .NET do ADF para 4.5.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-112">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3a8fe-113">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-113">Az.FrontDoor</span></span>
* <span data-ttu-id="3a8fe-114">Adicionado suporte à exclusão de regras gerenciadas do WAF</span><span class="sxs-lookup"><span data-stu-id="3a8fe-114">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="3a8fe-115">Adicionado SocketAddr para preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="3a8fe-115">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3a8fe-116">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3a8fe-116">Az.HealthcareApis</span></span>
* <span data-ttu-id="3a8fe-117">Tratamento de exceção</span><span class="sxs-lookup"><span data-stu-id="3a8fe-117">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a8fe-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-118">Az.KeyVault</span></span>
* <span data-ttu-id="3a8fe-119">Corrigido erro ao acessar o valor que potencialmente não está definido</span><span class="sxs-lookup"><span data-stu-id="3a8fe-119">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="3a8fe-120">Gerenciamento de certificado de criptografia de curva elíptica</span><span class="sxs-lookup"><span data-stu-id="3a8fe-120">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="3a8fe-121">Adicionado suporte para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-121">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-122">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-122">Az.Monitor</span></span>
* <span data-ttu-id="3a8fe-123">Adicionando um argumento opcional ao comando Adicionar Configurações de Diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-123">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="3a8fe-124">Um argumento de opção que, se presente, indica que a exportação para o Log Analytics deve ser para um esquema fixo (também conhecido como</span><span class="sxs-lookup"><span data-stu-id="3a8fe-124">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="3a8fe-125">tipo de dados dedicado)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-125">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-126">Az.Network</span></span>
* <span data-ttu-id="3a8fe-127">Suporte para IpGroups no aplicativo AzureFirewall, Nat e regras de rede.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-127">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-128">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-129">Correção de um problema no qual a implantação de modelo falha ao ler um parâmetro de modelo se o nome dele entra em conflito com um nome de parâmetro interno.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-129">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="3a8fe-130">Cmdlets de política atualizados para usar a nova versão de API 2019-09-01, que introduz o suporte a agrupamento nas definições de conjunto de políticas.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-130">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-131">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-132">Criação de armazenamento atualizada na habilitação automática de Avaliação de Vulnerabilidade para StorageV2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-132">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-133">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-133">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-134">Suporte para gerar token SAS baseado em identidade de blob/contêiner com contexto de armazenamento baseado na autenticação OAuth</span><span class="sxs-lookup"><span data-stu-id="3a8fe-134">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="3a8fe-135">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3a8fe-135">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="3a8fe-136">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3a8fe-136">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="3a8fe-137">Suporte para revogar chaves de delegação de usuário da conta de armazenamento; portanto, todos os tokens SAS de identidade são revogados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-137">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="3a8fe-138">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="3a8fe-138">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="3a8fe-139">Atualize para Microsoft.Azure.Management.Storage 14.2.0, para oferecer suporte à nova API versão 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-139">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="3a8fe-140">Suporte de compartilhamento QuotaGiB mais de 5120 em cmdlets de compartilhamento de arquivo do plano de gerenciamento e adicionar o alias de parâmetro 'Quota' ao parâmetro 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-140">Support Share QuotaGiB more than 5120 in Management plane File Share cmdlets, and add parameter alias 'Quota' to parameter 'QuotaGiB'</span></span> 
    - <span data-ttu-id="3a8fe-141">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a8fe-141">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="3a8fe-142">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a8fe-142">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="3a8fe-143">Adicionar alias de parâmetro 'QuotaGiB' ao parâmetro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-143">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="3a8fe-144">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="3a8fe-144">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="3a8fe-145">Correção do problema no qual Set-AzStorageContainerAcl pode limpar a política de acesso armazenada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-145">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="3a8fe-146">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3a8fe-146">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="3a8fe-147">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-147">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a8fe-148">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="3a8fe-148">Highlights since the last major release</span></span>
* <span data-ttu-id="3a8fe-149">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-149">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="3a8fe-150">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-150">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-151">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-152">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-152">VM Reapply feature</span></span>
    - <span data-ttu-id="3a8fe-153">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-153">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="3a8fe-154">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-154">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="3a8fe-155">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-155">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="3a8fe-156">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-156">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="3a8fe-157">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-157">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="3a8fe-158">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="3a8fe-158">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="3a8fe-159">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="3a8fe-159">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="3a8fe-160">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3a8fe-160">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="3a8fe-161">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="3a8fe-161">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="3a8fe-162">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-162">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="3a8fe-163">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="3a8fe-163">Az.DataBoxEdge</span></span>
* <span data-ttu-id="3a8fe-164">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-164">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3a8fe-165">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-165">Get the Order</span></span>
* <span data-ttu-id="3a8fe-166">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-166">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3a8fe-167">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-167">Create new Order</span></span>
* <span data-ttu-id="3a8fe-168">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-168">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="3a8fe-169">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-169">Remove the Order</span></span>
* <span data-ttu-id="3a8fe-170">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="3a8fe-170">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="3a8fe-171">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="3a8fe-171">Now creates Local Share</span></span>
* <span data-ttu-id="3a8fe-172">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-172">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="3a8fe-173">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="3a8fe-173">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="3a8fe-174">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-174">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="3a8fe-175">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-175">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="3a8fe-176">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-176">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3a8fe-177">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-177">Gets the information about Triggers</span></span>
* <span data-ttu-id="3a8fe-178">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-178">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3a8fe-179">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-179">Create new Triggers</span></span>
* <span data-ttu-id="3a8fe-180">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-180">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="3a8fe-181">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-181">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-182">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-183">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-183">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="3a8fe-184">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-184">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-185">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-186">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-186">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a8fe-187">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-187">Az.EventHub</span></span>
* <span data-ttu-id="3a8fe-188">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="3a8fe-188">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3a8fe-189">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-189">Az.FrontDoor</span></span>
* <span data-ttu-id="3a8fe-190">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="3a8fe-190">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="3a8fe-191">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="3a8fe-191">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="3a8fe-192">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="3a8fe-192">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="3a8fe-193">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="3a8fe-193">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-194">Az.Network</span></span>
* <span data-ttu-id="3a8fe-195">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-195">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="3a8fe-196">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="3a8fe-196">Az.PrivateDns</span></span>
* <span data-ttu-id="3a8fe-197">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-197">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-198">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-198">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-199">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-199">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="3a8fe-200">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-200">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="3a8fe-201">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-201">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a8fe-202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a8fe-202">Az.RedisCache</span></span>
* <span data-ttu-id="3a8fe-203">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-203">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="3a8fe-204">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-204">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="3a8fe-205">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-205">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-206">Az.Resources</span></span>
- <span data-ttu-id="3a8fe-207">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-207">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="3a8fe-208">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-208">Updated create policy definition help example</span></span>
- <span data-ttu-id="3a8fe-209">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-209">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="3a8fe-210">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-210">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="3a8fe-211">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-211">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-212">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-213">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-213">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="3a8fe-214">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="3a8fe-214">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="3a8fe-215">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-215">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="3a8fe-216">Geral</span><span class="sxs-lookup"><span data-stu-id="3a8fe-216">General</span></span>
* <span data-ttu-id="3a8fe-217">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-217">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-218">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-218">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-219">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-219">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3a8fe-220">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-220">Az.Advisor</span></span>
* <span data-ttu-id="3a8fe-221">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-221">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3a8fe-222">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a8fe-222">Az.Batch</span></span>
* <span data-ttu-id="3a8fe-223">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-223">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="3a8fe-224">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-224">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="3a8fe-225">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-225">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="3a8fe-226">O parâmetro `-ResourceFile` do **New-AzBatchTask** agora usa uma coleção de objetos do `PSResourceFile` que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-226">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="3a8fe-227">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-227">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="3a8fe-228">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-228">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="3a8fe-229">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-229">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="3a8fe-230">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-230">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="3a8fe-231">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-231">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="3a8fe-232">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-232">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="3a8fe-233">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-233">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="3a8fe-234">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-234">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="3a8fe-235">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-235">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="3a8fe-236">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-236">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="3a8fe-237">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-237">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="3a8fe-238">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-238">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="3a8fe-239">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-239">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="3a8fe-240">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-240">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="3a8fe-241">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-241">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="3a8fe-242">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-242">This operation is no longer supported.</span></span>
* <span data-ttu-id="3a8fe-243">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-243">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="3a8fe-244">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-244">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="3a8fe-245">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-245">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="3a8fe-246">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-246">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="3a8fe-247">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-247">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="3a8fe-248">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-248">New non-verified images are also now returned.</span></span> <span data-ttu-id="3a8fe-249">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-249">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="3a8fe-250">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-250">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="3a8fe-251">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-251">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="3a8fe-252">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-252">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="3a8fe-253">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-253">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="3a8fe-254">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-254">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="3a8fe-255">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-255">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="3a8fe-256">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-256">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="3a8fe-257">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-257">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="3a8fe-258">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-258">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a8fe-259">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a8fe-259">Az.Cdn</span></span>
* <span data-ttu-id="3a8fe-260">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-260">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="3a8fe-261">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-261">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-262">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-263">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="3a8fe-263">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="3a8fe-264">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-264">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="3a8fe-265">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-265">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="3a8fe-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3a8fe-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="3a8fe-267">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-267">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3a8fe-268">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-268">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="3a8fe-269">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="3a8fe-269">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="3a8fe-270">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-270">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="3a8fe-271">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="3a8fe-271">Breaking changes</span></span>
    - <span data-ttu-id="3a8fe-272">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-272">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="3a8fe-273">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3a8fe-273">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-274">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-274">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-275">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-275">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-276">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-277">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="3a8fe-277">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="3a8fe-278">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-278">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="3a8fe-279">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="3a8fe-279">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="3a8fe-280">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="3a8fe-280">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="3a8fe-281">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-281">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="3a8fe-282">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="3a8fe-282">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3a8fe-283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-283">Az.FrontDoor</span></span>
* <span data-ttu-id="3a8fe-284">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-284">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3a8fe-285">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a8fe-285">Az.HDInsight</span></span>
* <span data-ttu-id="3a8fe-286">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-286">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="3a8fe-287">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-287">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="3a8fe-288">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-288">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="3a8fe-289">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-289">Removed five cmdlets:</span></span>
    - <span data-ttu-id="3a8fe-290">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3a8fe-290">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3a8fe-291">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3a8fe-291">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3a8fe-292">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3a8fe-292">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="3a8fe-293">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3a8fe-293">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="3a8fe-294">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3a8fe-294">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="3a8fe-295">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-295">Added three cmdlets:</span></span>
    - <span data-ttu-id="3a8fe-296">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-296">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="3a8fe-297">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-297">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="3a8fe-298">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-298">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="3a8fe-299">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-299">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="3a8fe-300">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-300">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="3a8fe-301">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-301">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="3a8fe-302">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-302">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="3a8fe-303">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-303">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="3a8fe-304">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-304">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="3a8fe-305">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-305">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="3a8fe-306">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-306">Added some scenario test cases.</span></span>
* <span data-ttu-id="3a8fe-307">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-307">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a8fe-308">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-308">Az.IotHub</span></span>
* <span data-ttu-id="3a8fe-309">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-309">Breaking changes:</span></span>
    - <span data-ttu-id="3a8fe-310">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-310">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3a8fe-311">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-311">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3a8fe-312">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-312">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3a8fe-313">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-313">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3a8fe-314">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-314">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="3a8fe-315">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-315">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="3a8fe-316">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-316">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="3a8fe-317">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-317">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="3a8fe-318">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-318">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3a8fe-319">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-319">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="3a8fe-320">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-320">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="3a8fe-321">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-321">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-322">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-323">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-323">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="3a8fe-324">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-324">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="3a8fe-325">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-325">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="3a8fe-326">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-326">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="3a8fe-327">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-327">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="3a8fe-328">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-328">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="3a8fe-329">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-329">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="3a8fe-330">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-330">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="3a8fe-331">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="3a8fe-331">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-332">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-332">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-333">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-333">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-334">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-334">Az.Network</span></span>
* <span data-ttu-id="3a8fe-335">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-335">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="3a8fe-336">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-336">Updated cmdlet:</span></span>
        - <span data-ttu-id="3a8fe-337">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-337">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-338">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-338">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-339">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-339">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-340">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-340">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-341">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-341">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3a8fe-342">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-342">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="3a8fe-343">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-343">New cmdlet:</span></span>
        - <span data-ttu-id="3a8fe-344">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="3a8fe-344">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="3a8fe-345">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-345">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="3a8fe-346">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-346">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="3a8fe-347">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-347">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="3a8fe-348">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-348">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="3a8fe-349">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-349">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="3a8fe-350">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-350">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="3a8fe-351">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-351">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="3a8fe-352">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-352">New cmdlets added:</span></span>
        - <span data-ttu-id="3a8fe-353">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-353">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="3a8fe-354">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-354">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3a8fe-355">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-355">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3a8fe-356">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-356">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="3a8fe-357">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-357">Set-AzVirtualHub</span></span>
* <span data-ttu-id="3a8fe-358">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="3a8fe-358">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="3a8fe-359">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-359">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3a8fe-360">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-360">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="3a8fe-361">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-361">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="3a8fe-362">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-362">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="3a8fe-363">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-363">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="3a8fe-364">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-364">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="3a8fe-365">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-365">New cmdlets added:</span></span>
        - <span data-ttu-id="3a8fe-366">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-366">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="3a8fe-367">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-367">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3a8fe-368">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-368">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3a8fe-369">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-369">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3a8fe-370">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-370">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3a8fe-371">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-371">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="3a8fe-372">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-372">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="3a8fe-373">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="3a8fe-373">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="3a8fe-374">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-374">New cmdlets added:</span></span>
        - <span data-ttu-id="3a8fe-375">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="3a8fe-375">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="3a8fe-376">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="3a8fe-376">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="3a8fe-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="3a8fe-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="3a8fe-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="3a8fe-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="3a8fe-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="3a8fe-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="3a8fe-381">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3a8fe-382">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-382">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="3a8fe-383">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-383">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="3a8fe-384">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="3a8fe-384">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="3a8fe-385">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="3a8fe-385">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="3a8fe-386">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="3a8fe-387">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-387">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="3a8fe-388">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-388">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="3a8fe-389">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-389">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="3a8fe-390">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-390">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="3a8fe-391">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-391">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="3a8fe-392">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-392">New cmdlets added:</span></span>
        - <span data-ttu-id="3a8fe-393">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-393">New-AzIpGroup</span></span>
        - <span data-ttu-id="3a8fe-394">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-394">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="3a8fe-395">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-395">Get-AzIpGroup</span></span>
        - <span data-ttu-id="3a8fe-396">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-396">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-397">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-398">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-398">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-399">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-399">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-400">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-400">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="3a8fe-401">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-401">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="3a8fe-402">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-402">Removed deprecated aliases:</span></span>
* <span data-ttu-id="3a8fe-403">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-403">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="3a8fe-404">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-404">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="3a8fe-405">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-405">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3a8fe-406">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-406">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="3a8fe-407">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="3a8fe-407">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="3a8fe-408">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-408">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-409">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-409">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-410">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a8fe-410">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="3a8fe-411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-411">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3a8fe-412">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-412">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3a8fe-413">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="3a8fe-413">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="3a8fe-414">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3a8fe-414">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="3a8fe-415">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3a8fe-415">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="3a8fe-416">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-416">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="3a8fe-417">Geral</span><span class="sxs-lookup"><span data-stu-id="3a8fe-417">General</span></span>
* <span data-ttu-id="3a8fe-418">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-418">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-419">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-420">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-420">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3a8fe-421">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-421">Az.ApiManagement</span></span>
* <span data-ttu-id="3a8fe-422">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-422">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="3a8fe-423">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="3a8fe-423">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-424">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-424">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-425">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-425">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="3a8fe-426">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a8fe-426">Az.Batch</span></span>
* <span data-ttu-id="3a8fe-427">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-427">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-428">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-429">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-429">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="3a8fe-430">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3a8fe-430">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="3a8fe-431">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-431">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="3a8fe-432">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-432">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-433">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-433">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-434">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-434">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="3a8fe-435">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-435">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="3a8fe-436">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-436">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-437">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-437">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-438">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="3a8fe-438">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="3a8fe-439">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="3a8fe-439">Az.HealthcareApis</span></span>
* <span data-ttu-id="3a8fe-440">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-440">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="3a8fe-441">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-441">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="3a8fe-442">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="3a8fe-442">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="3a8fe-443">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-443">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a8fe-444">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-444">Az.IotHub</span></span>
* <span data-ttu-id="3a8fe-445">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="3a8fe-445">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="3a8fe-446">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a8fe-446">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-447">Az.Monitor</span></span>
* <span data-ttu-id="3a8fe-448">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="3a8fe-448">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="3a8fe-449">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-449">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="3a8fe-450">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="3a8fe-450">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="3a8fe-451">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-451">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-452">Az.Network</span></span>
* <span data-ttu-id="3a8fe-453">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-453">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="3a8fe-454">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="3a8fe-454">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="3a8fe-455">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-455">New cmdlets added:</span></span>
        - <span data-ttu-id="3a8fe-456">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-456">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="3a8fe-457">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-457">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3a8fe-458">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="3a8fe-458">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="3a8fe-459">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-459">Updated cmdlets:</span></span>
        - <span data-ttu-id="3a8fe-460">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-460">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a8fe-461">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-461">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a8fe-462">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-462">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3a8fe-463">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="3a8fe-463">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="3a8fe-464">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="3a8fe-464">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="3a8fe-465">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-465">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="3a8fe-466">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-466">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a8fe-467">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a8fe-467">Az.RedisCache</span></span>
* <span data-ttu-id="3a8fe-468">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-468">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-469">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-470">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-470">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-471">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-472">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-472">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="3a8fe-473">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="3a8fe-473">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3a8fe-474">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a8fe-474">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="3a8fe-475">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="3a8fe-475">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="3a8fe-476">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-476">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3a8fe-477">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3a8fe-477">Az.StorageSync</span></span>
* <span data-ttu-id="3a8fe-478">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-478">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-479">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-479">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-480">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="3a8fe-480">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="3a8fe-481">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-481">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3a8fe-482">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-482">Az.ApiManagement</span></span>
* <span data-ttu-id="3a8fe-483">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-483">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="3a8fe-484">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-484">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="3a8fe-485">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-485">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-486">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-486">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-487">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-487">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="3a8fe-488">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="3a8fe-488">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="3a8fe-489">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-489">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-490">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-491">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-491">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="3a8fe-492">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-492">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3a8fe-493">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-493">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="3a8fe-494">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-494">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="3a8fe-495">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-495">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="3a8fe-496">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-496">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="3a8fe-497">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-497">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="3a8fe-498">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-498">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="3a8fe-499">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-499">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-500">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-501">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-501">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="3a8fe-502">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="3a8fe-502">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="3a8fe-503">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a8fe-503">Az.HDInsight</span></span>
* <span data-ttu-id="3a8fe-504">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="3a8fe-504">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a8fe-505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-505">Az.IotHub</span></span>
* <span data-ttu-id="3a8fe-506">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-506">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="3a8fe-507">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-507">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="3a8fe-508">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-508">New cmdlets are:</span></span>
    - <span data-ttu-id="3a8fe-509">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a8fe-509">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3a8fe-510">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a8fe-510">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3a8fe-511">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a8fe-511">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="3a8fe-512">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="3a8fe-512">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-513">Az.Monitor</span></span>
* <span data-ttu-id="3a8fe-514">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="3a8fe-514">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="3a8fe-515">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-515">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="3a8fe-516">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-516">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="3a8fe-517">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-517">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="3a8fe-518">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-518">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="3a8fe-519">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-519">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="3a8fe-520">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-520">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="3a8fe-521">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-521">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="3a8fe-522">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-522">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3a8fe-523">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-523">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="3a8fe-524">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-524">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="3a8fe-525">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-525">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="3a8fe-526">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-526">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="3a8fe-527">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="3a8fe-527">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="3a8fe-528">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="3a8fe-528">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="3a8fe-529">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-529">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="3a8fe-530">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-530">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="3a8fe-531">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="3a8fe-531">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="3a8fe-532">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-532">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="3a8fe-533">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="3a8fe-533">Overall improved help files</span></span>
* <span data-ttu-id="3a8fe-534">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-534">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-535">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-535">Az.Network</span></span>
* <span data-ttu-id="3a8fe-536">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-536">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="3a8fe-537">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="3a8fe-537">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="3a8fe-538">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="3a8fe-538">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="3a8fe-539">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-539">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="3a8fe-540">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="3a8fe-540">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="3a8fe-541">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="3a8fe-541">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="3a8fe-542">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-542">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="3a8fe-543">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3a8fe-543">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="3a8fe-544">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-544">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="3a8fe-545">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-545">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="3a8fe-546">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-546">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="3a8fe-547">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="3a8fe-547">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="3a8fe-548">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a8fe-548">New cmdlets</span></span>
        - <span data-ttu-id="3a8fe-549">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="3a8fe-549">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="3a8fe-550">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-550">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="3a8fe-551">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-551">Updated cmdlet:</span></span>
        - <span data-ttu-id="3a8fe-552">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3a8fe-552">New-VpnSite</span></span>
        - <span data-ttu-id="3a8fe-553">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="3a8fe-553">Update-VpnSite</span></span>
        - <span data-ttu-id="3a8fe-554">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-554">New-VpnConnection</span></span>
        - <span data-ttu-id="3a8fe-555">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-555">Update-VpnConnection</span></span>
* <span data-ttu-id="3a8fe-556">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-556">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-557">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-558">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-558">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="3a8fe-559">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="3a8fe-559">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-560">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-560">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-561">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-561">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-562">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-562">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-563">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-563">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="3a8fe-564">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-564">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="3a8fe-565">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a8fe-565">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a8fe-566">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3a8fe-566">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3a8fe-567">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3a8fe-567">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3a8fe-568">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-568">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="3a8fe-569">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a8fe-569">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a8fe-570">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a8fe-570">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a8fe-571">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3a8fe-571">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3a8fe-572">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3a8fe-572">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3a8fe-573">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-573">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="3a8fe-574">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3a8fe-574">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="3a8fe-575">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3a8fe-575">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="3a8fe-576">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3a8fe-576">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="3a8fe-577">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="3a8fe-577">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="3a8fe-578">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-578">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a8fe-579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a8fe-579">Az.SignalR</span></span>
* <span data-ttu-id="3a8fe-580">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-580">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-581">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-582">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-582">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="3a8fe-583">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-583">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="3a8fe-584">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-584">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="3a8fe-585">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-585">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="3a8fe-586">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-586">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-587">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-587">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-588">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-588">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="3a8fe-589">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="3a8fe-589">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="3a8fe-590">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-590">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="3a8fe-591">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-591">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="3a8fe-592">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-592">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="3a8fe-593">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-593">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="3a8fe-594">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3a8fe-594">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="3a8fe-595">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a8fe-595">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3a8fe-596">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a8fe-596">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3a8fe-597">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a8fe-597">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="3a8fe-598">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3a8fe-598">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-599">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-600">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="3a8fe-600">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="3a8fe-601">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="3a8fe-601">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="3a8fe-602">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-602">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="3a8fe-603">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-603">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="3a8fe-604">Geral</span><span class="sxs-lookup"><span data-stu-id="3a8fe-604">General</span></span>
* <span data-ttu-id="3a8fe-605">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-605">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-606">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-606">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-607">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-607">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="3a8fe-608">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3a8fe-608">Az.Aks</span></span>
* <span data-ttu-id="3a8fe-609">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-609">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="3a8fe-610">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="3a8fe-610">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3a8fe-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-611">Az.ApiManagement</span></span>
* <span data-ttu-id="3a8fe-612">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="3a8fe-612">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="3a8fe-613">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="3a8fe-613">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="3a8fe-614">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-614">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="3a8fe-615">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="3a8fe-615">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="3a8fe-616">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-616">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3a8fe-617">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a8fe-617">Az.Batch</span></span>
* <span data-ttu-id="3a8fe-618">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="3a8fe-618">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a8fe-619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a8fe-619">Az.Cdn</span></span>
* <span data-ttu-id="3a8fe-620">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="3a8fe-620">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-621">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-622">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-622">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="3a8fe-623">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-623">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="3a8fe-624">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-624">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="3a8fe-625">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-625">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="3a8fe-626">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="3a8fe-626">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="3a8fe-627">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-627">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="3a8fe-628">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="3a8fe-628">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="3a8fe-629">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-629">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-630">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-630">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-631">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-631">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="3a8fe-632">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="3a8fe-632">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="3a8fe-633">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="3a8fe-633">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="3a8fe-634">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="3a8fe-634">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-635">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-635">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-636">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-636">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a8fe-637">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-637">Az.EventHub</span></span>
* <span data-ttu-id="3a8fe-638">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-638">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="3a8fe-639">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="3a8fe-639">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="3a8fe-640">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="3a8fe-640">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="3a8fe-641">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="3a8fe-641">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="3a8fe-642">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3a8fe-642">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3a8fe-643">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-643">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-644">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-644">Az.Monitor</span></span>
* <span data-ttu-id="3a8fe-645">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="3a8fe-645">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-646">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-646">Az.Network</span></span>
* <span data-ttu-id="3a8fe-647">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-647">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="3a8fe-648">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-648">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="3a8fe-649">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-649">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="3a8fe-650">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="3a8fe-650">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="3a8fe-651">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-651">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="3a8fe-652">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-652">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="3a8fe-653">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="3a8fe-653">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a8fe-654">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-654">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a8fe-655">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-655">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="3a8fe-656">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-656">Added example</span></span>
    - <span data-ttu-id="3a8fe-657">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-657">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="3a8fe-658">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="3a8fe-658">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="3a8fe-659">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="3a8fe-659">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-660">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-661">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-661">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-662">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-663">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="3a8fe-663">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="3a8fe-664">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="3a8fe-664">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="3a8fe-665">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-665">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="3a8fe-666">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="3a8fe-666">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a8fe-667">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-667">Az.ServiceBus</span></span>
* <span data-ttu-id="3a8fe-668">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-668">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="3a8fe-669">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="3a8fe-669">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="3a8fe-670">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="3a8fe-670">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-671">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-671">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-672">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-672">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="3a8fe-673">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-673">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="3a8fe-674">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="3a8fe-674">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="3a8fe-675">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-675">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="3a8fe-676">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="3a8fe-676">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="3a8fe-677">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a8fe-677">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-678">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-679">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-679">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-680">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-681">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a8fe-681">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="3a8fe-682">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="3a8fe-682">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="3a8fe-683">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-683">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="3a8fe-684">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-684">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="3a8fe-685">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="3a8fe-685">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="3a8fe-686">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-686">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-687">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-688">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a8fe-688">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="3a8fe-689">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-689">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-690">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-690">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-691">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3a8fe-691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="3a8fe-692">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-692">Az.ApplicationInsights</span></span>
* <span data-ttu-id="3a8fe-693">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-693">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-694">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-695">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-695">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a8fe-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a8fe-697">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-697">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-698">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-699">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-699">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3a8fe-700">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3a8fe-700">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3a8fe-701">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="3a8fe-701">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="3a8fe-702">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="3a8fe-702">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-703">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-704">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-704">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="3a8fe-705">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="3a8fe-705">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a8fe-706">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-706">Az.EventHub</span></span>
* <span data-ttu-id="3a8fe-707">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3a8fe-707">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3a8fe-708">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="3a8fe-708">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a8fe-709">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-709">Az.KeyVault</span></span>
* <span data-ttu-id="3a8fe-710">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-710">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a8fe-711">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a8fe-711">Az.LogicApp</span></span>
* <span data-ttu-id="3a8fe-712">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="3a8fe-712">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="3a8fe-713">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-713">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="3a8fe-714">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-714">Az.ManagedServices</span></span>
* <span data-ttu-id="3a8fe-715">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-715">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-716">Az.Network</span></span>
* <span data-ttu-id="3a8fe-717">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-717">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="3a8fe-718">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a8fe-718">New cmdlets</span></span>
        - <span data-ttu-id="3a8fe-719">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a8fe-719">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a8fe-720">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-720">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3a8fe-721">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-721">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-722">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-722">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-723">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-723">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-724">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-724">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="3a8fe-725">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="3a8fe-725">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="3a8fe-726">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-726">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="3a8fe-727">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="3a8fe-727">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="3a8fe-728">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-728">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="3a8fe-729">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-729">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="3a8fe-730">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-730">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="3a8fe-731">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="3a8fe-731">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="3a8fe-732">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="3a8fe-732">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="3a8fe-733">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-733">Updated cmdlets</span></span>
        - <span data-ttu-id="3a8fe-734">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-734">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a8fe-735">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-735">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="3a8fe-736">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-736">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="3a8fe-737">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-737">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="3a8fe-738">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-738">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="3a8fe-739">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-739">Updated cmdlet:</span></span>
        - <span data-ttu-id="3a8fe-740">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-740">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3a8fe-741">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-741">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="3a8fe-742">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-742">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="3a8fe-743">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="3a8fe-743">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="3a8fe-744">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-744">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="3a8fe-745">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-745">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a8fe-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a8fe-747">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-747">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="3a8fe-748">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="3a8fe-748">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-749">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-749">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-750">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-750">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3a8fe-751">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-751">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="3a8fe-752">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-752">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="3a8fe-753">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-753">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="3a8fe-754">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-754">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="3a8fe-755">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-755">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3a8fe-756">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-756">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="3a8fe-757">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-757">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="3a8fe-758">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-758">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="3a8fe-759">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-759">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-760">Az.Resources</span></span>
- <span data-ttu-id="3a8fe-761">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-761">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="3a8fe-762">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="3a8fe-762">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a8fe-763">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-763">Az.ServiceBus</span></span>
* <span data-ttu-id="3a8fe-764">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="3a8fe-764">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="3a8fe-765">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="3a8fe-765">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-766">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-766">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-767">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3a8fe-767">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="3a8fe-768">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="3a8fe-768">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="3a8fe-769">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-769">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-770">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-770">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-771">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="3a8fe-771">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3a8fe-772">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3a8fe-772">Az.StorageSync</span></span>
* <span data-ttu-id="3a8fe-773">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-773">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="3a8fe-774">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="3a8fe-774">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-775">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-775">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-776">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fe-776">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="3a8fe-777">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fe-777">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="3a8fe-778">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="3a8fe-778">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="3a8fe-779">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-779">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-780">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-780">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-781">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="3a8fe-781">Add support for profile cmdlets</span></span>
* <span data-ttu-id="3a8fe-782">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-782">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="3a8fe-783">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3a8fe-783">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="3a8fe-784">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-784">Az.Advisor</span></span>
* <span data-ttu-id="3a8fe-785">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-785">GA release of Az.Advisor</span></span>
* <span data-ttu-id="3a8fe-786">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-786">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="3a8fe-787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-787">Az.ApiManagement</span></span>
* <span data-ttu-id="3a8fe-788">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="3a8fe-788">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="3a8fe-789">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-789">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="3a8fe-790">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="3a8fe-790">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="3a8fe-791">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-791">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="3a8fe-792">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="3a8fe-792">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="3a8fe-793">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-793">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="3a8fe-794">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="3a8fe-794">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-795">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-795">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-796">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-796">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-797">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-798">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-798">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-799">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-800">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-800">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a8fe-801">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a8fe-801">Az.EventGrid</span></span>
* <span data-ttu-id="3a8fe-802">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-802">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a8fe-803">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-803">Az.IotHub</span></span>
* <span data-ttu-id="3a8fe-804">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-804">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-805">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-805">Az.Network</span></span>
* <span data-ttu-id="3a8fe-806">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="3a8fe-806">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="3a8fe-807">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-807">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a8fe-808">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-808">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a8fe-809">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="3a8fe-809">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="3a8fe-810">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="3a8fe-810">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a8fe-811">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-811">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a8fe-812">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="3a8fe-812">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-813">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-814">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="3a8fe-814">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-815">Az.Resources</span></span>
    - <span data-ttu-id="3a8fe-816">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="3a8fe-816">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="3a8fe-817">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="3a8fe-817">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="3a8fe-818">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="3a8fe-818">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="3a8fe-819">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-819">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a8fe-820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-820">Az.ServiceBus</span></span>
* <span data-ttu-id="3a8fe-821">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-821">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-822">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-823">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="3a8fe-823">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="3a8fe-824">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-824">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="3a8fe-825">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3a8fe-825">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3a8fe-826">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3a8fe-826">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3a8fe-827">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="3a8fe-827">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="3a8fe-828">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3a8fe-828">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3a8fe-829">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3a8fe-829">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="3a8fe-830">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="3a8fe-830">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="3a8fe-831">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="3a8fe-831">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-832">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-833">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-833">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="3a8fe-834">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a8fe-834">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="3a8fe-835">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-835">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="3a8fe-836">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="3a8fe-836">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="3a8fe-837">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-837">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="3a8fe-838">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-838">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="3a8fe-839">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-839">Set-AzStorageAccount</span></span>
* <span data-ttu-id="3a8fe-840">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-840">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="3a8fe-841">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3a8fe-841">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="3a8fe-842">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="3a8fe-842">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="3a8fe-843">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="3a8fe-843">Az.StorageSync</span></span>
* <span data-ttu-id="3a8fe-844">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-844">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="3a8fe-845">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-845">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-846">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-846">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-847">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="3a8fe-847">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="3a8fe-848">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="3a8fe-848">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="3a8fe-849">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="3a8fe-849">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="3a8fe-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3a8fe-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="3a8fe-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="3a8fe-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-852">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-852">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-853">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-853">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="3a8fe-854">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-854">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="3a8fe-855">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3a8fe-855">Az.Dns</span></span>
* <span data-ttu-id="3a8fe-856">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-856">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a8fe-857">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a8fe-857">Az.EventGrid</span></span>
* <span data-ttu-id="3a8fe-858">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-858">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="3a8fe-859">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-859">New cmdlets:</span></span>
    - <span data-ttu-id="3a8fe-860">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3a8fe-860">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3a8fe-861">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-861">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3a8fe-862">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3a8fe-862">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3a8fe-863">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-863">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="3a8fe-864">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="3a8fe-864">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="3a8fe-865">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-865">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3a8fe-866">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3a8fe-866">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3a8fe-867">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-867">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="3a8fe-868">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="3a8fe-868">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="3a8fe-869">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-869">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="3a8fe-870">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-870">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3a8fe-871">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-871">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="3a8fe-872">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="3a8fe-872">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="3a8fe-873">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="3a8fe-873">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="3a8fe-874">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-874">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="3a8fe-875">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-875">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="3a8fe-876">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-876">Updated cmdlets:</span></span>
    - <span data-ttu-id="3a8fe-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="3a8fe-878">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-878">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3a8fe-879">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-879">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="3a8fe-880">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-880">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="3a8fe-881">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-881">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="3a8fe-882">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="3a8fe-882">Event subscription expiration date,</span></span>
            - <span data-ttu-id="3a8fe-883">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-883">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="3a8fe-884">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-884">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="3a8fe-885">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="3a8fe-885">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="3a8fe-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="3a8fe-887">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-887">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="3a8fe-888">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3a8fe-888">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="3a8fe-889">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-889">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="3a8fe-890">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-890">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3a8fe-891">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-891">Az.FrontDoor</span></span>
* <span data-ttu-id="3a8fe-892">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="3a8fe-892">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="3a8fe-893">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-893">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="3a8fe-894">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="3a8fe-894">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="3a8fe-895">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="3a8fe-895">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-896">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-896">Az.Network</span></span>
* <span data-ttu-id="3a8fe-897">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="3a8fe-897">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="3a8fe-898">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a8fe-898">New cmdlets</span></span>
        - <span data-ttu-id="3a8fe-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="3a8fe-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="3a8fe-900">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="3a8fe-900">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="3a8fe-901">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a8fe-901">New cmdlets</span></span> 
        - <span data-ttu-id="3a8fe-902">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="3a8fe-902">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="3a8fe-903">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-903">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="3a8fe-904">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a8fe-904">New cmdlets</span></span> 
        - <span data-ttu-id="3a8fe-905">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-905">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="3a8fe-906">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-906">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3a8fe-907">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-907">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="3a8fe-908">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-908">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="3a8fe-909">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-909">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="3a8fe-910">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a8fe-910">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="3a8fe-911">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a8fe-911">New cmdlets</span></span>
        - <span data-ttu-id="3a8fe-912">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a8fe-912">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a8fe-913">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a8fe-913">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a8fe-914">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a8fe-914">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="3a8fe-915">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-915">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="3a8fe-916">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-916">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="3a8fe-917">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-917">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="3a8fe-918">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-918">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="3a8fe-919">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-919">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="3a8fe-920">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-920">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="3a8fe-921">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a8fe-921">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="3a8fe-922">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-922">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="3a8fe-923">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-923">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="3a8fe-924">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-924">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="3a8fe-925">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-925">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="3a8fe-926">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="3a8fe-926">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="3a8fe-927">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="3a8fe-927">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="3a8fe-928">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="3a8fe-928">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="3a8fe-929">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-929">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="3a8fe-930">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-930">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="3a8fe-931">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="3a8fe-931">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="3a8fe-932">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="3a8fe-932">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="3a8fe-933">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-933">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="3a8fe-934">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3a8fe-934">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="3a8fe-935">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-935">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="3a8fe-936">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-936">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3a8fe-937">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-937">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="3a8fe-938">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-938">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a8fe-939">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-939">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a8fe-940">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-940">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-941">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-942">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-942">Support for additional Template Export options</span></span>
    - <span data-ttu-id="3a8fe-943">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-943">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3a8fe-944">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-944">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="3a8fe-945">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-945">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-946">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-947">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-947">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-948">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-948">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-949">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="3a8fe-949">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="3a8fe-950">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="3a8fe-950">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="3a8fe-951">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-951">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="3a8fe-952">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a8fe-952">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3a8fe-953">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a8fe-953">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3a8fe-954">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3a8fe-954">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="3a8fe-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3a8fe-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="3a8fe-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="3a8fe-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-957">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-957">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-958">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a8fe-958">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="3a8fe-959">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-959">New-AzStorageAccount</span></span>
* <span data-ttu-id="3a8fe-960">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="3a8fe-960">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="3a8fe-961">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-961">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-962">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-962">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-963">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="3a8fe-963">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="3a8fe-964">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="3a8fe-964">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="3a8fe-965">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-965">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="3a8fe-966">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a8fe-966">Az.Cdn</span></span>
* <span data-ttu-id="3a8fe-967">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-967">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-968">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-969">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-969">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="3a8fe-970">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-970">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a8fe-971">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-971">Az.EventHub</span></span>
* <span data-ttu-id="3a8fe-972">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-972">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="3a8fe-973">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8fe-973">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-974">Az.Network</span></span>
* <span data-ttu-id="3a8fe-975">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="3a8fe-975">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="3a8fe-976">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="3a8fe-976">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a8fe-977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-977">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a8fe-978">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-978">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-980">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="3a8fe-980">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a8fe-981">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-981">Az.ServiceBus</span></span>
* <span data-ttu-id="3a8fe-982">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8fe-982">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-983">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-984">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-984">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="3a8fe-985">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-985">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-986">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-987">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-987">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="3a8fe-988">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-988">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="3a8fe-989">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="3a8fe-989">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="3a8fe-990">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-990">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-991">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-991">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-992">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-992">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="3a8fe-993">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-993">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="3a8fe-994">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-994">Az.ApiManagement</span></span>
* <span data-ttu-id="3a8fe-995">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-995">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="3a8fe-996">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-996">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="3a8fe-997">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-997">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="3a8fe-998">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-998">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="3a8fe-999">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-999">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="3a8fe-1000">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1000">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="3a8fe-1001">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1001">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="3a8fe-1002">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1002">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="3a8fe-1003">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1003">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="3a8fe-1004">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1004">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="3a8fe-1005">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1005">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="3a8fe-1006">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1006">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="3a8fe-1007">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1007">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="3a8fe-1008">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1008">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="3a8fe-1009">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1009">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="3a8fe-1010">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1010">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="3a8fe-1011">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1011">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="3a8fe-1012">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1012">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="3a8fe-1013">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1013">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="3a8fe-1014">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1014">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="3a8fe-1015">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1015">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="3a8fe-1016">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1016">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="3a8fe-1017">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1017">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="3a8fe-1018">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1018">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="3a8fe-1019">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1019">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="3a8fe-1020">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1020">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="3a8fe-1021">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1021">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="3a8fe-1022">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1022">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="3a8fe-1023">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1023">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="3a8fe-1024">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1024">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="3a8fe-1025">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1025">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="3a8fe-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="3a8fe-1027">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1027">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="3a8fe-1028">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1028">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3a8fe-1029">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1029">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="3a8fe-1030">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1030">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="3a8fe-1031">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1031">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="3a8fe-1032">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1032">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="3a8fe-1033">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1033">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="3a8fe-1034">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1034">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="3a8fe-1035">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1035">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3a8fe-1036">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1036">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="3a8fe-1037">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1037">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="3a8fe-1038">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1038">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3a8fe-1039">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1039">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="3a8fe-1040">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1040">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="3a8fe-1041">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1041">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="3a8fe-1042">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1042">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="3a8fe-1043">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1043">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="3a8fe-1044">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1044">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="3a8fe-1045">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1045">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="3a8fe-1046">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1046">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="3a8fe-1047">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1047">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="3a8fe-1048">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1048">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="3a8fe-1049">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1049">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="3a8fe-1050">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1050">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="3a8fe-1051">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1051">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3a8fe-1052">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1052">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3a8fe-1053">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1053">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3a8fe-1054">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1054">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3a8fe-1055">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1055">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="3a8fe-1056">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1056">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="3a8fe-1057">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1057">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="3a8fe-1058">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1058">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="3a8fe-1059">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1059">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="3a8fe-1060">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1060">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="3a8fe-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="3a8fe-1062">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1062">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="3a8fe-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="3a8fe-1064">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1064">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="3a8fe-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="3a8fe-1066">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1066">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="3a8fe-1067">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1067">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="3a8fe-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="3a8fe-1069">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1069">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="3a8fe-1070">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1070">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="3a8fe-1071">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1071">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-1072">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1072">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1073">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1073">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="3a8fe-1074">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1074">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="3a8fe-1075">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1075">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="3a8fe-1076">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1076">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="3a8fe-1077">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1077">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="3a8fe-1078">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1078">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="3a8fe-1079">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1079">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1080">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1081">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1081">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="3a8fe-1082">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1082">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1083">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-1084">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1084">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1085">Az.Monitor</span></span>
* <span data-ttu-id="3a8fe-1086">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1086">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1087">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1088">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1088">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="3a8fe-1089">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1089">Updated cmdlet:</span></span>
        - <span data-ttu-id="3a8fe-1090">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1090">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="3a8fe-1091">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1091">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1092">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1093">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1093">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1094">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1095">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1095">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="3a8fe-1096">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1096">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1097">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1097">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1098">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1098">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a8fe-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a8fe-1100">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1100">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="3a8fe-1101">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1101">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1102">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1103">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1103">Proximity placement group feature.</span></span>
    - <span data-ttu-id="3a8fe-1104">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1104">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="3a8fe-1105">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1105">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="3a8fe-1106">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1106">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="3a8fe-1107">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1107">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="3a8fe-1108">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1108">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="3a8fe-1109">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1109">Breaking changes</span></span>
    - <span data-ttu-id="3a8fe-1110">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1110">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="3a8fe-1111">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1111">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="3a8fe-1112">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1112">Az.DeploymentManager</span></span>
* <span data-ttu-id="3a8fe-1113">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1113">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="3a8fe-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1114">Az.Dns</span></span>
* <span data-ttu-id="3a8fe-1115">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1115">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="3a8fe-1116">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1116">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="3a8fe-1117">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1117">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="3a8fe-1118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1118">Az.FrontDoor</span></span>
* <span data-ttu-id="3a8fe-1119">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1119">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="3a8fe-1120">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1120">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="3a8fe-1121">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1121">Az.HDInsight</span></span>
* <span data-ttu-id="3a8fe-1122">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1122">Removed two cmdlets:</span></span>
    - <span data-ttu-id="3a8fe-1123">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1123">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="3a8fe-1124">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1124">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3a8fe-1125">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1125">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="3a8fe-1126">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1126">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="3a8fe-1127">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1127">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="3a8fe-1128">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1128">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-1129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1129">Az.Monitor</span></span>
* <span data-ttu-id="3a8fe-1130">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1130">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="3a8fe-1131">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1131">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="3a8fe-1132">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1132">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="3a8fe-1133">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1133">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="3a8fe-1134">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1134">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="3a8fe-1135">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1135">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="3a8fe-1136">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1136">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="3a8fe-1137">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1137">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a8fe-1138">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1138">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a8fe-1139">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1139">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a8fe-1140">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1140">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a8fe-1141">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1141">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="3a8fe-1142">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1142">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="3a8fe-1143">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1143">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1144">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1145">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1145">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="3a8fe-1146">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1146">New cmdlets</span></span>
        - <span data-ttu-id="3a8fe-1147">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1147">New-AzNatGateway</span></span>
        - <span data-ttu-id="3a8fe-1148">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1148">Get-AzNatGateway</span></span>
        - <span data-ttu-id="3a8fe-1149">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1149">Set-AzNatGateway</span></span>
        - <span data-ttu-id="3a8fe-1150">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1150">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="3a8fe-1151">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1151">Updated cmdlets</span></span>
        - <span data-ttu-id="3a8fe-1152">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1152">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="3a8fe-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="3a8fe-1154">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1154">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="3a8fe-1155">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1155">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="3a8fe-1156">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1156">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a8fe-1157">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1157">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a8fe-1158">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1158">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="3a8fe-1159">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1159">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="3a8fe-1160">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1160">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-1162">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1162">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="3a8fe-1163">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1163">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="3a8fe-1164">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1164">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="3a8fe-1165">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1165">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="3a8fe-1166">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1166">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="3a8fe-1167">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1167">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="3a8fe-1168">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1168">Az.Relay</span></span>
* <span data-ttu-id="3a8fe-1169">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1169">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a8fe-1170">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1170">Az.ServiceBus</span></span>
* <span data-ttu-id="3a8fe-1171">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1171">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-1172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1172">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-1173">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1173">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="3a8fe-1174">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1174">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="3a8fe-1175">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1175">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="3a8fe-1176">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1176">New-AzStorageAccount</span></span>
* <span data-ttu-id="3a8fe-1177">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1177">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="3a8fe-1178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1178">New-AzStorageAccount</span></span>
    - <span data-ttu-id="3a8fe-1179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1179">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="3a8fe-1180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1180">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1181">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1181">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-1182">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1182">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="3a8fe-1183">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1183">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="3a8fe-1184">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1184">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a8fe-1185">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1185">Highlights since the last major release</span></span>
* <span data-ttu-id="3a8fe-1186">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1186">General availability of `Az` module</span></span>
* <span data-ttu-id="3a8fe-1187">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1187">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a8fe-1188">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1188">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a8fe-1189">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1189">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a8fe-1190">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1190">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a8fe-1191">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1191">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1192">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1192">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1193">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1193">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1194">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1194">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="3a8fe-1195">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1195">Az.Batch</span></span>
* <span data-ttu-id="3a8fe-1196">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a8fe-1197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1197">Az.Cdn</span></span>
* <span data-ttu-id="3a8fe-1198">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a8fe-1199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1199">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a8fe-1200">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1200">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1201">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1202">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1202">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="3a8fe-1203">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a8fe-1204">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1204">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1205">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-1206">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1206">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1207">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1207">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-1208">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a8fe-1209">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1209">Az.EventGrid</span></span>
* <span data-ttu-id="3a8fe-1210">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1210">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a8fe-1211">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1211">Az.EventHub</span></span>
* <span data-ttu-id="3a8fe-1212">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1212">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="3a8fe-1213">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1213">Az.HDInsight</span></span>
* <span data-ttu-id="3a8fe-1214">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1214">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a8fe-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1215">Az.IotHub</span></span>
* <span data-ttu-id="3a8fe-1216">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a8fe-1217">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1217">Az.KeyVault</span></span>
* <span data-ttu-id="3a8fe-1218">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a8fe-1219">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1219">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="3a8fe-1220">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1220">Az.MachineLearning</span></span>
* <span data-ttu-id="3a8fe-1221">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="3a8fe-1222">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1222">Az.Media</span></span>
* <span data-ttu-id="3a8fe-1223">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-1224">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1224">Az.Monitor</span></span>
  * <span data-ttu-id="3a8fe-1225">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1225">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="3a8fe-1226">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1226">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="3a8fe-1227">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1227">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="3a8fe-1228">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1228">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3a8fe-1229">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1229">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="3a8fe-1230">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1230">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="3a8fe-1231">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1231">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1232">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1232">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1233">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a8fe-1234">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1234">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="3a8fe-1235">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1235">Az.NotificationHubs</span></span>
* <span data-ttu-id="3a8fe-1236">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a8fe-1237">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1237">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a8fe-1238">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="3a8fe-1239">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1239">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="3a8fe-1240">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1241">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1241">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-1242">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a8fe-1243">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1243">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="3a8fe-1244">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1244">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="3a8fe-1245">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1245">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a8fe-1246">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1246">Az.RedisCache</span></span>
* <span data-ttu-id="3a8fe-1247">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1248">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1248">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1249">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1249">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1250">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1251">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1251">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="3a8fe-1252">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a8fe-1253">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1253">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="3a8fe-1254">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1254">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="3a8fe-1255">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1255">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="3a8fe-1256">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1256">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="3a8fe-1257">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1257">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1258">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-1259">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1259">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="3a8fe-1260">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="3a8fe-1261">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1261">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="3a8fe-1262">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1262">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="3a8fe-1263">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1263">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a8fe-1264">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1264">Highlights since the last major release</span></span>
* <span data-ttu-id="3a8fe-1265">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1265">General availability of `Az` module</span></span>
* <span data-ttu-id="3a8fe-1266">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1266">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a8fe-1267">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1267">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a8fe-1268">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1268">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a8fe-1269">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1269">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a8fe-1270">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1270">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1271">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1271">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1272">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1273">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a8fe-1274">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1274">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a8fe-1275">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1275">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="3a8fe-1276">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1276">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1277">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1278">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1278">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="3a8fe-1279">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1279">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="3a8fe-1280">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1280">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1281">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1282">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1282">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="3a8fe-1283">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1283">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="3a8fe-1284">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1284">Az.ContainerInstance</span></span>
* <span data-ttu-id="3a8fe-1285">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1285">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-1286">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1286">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-1287">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1287">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="3a8fe-1288">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1288">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1289">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1289">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1290">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1290">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="3a8fe-1291">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1291">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="3a8fe-1292">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1292">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="3a8fe-1293">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1293">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="3a8fe-1294">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1294">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="3a8fe-1295">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1295">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1296">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1296">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1297">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1297">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1298">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-1299">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1299">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="3a8fe-1300">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1300">New-AzStorageContext</span></span>
* <span data-ttu-id="3a8fe-1301">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1301">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="3a8fe-1302">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1302">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3a8fe-1303">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1303">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="3a8fe-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="3a8fe-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="3a8fe-1306">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1306">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="3a8fe-1307">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1307">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3a8fe-1308">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1308">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="3a8fe-1309">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1309">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="3a8fe-1310">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1310">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="3a8fe-1311">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1311">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="3a8fe-1312">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="3a8fe-1313">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1313">General availability of `Az` module</span></span>
* <span data-ttu-id="3a8fe-1314">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1314">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="3a8fe-1315">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1315">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="3a8fe-1316">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1316">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="3a8fe-1317">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1317">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a8fe-1318">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1318">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1319">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1319">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-1320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1320">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1321">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1321">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="3a8fe-1322">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1322">Dynamic grouping</span></span>
    * <span data-ttu-id="3a8fe-1323">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1323">Pre-Post script</span></span>
    * <span data-ttu-id="3a8fe-1324">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1324">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1325">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1326">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1326">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="3a8fe-1327">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1327">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a8fe-1328">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1328">Az.KeyVault</span></span>
* <span data-ttu-id="3a8fe-1329">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1329">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1330">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1331">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1331">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="3a8fe-1332">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1332">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1333">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1333">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-1334">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1334">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="3a8fe-1335">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1335">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1336">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1336">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1337">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1337">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="3a8fe-1338">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1338">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1339">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1340">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1340">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-1341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1341">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-1342">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1342">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="3a8fe-1343">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1343">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a8fe-1344">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1344">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a8fe-1345">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1345">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="3a8fe-1346">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1346">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="3a8fe-1347">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1347">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="3a8fe-1348">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1348">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1349">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-1350">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1350">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="3a8fe-1351">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1351">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1352">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1353">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1353">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="3a8fe-1354">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1354">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-1355">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1355">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1356">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1356">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="3a8fe-1357">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1357">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="3a8fe-1358">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1358">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a8fe-1359">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1359">Az.Cdn</span></span>
* <span data-ttu-id="3a8fe-1360">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1360">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1361">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1362">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1362">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-1363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1363">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-1364">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1364">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a8fe-1365">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1365">Az.LogicApp</span></span>
* <span data-ttu-id="3a8fe-1366">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1366">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1367">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1367">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1368">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1368">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1369">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-1370">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1370">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="3a8fe-1371">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1371">SDK Update</span></span>
* <span data-ttu-id="3a8fe-1372">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1372">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="3a8fe-1373">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1373">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1374">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1375">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1375">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="3a8fe-1376">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1376">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="3a8fe-1377">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1377">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="3a8fe-1378">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1378">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="3a8fe-1379">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1379">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="3a8fe-1380">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1380">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1381">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1382">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1382">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="3a8fe-1383">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1383">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-1384">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1384">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-1385">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1385">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="3a8fe-1386">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1386">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="3a8fe-1387">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1387">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a8fe-1388">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1388">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1389">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1390">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1390">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="3a8fe-1391">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1391">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="3a8fe-1392">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1392">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a8fe-1393">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1393">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a8fe-1394">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1394">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1395">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1396">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1396">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="3a8fe-1397">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1397">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="3a8fe-1398">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1398">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="3a8fe-1399">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1399">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1400">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1400">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-1401">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1401">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="3a8fe-1402">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1402">Az.EventHub</span></span>
* <span data-ttu-id="3a8fe-1403">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1403">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="3a8fe-1404">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1404">Az.KeyVault</span></span>
* <span data-ttu-id="3a8fe-1405">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1405">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a8fe-1406">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1406">Az.LogicApp</span></span>
* <span data-ttu-id="3a8fe-1407">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1407">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="3a8fe-1408">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1408">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="3a8fe-1409">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1409">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="3a8fe-1410">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1410">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a8fe-1411">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1411">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a8fe-1412">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1412">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="3a8fe-1413">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1413">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="3a8fe-1414">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1414">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="3a8fe-1415">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1415">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a8fe-1416">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1416">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a8fe-1417">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1417">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="3a8fe-1418">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1418">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="3a8fe-1419">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1419">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="3a8fe-1420">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1420">Az.Monitor</span></span>
* <span data-ttu-id="3a8fe-1421">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1421">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1422">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1422">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1423">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1423">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="3a8fe-1424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1424">Az.OperationalInsights</span></span>
* <span data-ttu-id="3a8fe-1425">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1425">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="3a8fe-1426">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1426">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="3a8fe-1427">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1427">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1428">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1429">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1429">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3a8fe-1430">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1430">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="3a8fe-1431">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1431">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="3a8fe-1432">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1432">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1433">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1433">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1434">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1434">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="3a8fe-1435">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1435">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1436">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1436">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-1437">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1437">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="3a8fe-1438">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1438">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1439">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1439">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1440">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1440">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a8fe-1441">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1441">Az.AnalysisServices</span></span>
<span data-ttu-id="3a8fe-1442">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1442">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1443">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1444">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1444">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="3a8fe-1445">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1445">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="3a8fe-1446">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1446">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1447">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1447">Az.RecoveryServices</span></span>
<span data-ttu-id="3a8fe-1448">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1448">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1449">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1450">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1450">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="3a8fe-1451">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1451">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="3a8fe-1452">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1452">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="3a8fe-1453">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1453">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1454">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1454">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1455">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1455">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="3a8fe-1456">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1456">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="3a8fe-1457">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1457">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="3a8fe-1458">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1458">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1459">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1459">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1460">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1460">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="3a8fe-1461">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1461">Az.AnalysisServices</span></span>
* <span data-ttu-id="3a8fe-1462">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1462">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="3a8fe-1464">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1464">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="3a8fe-1465">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1465">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1466">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1467">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1467">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="3a8fe-1468">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1468">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a8fe-1469">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1469">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="3a8fe-1470">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1470">Az.Aks</span></span>
* <span data-ttu-id="3a8fe-1471">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1471">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="3a8fe-1472">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1472">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1473">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1473">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="3a8fe-1474">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1474">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="3a8fe-1475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1475">Az.Cdn</span></span>
* <span data-ttu-id="3a8fe-1476">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1476">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1477">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1478">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1478">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="3a8fe-1479">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1479">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="3a8fe-1480">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1480">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="3a8fe-1481">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1481">Az.ContainerRegistry</span></span>
* <span data-ttu-id="3a8fe-1482">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1482">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="3a8fe-1483">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1483">Az.DataFactory</span></span>
* <span data-ttu-id="3a8fe-1484">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1484">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1485">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-1486">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1486">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="3a8fe-1487">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1487">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="3a8fe-1488">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1488">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a8fe-1489">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1489">Az.IotHub</span></span>
* <span data-ttu-id="3a8fe-1490">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1490">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="3a8fe-1491">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1491">Az.KeyVault</span></span>
* <span data-ttu-id="3a8fe-1492">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1492">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1493">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1494">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1494">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1495">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1496">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1496">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="3a8fe-1497">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1497">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="3a8fe-1498">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1498">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="3a8fe-1499">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1499">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="3a8fe-1500">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1500">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="3a8fe-1501">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1501">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="3a8fe-1502">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1502">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-1503">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1503">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-1504">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1504">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="3a8fe-1505">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1505">Fix some error messages.</span></span>
* <span data-ttu-id="3a8fe-1506">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1506">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="3a8fe-1507">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1507">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a8fe-1508">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1508">Az.SignalR</span></span>
* <span data-ttu-id="3a8fe-1509">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1509">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1510">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1511">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1511">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a8fe-1512">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1512">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="3a8fe-1513">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1513">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="3a8fe-1514">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1514">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-1515">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1515">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-1516">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a8fe-1517">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1517">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="3a8fe-1518">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1518">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="3a8fe-1519">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1519">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="3a8fe-1520">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1520">Az.TrafficManager</span></span>
* <span data-ttu-id="3a8fe-1521">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1521">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1522">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1522">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-1523">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1523">Update incorrect online help URLs</span></span>
* <span data-ttu-id="3a8fe-1524">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1524">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="3a8fe-1525">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1525">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="3a8fe-1526">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1526">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1527">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1527">Az.Accounts</span></span>
* <span data-ttu-id="3a8fe-1528">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1528">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1529">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1529">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1530">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1530">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="3a8fe-1531">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1531">Updated the description of ID in help files</span></span>
* <span data-ttu-id="3a8fe-1532">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1532">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1533">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1533">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-1534">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1534">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="3a8fe-1535">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1535">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="3a8fe-1536">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1536">Az.EventGrid</span></span>
* <span data-ttu-id="3a8fe-1537">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1537">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="3a8fe-1538">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1538">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="3a8fe-1539">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1539">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3a8fe-1540">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1540">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3a8fe-1541">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1541">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3a8fe-1542">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1542">Dead letter endpoint.</span></span>
    - <span data-ttu-id="3a8fe-1543">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1543">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="3a8fe-1544">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1544">Event Time-To-Live,</span></span>
        - <span data-ttu-id="3a8fe-1545">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1545">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="3a8fe-1546">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1546">Dead letter endpoint.</span></span>
* <span data-ttu-id="3a8fe-1547">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1547">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="3a8fe-1548">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1548">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="3a8fe-1549">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1549">Az.IotHub</span></span>
* <span data-ttu-id="3a8fe-1550">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1550">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="3a8fe-1551">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1551">Az.LogicApp</span></span>
* <span data-ttu-id="3a8fe-1552">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1552">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1553">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1554">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1554">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="3a8fe-1555">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1555">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="3a8fe-1556">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1556">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3a8fe-1557">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1557">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="3a8fe-1558">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1558">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="3a8fe-1559">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1559">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="3a8fe-1560">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1560">Az.SignalR</span></span>
* <span data-ttu-id="3a8fe-1561">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1561">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1562">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1563">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1563">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="3a8fe-1564">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1564">Az.Storage</span></span>
* <span data-ttu-id="3a8fe-1565">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1565">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="3a8fe-1566">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1566">New-AzStorageContext</span></span>
* <span data-ttu-id="3a8fe-1567">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1567">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="3a8fe-1568">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1568">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1569">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-1570">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1570">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="3a8fe-1571">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1571">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="3a8fe-1572">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1572">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="3a8fe-1573">Geral</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1573">General</span></span>

- <span data-ttu-id="3a8fe-1574">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1574">General Availability of Az Module</span></span>
- <span data-ttu-id="3a8fe-1575">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1575">Online help for each module</span></span>
- <span data-ttu-id="3a8fe-1576">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1576">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="3a8fe-1577">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1577">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="3a8fe-1578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1578">Az.Accounts</span></span>
- <span data-ttu-id="3a8fe-1579">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1579">Changed from Az.Profile</span></span>
- <span data-ttu-id="3a8fe-1580">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1580">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3a8fe-1581">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1581">Az.ApiManagement</span></span>
- <span data-ttu-id="3a8fe-1582">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1582">Fixes for #7002</span></span>
- <span data-ttu-id="3a8fe-1583">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1583">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="3a8fe-1584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1584">Az.Batch</span></span>
- <span data-ttu-id="3a8fe-1585">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1585">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="3a8fe-1586">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1586">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="3a8fe-1587">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1587">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="3a8fe-1588">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1588">Az.Billing</span></span>
- <span data-ttu-id="3a8fe-1589">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1589">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="3a8fe-1590">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1590">Az.CognitivServices</span></span>
- <span data-ttu-id="3a8fe-1591">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1591">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="3a8fe-1592">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1592">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3a8fe-1593">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1593">Az.ContainerInstance</span></span>
- <span data-ttu-id="3a8fe-1594">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1594">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="3a8fe-1595">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1595">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="3a8fe-1596">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1596">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1597">Az.DataLakeStore</span></span>
- <span data-ttu-id="3a8fe-1598">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1598">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="3a8fe-1599">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1599">Az.Monitor</span></span>
- <span data-ttu-id="3a8fe-1600">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1600">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="3a8fe-1601">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1601">Az.KeyVault</span></span>
- <span data-ttu-id="3a8fe-1602">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1602">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="3a8fe-1603">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1603">Az.MachineLearning</span></span>
- <span data-ttu-id="3a8fe-1604">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1604">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="3a8fe-1605">Az.Media</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1605">Az.Media</span></span>
- <span data-ttu-id="3a8fe-1606">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1606">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1607">Az.Network</span></span>
<span data-ttu-id="3a8fe-1608">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1608">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="3a8fe-1609">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1609">New cmdlets added:</span></span>
        - <span data-ttu-id="3a8fe-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a8fe-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a8fe-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a8fe-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a8fe-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="3a8fe-1615">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1615">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="3a8fe-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="3a8fe-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="3a8fe-1618">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1618">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="3a8fe-1619">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1619">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="3a8fe-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3a8fe-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="3a8fe-1622">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1622">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="3a8fe-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="3a8fe-1624">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1624">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="3a8fe-1625">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1625">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="3a8fe-1626">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1626">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3a8fe-1627">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1627">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="3a8fe-1628">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1628">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="3a8fe-1629">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1629">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="3a8fe-1630">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1630">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="3a8fe-1631">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1631">Az.OperationalInsights</span></span>
- <span data-ttu-id="3a8fe-1632">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1632">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="3a8fe-1633">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1633">Az.Profile</span></span>
- <span data-ttu-id="3a8fe-1634">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1634">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1635">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1635">Az.RecoveryServices</span></span>
- <span data-ttu-id="3a8fe-1636">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1636">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="3a8fe-1637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1637">Az.Resources</span></span>
- <span data-ttu-id="3a8fe-1638">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1638">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1639">Az.ServiceFabric</span></span>
- <span data-ttu-id="3a8fe-1640">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1640">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="3a8fe-1641">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1641">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="3a8fe-1642">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1642">Az.SIgnalR</span></span>
- <span data-ttu-id="3a8fe-1643">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1643">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="3a8fe-1644">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1644">Az.Sql</span></span>
- <span data-ttu-id="3a8fe-1645">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1645">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="3a8fe-1646">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1646">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="3a8fe-1647">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1647">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="3a8fe-1648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1648">Az.Storage</span></span>
- <span data-ttu-id="3a8fe-1649">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1650">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1650">Az.Websites</span></span>
- <span data-ttu-id="3a8fe-1651">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="3a8fe-1652">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1652">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="3a8fe-1653">Geral</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1653">General</span></span>

* <span data-ttu-id="3a8fe-1654">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1654">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="3a8fe-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1655">Az.Compute</span></span>

* <span data-ttu-id="3a8fe-1656">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1656">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1657">Az.DataLakeStore</span></span>

* <span data-ttu-id="3a8fe-1658">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1658">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="3a8fe-1659">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1659">Az.FrontDoor</span></span>

* <span data-ttu-id="3a8fe-1660">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1660">Fixed some broken links</span></span>
    - <span data-ttu-id="3a8fe-1661">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1661">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="3a8fe-1662">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1662">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="3a8fe-1663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1663">Az.RecoveryServices</span></span>

* <span data-ttu-id="3a8fe-1664">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1664">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="3a8fe-1665">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1665">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="3a8fe-1666">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1666">Az.Resources</span></span>

* <span data-ttu-id="3a8fe-1667">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1667">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="3a8fe-1668">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1668">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="3a8fe-1669">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1669">Az.Sql</span></span>

* <span data-ttu-id="3a8fe-1670">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1670">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="3a8fe-1671">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1671">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="3a8fe-1672">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1672">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="3a8fe-1673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1673">Az.Storage</span></span>

* <span data-ttu-id="3a8fe-1674">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1674">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="3a8fe-1675">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1675">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="3a8fe-1676">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1676">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3a8fe-1677">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1677">Support Static Website configuration</span></span>
    - <span data-ttu-id="3a8fe-1678">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1678">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="3a8fe-1679">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1679">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1680">Az.Websites</span></span>

* <span data-ttu-id="3a8fe-1681">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1681">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="3a8fe-1682">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1682">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="3a8fe-1683">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1683">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="3a8fe-1684">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1684">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="3a8fe-1685">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1685">Az.ApiManagement</span></span>
* <span data-ttu-id="3a8fe-1686">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1686">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="3a8fe-1687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1687">Az.Automation</span></span>
* <span data-ttu-id="3a8fe-1688">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1688">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="3a8fe-1689">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1689">Added Update Management cmdlets</span></span>
* <span data-ttu-id="3a8fe-1690">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1690">Added Source Control cmdlets</span></span>
* <span data-ttu-id="3a8fe-1691">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1691">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="3a8fe-1692">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1692">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="3a8fe-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1693">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1694">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1694">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="3a8fe-1695">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1695">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="3a8fe-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="3a8fe-1697">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1697">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="3a8fe-1698">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1698">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="3a8fe-1699">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1699">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1700">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1700">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1701">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1701">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="3a8fe-1702">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1702">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="3a8fe-1703">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1703">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="3a8fe-1704">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1704">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="3a8fe-1705">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1705">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="3a8fe-1706">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1706">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="3a8fe-1707">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1707">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="3a8fe-1708">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1708">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="3a8fe-1709">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1709">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="3a8fe-1710">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1710">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="3a8fe-1711">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1711">Az.Relay</span></span>
* <span data-ttu-id="3a8fe-1712">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1712">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="3a8fe-1713">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1713">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1714">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1714">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="3a8fe-1715">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1715">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="3a8fe-1716">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1716">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-1717">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1717">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-1718">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1718">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="3a8fe-1719">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1719">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1720">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1720">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="3a8fe-1721">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1721">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a8fe-1722">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1722">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a8fe-1723">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1723">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a8fe-1724">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1724">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="3a8fe-1725">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1725">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a8fe-1726">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1726">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a8fe-1727">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1727">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="3a8fe-1728">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1728">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="3a8fe-1729">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1729">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="3a8fe-1730">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1730">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="3a8fe-1731">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1731">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="3a8fe-1732">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1732">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3a8fe-1733">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1733">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="3a8fe-1734">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1734">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="3a8fe-1735">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1735">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="3a8fe-1736">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1736">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="3a8fe-1737">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1737">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="3a8fe-1738">Geral</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1738">General</span></span>
* <span data-ttu-id="3a8fe-1739">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1739">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="3a8fe-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1740">Az.Profile</span></span>
* <span data-ttu-id="3a8fe-1741">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1741">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="3a8fe-1742">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1742">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="3a8fe-1743">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1743">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="3a8fe-1744">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1744">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="3a8fe-1745">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1745">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="3a8fe-1746">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1746">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="3a8fe-1747">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1747">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="3a8fe-1748">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1748">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a8fe-1749">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1749">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1750">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1751">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1751">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="3a8fe-1752">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1752">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="3a8fe-1753">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1753">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1754">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1754">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-1755">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1755">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="3a8fe-1756">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1756">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="3a8fe-1757">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1757">Az.Insights</span></span>
* <span data-ttu-id="3a8fe-1758">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1758">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="3a8fe-1759">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1759">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="3a8fe-1760">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1760">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="3a8fe-1761">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1761">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1762">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1762">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1763">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1763">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="3a8fe-1764">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1764">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="3a8fe-1765">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1765">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="3a8fe-1766">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1766">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="3a8fe-1767">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1767">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="3a8fe-1768">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1768">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="3a8fe-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="3a8fe-1770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1770">Az.PolicyInsights</span></span>
* <span data-ttu-id="3a8fe-1771">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1771">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1772">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1772">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1773">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1773">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="3a8fe-1774">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1774">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="3a8fe-1775">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1775">Az.ServiceBus</span></span>
* <span data-ttu-id="3a8fe-1776">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1776">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="3a8fe-1777">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1777">Az.ServiceFabric</span></span>
* <span data-ttu-id="3a8fe-1778">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1778">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="3a8fe-1779">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1779">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="3a8fe-1780">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1780">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="3a8fe-1781">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1781">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="3a8fe-1782">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1782">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="3a8fe-1783">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1783">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="3a8fe-1784">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1784">Az.Profile</span></span>
* <span data-ttu-id="3a8fe-1785">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1785">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="3a8fe-1786">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1786">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1787">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1787">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1788">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1788">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="3a8fe-1789">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1789">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="3a8fe-1790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1790">Az.DataLakeStore</span></span>
* <span data-ttu-id="3a8fe-1791">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1791">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="3a8fe-1792">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1792">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="3a8fe-1793">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1793">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3a8fe-1794">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1794">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="3a8fe-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1796">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1797">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1797">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="3a8fe-1798">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1798">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1799">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1800">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1800">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="3a8fe-1801">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1801">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="3a8fe-1802">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1802">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="3a8fe-1803">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1803">Azure.Storage</span></span>
* <span data-ttu-id="3a8fe-1804">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1804">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="3a8fe-1805">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1805">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="3a8fe-1806">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1806">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="3a8fe-1807">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1807">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="3a8fe-1808">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1808">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="3a8fe-1809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1809">Az.CognitiveServices</span></span>
* <span data-ttu-id="3a8fe-1810">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1810">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="3a8fe-1811">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1811">Az.Compute</span></span>
* <span data-ttu-id="3a8fe-1812">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1812">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="3a8fe-1813">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1813">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="3a8fe-1814">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1814">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="3a8fe-1815">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1815">Az.DataFactoryV2</span></span>
* <span data-ttu-id="3a8fe-1816">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1816">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="3a8fe-1817">Az.Network</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1817">Az.Network</span></span>
* <span data-ttu-id="3a8fe-1818">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1818">Added NetworkProfile functionality.</span></span> <span data-ttu-id="3a8fe-1819">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1819">new cmdlets added</span></span>
    - <span data-ttu-id="3a8fe-1820">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1820">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a8fe-1821">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1821">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a8fe-1822">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1822">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a8fe-1823">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1823">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="3a8fe-1824">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1824">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="3a8fe-1825">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1825">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="3a8fe-1826">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1826">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="3a8fe-1827">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1827">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="3a8fe-1828">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1828">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="3a8fe-1829">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1829">Az.RedisCache</span></span>
* <span data-ttu-id="3a8fe-1830">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1830">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="3a8fe-1831">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1831">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="3a8fe-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1832">Az.Resources</span></span>
* <span data-ttu-id="3a8fe-1833">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1833">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="3a8fe-1834">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1834">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="3a8fe-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1835">Az.Sql</span></span>
* <span data-ttu-id="3a8fe-1836">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1836">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="3a8fe-1837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1837">Az.Websites</span></span>
* <span data-ttu-id="3a8fe-1838">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1838">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="3a8fe-1839">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1839">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="3a8fe-1840">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1840">0.2.0 - September 2018</span></span>
 <span data-ttu-id="3a8fe-1841">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="3a8fe-1841">Initial Release</span></span>
