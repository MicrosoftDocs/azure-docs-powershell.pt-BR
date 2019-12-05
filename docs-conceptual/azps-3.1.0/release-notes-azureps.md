---
title: Notas sobre a versão do Azure PowerShell
description: Saiba mais sobre todas as atualizações mais recentes dos módulos do Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537117"
---
## <a name="310---november-2019"></a><span data-ttu-id="7d4ac-103">3.1.0 – Novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7d4ac-104">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="7d4ac-104">Highlights since the last major release</span></span>
* <span data-ttu-id="7d4ac-105">Az.DataBoxEdge 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="7d4ac-106">Az.SqlVirtualMachine 1.0.0 lançado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-107">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-108">Recurso Reapply da VM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-108">VM Reapply feature</span></span>
    - <span data-ttu-id="7d4ac-109">Adicionar parâmetro Reapply ao cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="7d4ac-110">Recurso AutomaticRepairs do conjunto de dimensionamento da VM:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="7d4ac-111">Adicionar os parâmetros EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent aos cmdlets a seguir:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="7d4ac-112">Suporte de imagem da galeria entre locatários para New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="7d4ac-113">Adicionar 'Spot' ao completador de argumento do parâmetro Priority nos cmdlets New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7d4ac-114">Adicionar os parâmetros DiskIOPSReadWrite e DiskMBpsReadWrite ao cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="7d4ac-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="7d4ac-115">Alterar o parâmetro SourceImageId do cmdlet New-AzGalleryImageVersion para opcional</span><span class="sxs-lookup"><span data-stu-id="7d4ac-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="7d4ac-116">Adicionar os parâmetros OSDiskImage e DataDiskImage ao cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7d4ac-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="7d4ac-117">Adicionar o parâmetro HyperVGeneration ao cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="7d4ac-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="7d4ac-118">Adicionar os parâmetros SkipExtensionsOnOverprovisionedVMs aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7d4ac-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7d4ac-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7d4ac-120">Cmdlet `Get-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7d4ac-121">Obter a ordem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-121">Get the Order</span></span>
* <span data-ttu-id="7d4ac-122">Cmdlet `New-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7d4ac-123">Criar ordem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-123">Create new Order</span></span>
* <span data-ttu-id="7d4ac-124">Cmdlet `Remove-AzDataBoxEdgeOrder` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7d4ac-125">Remover a ordem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-125">Remove the Order</span></span>
* <span data-ttu-id="7d4ac-126">Alterar no cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="7d4ac-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="7d4ac-127">Agora cria o Compartilhamento Local</span><span class="sxs-lookup"><span data-stu-id="7d4ac-127">Now creates Local Share</span></span>
* <span data-ttu-id="7d4ac-128">Cmdlet `Set-AzDataBoxEdgeRole` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="7d4ac-129">Agora IotRole pode ser mapeado para Compartilhar</span><span class="sxs-lookup"><span data-stu-id="7d4ac-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="7d4ac-130">Cmdlet `Invoke-AzDataBoxEdgeDevice` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="7d4ac-131">Invocar atualização da verificação e do download e instalar as atualizações no dispositivo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="7d4ac-132">Cmdlet `Get-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7d4ac-133">Obtém as informações sobre Gatilhos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="7d4ac-134">Cmdlet `New-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7d4ac-135">Criar gatilhos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-135">Create new Triggers</span></span>
* <span data-ttu-id="7d4ac-136">Cmdlet `Remove-AzDataBoxEdgeTrigger` adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7d4ac-137">Remover os gatilhos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-138">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-139">Atualizar a versão do SDK do .NET do ADF para 4.4.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="7d4ac-140">Adicionar parâmetro 'ExpressCustomSetup' do cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' para habilitar configurações de instalação e componentes de terceiros sem o script de instalação personalizado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-142">Atualizar a documentação de Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d4ac-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-143">Az.EventHub</span></span>
* <span data-ttu-id="7d4ac-144">Correção para o problema 10301: corrigir o formato de data do Token SAS</span><span class="sxs-lookup"><span data-stu-id="7d4ac-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7d4ac-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-145">Az.FrontDoor</span></span>
* <span data-ttu-id="7d4ac-146">Adicionar o parâmetro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="7d4ac-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="7d4ac-147">Adicionar os parâmetros HealthProbeMethod e EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="7d4ac-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="7d4ac-148">Adicionar novo cmdlet para criar o objeto BackendPoolsSettings para passar para a criação/atualização do Front Door</span><span class="sxs-lookup"><span data-stu-id="7d4ac-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="7d4ac-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="7d4ac-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-150">Az.Network</span></span>
* <span data-ttu-id="7d4ac-151">Altere os exemplos de opção FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7d4ac-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7d4ac-152">Az.PrivateDns</span></span>
* <span data-ttu-id="7d4ac-153">SDK do .NET PrivateDns atualizado para a versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-155">Suporte do Azure Site Recovery para selecionar o tipo de disco ao habilitar a proteção.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="7d4ac-156">Correção de bug do Azure Site Recovery para a edição da ação do plano de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="7d4ac-157">Suporte à restauração do SQL do Backup do Azure para aceitar BDs de fluxo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7d4ac-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7d4ac-158">Az.RedisCache</span></span>
* <span data-ttu-id="7d4ac-159">Parâmetro 'MinimumTlsVersion' adicionado nos cmdlets 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="7d4ac-160">Além disso, 'MinimumTlsVersion' foi adicionado na saída do cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="7d4ac-161">Validação adicionada no parâmetro '-Size' para os cmdlets 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-162">Az.Resources</span></span>
- <span data-ttu-id="7d4ac-163">Cmdlets de política atualizados para usar uma nova versão da API 2019-06-01 que tem uma nova propriedade EnforcementMode na atribuição de política.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="7d4ac-164">Exemplo de ajuda de criar definição de política atualizado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="7d4ac-165">Corrija o bug Remove-AZADServicePrincipal-ServicePrincipalName e gere referência nula quando o nome da entidade de serviço não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="7d4ac-166">Corrija o bug New-AZADServicePrincipal e gere referência nula quando o locatário não tiver nenhuma assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="7d4ac-167">Altere New-AzAdServicePrincipal para adicionar credenciais apenas ao aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-168">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-169">Suporte para o banco de dados ReadReplicaCount adicionado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="7d4ac-170">Set-AzSqlDatabase corrigido quando a redundância de zona não está definida</span><span class="sxs-lookup"><span data-stu-id="7d4ac-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="7d4ac-171">3.0.0 – novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7d4ac-172">Geral</span><span class="sxs-lookup"><span data-stu-id="7d4ac-172">General</span></span>
* <span data-ttu-id="7d4ac-173">Az.PrivateDns 1.0.0 liberado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-174">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-175">Adicionar uma mensagem de reprovação para o alias 'Resolve-Error'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7d4ac-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-176">Az.Advisor</span></span>
* <span data-ttu-id="7d4ac-177">Nova categoria 'Excelência Operacional' adicionada para o cmdlet Get-AzAdvisorRecommendation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7d4ac-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7d4ac-178">Az.Batch</span></span>
* <span data-ttu-id="7d4ac-179">`CoreQuota` renomeado em `BatchAccountContext` para `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7d4ac-180">Também há um novo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7d4ac-181">Isso afeta o **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7d4ac-182">O parâmetro `-ResourceFile` do **New-AzBatchTask** agora usa uma coleção de objetos do `PSResourceFile` que podem ser construídos usando o novo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7d4ac-183">Novo cmdlet **New-AzBatchResourceFile** para ajudar a criar `PSResourceFile` objetos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7d4ac-184">Eles podem ser fornecidos para **New-AzBatchTask** no parâmetro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7d4ac-185">Isso é compatível com dois novos tipos de arquivo de recurso, além da maneira `HttpUrl` existente:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7d4ac-186">Os arquivos de recursos baseados em `AutoStorageContainerName` baixam um contêiner de armazenamento automático inteiro para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7d4ac-187">Os arquivos de recursos baseados em `StorageContainerUrl` baixam o contêiner especificado na URL para o nó do Lote.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7d4ac-188">Propriedade `ApplicationPackages` removida de `PSApplication` retornada por **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7d4ac-189">Os pacotes específicos dentro de um aplicativo agora podem ser recuperados usando o **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7d4ac-190">Por exemplo: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7d4ac-191">`ApplicationId` renomeado para `ApplicationName` em **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7d4ac-192">`ApplicationId` agora é um alias de `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7d4ac-193">Nova propriedade `PSWindowsUserConfiguration` adicionada a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7d4ac-194">`Version` renomeado para `Name` em `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7d4ac-195">`BlobSource` renomeado para `HttpUrl` em `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7d4ac-196">A propriedade `OSDisk` foi removida de `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7d4ac-197">O **Set-AzBatchPoolOSVersion** removido.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7d4ac-198">Não há mais suporte para esta operação.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="7d4ac-199">`TargetOSVersion` removido de `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7d4ac-200">`CurrentOSVersion` renomeado para `OSVersion` em `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7d4ac-201">`DataEgressGiB` e `DataIngressGiB` removidos de `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7d4ac-202">O **Get-AzBatchNodeAgentSku** foi removido e substituído por **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="7d4ac-203">**Get-AzBatchSupportedImage** retorna os mesmos dados que **Get-AzBatchNodeAgentSku**, mas em um formato mais amigável.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7d4ac-204">Novas imagens não verificadas agora também são retornadas.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="7d4ac-205">Informações adicionais sobre `Capabilities` e `BatchSupportEndOfLife` para cada imagem também estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7d4ac-206">Foi adicionada a capacidade de montar sistemas de arquivos remotos em cada nó de um pool por meio do novo parâmetro `MountConfiguration` de **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7d4ac-207">Agora, dê suporte às regras de segurança de rede bloqueando o acesso à rede para um pool com base na porta de origem do tráfego.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7d4ac-208">Isso é feito por meio da propriedade `SourcePortRanges` em `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7d4ac-209">Ao executar um contêiner, o Lote agora é compatível com a execução da tarefa no diretório de trabalho do contêiner ou no diretório de trabalho da tarefa do Lote.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7d4ac-210">Isso é controlado pela propriedade `WorkingDirectory` em `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7d4ac-211">Capacidade adicional para especificar uma coleção de IPs públicos em `PSNetworkConfiguration` por meio da nova propriedade `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7d4ac-212">Isso garante que os nós no Pool terão um IP da lista de IPs fornecidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7d4ac-213">Quando não especificado, o valor padrão de `WaitForSuccess` em `PSSTartTask` agora é `$True` (antes `$False`).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7d4ac-214">Quando não especificado, o valor padrão de `Scope` em `PSAutoUserSpecification` agora é `Pool` (era `Task` no Windows e `Pool` no Linux).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d4ac-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d4ac-215">Az.Cdn</span></span>
* <span data-ttu-id="7d4ac-216">UrlRewriteAction e CacheKeyQueryStringAction introduzido no RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7d4ac-217">Correção de vários bugs, como a entrada 'Seletor' ausente no cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-218">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-219">Recurso do Conjunto de Criptografia de Disco</span><span class="sxs-lookup"><span data-stu-id="7d4ac-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7d4ac-220">Novos cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7d4ac-221">O parâmetro DiskEncryptionSetId é adicionado aos seguintes cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="7d4ac-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7d4ac-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7d4ac-223">Os parâmetros DiskEncryptionSetId e EncryptionType são adicionados aos seguintes cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7d4ac-224">Adicionar o parâmetro PublicIPAddressVersion ao New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7d4ac-225">Mova o FileUris da extensão de script personalizado da configuração pública para a configuração protegida</span><span class="sxs-lookup"><span data-stu-id="7d4ac-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7d4ac-226">Adicionar ScaleInPolicy aos cmdlets New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7d4ac-227">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="7d4ac-227">Breaking changes</span></span>
    - <span data-ttu-id="7d4ac-228">O parâmetro UploadSizeInBytes é usado em vez de DiskSizeGB para New-AzDiskConfig quando CreateOption for carregado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7d4ac-229">PublishingProfile.Source.ManagedImage.Id é substituído por StorageProfile.Source.Id no objeto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7d4ac-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-230">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-231">Atualizar a versão do SDK do .NET do ADF para 4.3.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-233">Atualização da versão do SDK do ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), que apresenta as seguintes correções</span><span class="sxs-lookup"><span data-stu-id="7d4ac-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7d4ac-234">Evitar lançar exceção enquanto não for possível desserializar o creationtime da entrada da lixeira ou do diretório.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7d4ac-235">Exposição da configuração por tempo limite da solicitação em adlsclient</span><span class="sxs-lookup"><span data-stu-id="7d4ac-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7d4ac-236">Correção da passagem do syncflag original para a recuperação do badoffset</span><span class="sxs-lookup"><span data-stu-id="7d4ac-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7d4ac-237">Correção do EnumerateDirectory para recuperar o token de continuação depois que a resposta for verificada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7d4ac-238">Correção do bug Concat</span><span class="sxs-lookup"><span data-stu-id="7d4ac-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7d4ac-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-239">Az.FrontDoor</span></span>
* <span data-ttu-id="7d4ac-240">Diversos erros de digitação corrigidos no módulo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7d4ac-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7d4ac-241">Az.HDInsight</span></span>
* <span data-ttu-id="7d4ac-242">Após a correção do bug, o cliente verá o erro 'não é uma cadeia de caracteres válida de Base 64' ao usar o Get-AzHDInsightCluster para obter o cluster com armazenamento ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7d4ac-243">Adicionar um parâmetro chamado 'ApplicationId' a três cmdlets, Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster, para que o cliente possa fornecer a ID do aplicativo da entidade de serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7d4ac-244">O Microsoft.Azure.Management.HDInsight foi alterado de 2.1.0 para 5.1.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7d4ac-245">Cinco cmdlets removidos:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7d4ac-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7d4ac-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7d4ac-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7d4ac-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7d4ac-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7d4ac-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7d4ac-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7d4ac-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7d4ac-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7d4ac-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7d4ac-251">Três cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="7d4ac-252">Get-AzHDInsightMonitoring para substituir Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7d4ac-253">Enable-AzHDInsightMonitoring para substituir Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7d4ac-254">Disable-AzHDInsightMonitoring para substituir Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7d4ac-255">Cmdlet Get-AzHDInsightProperties corrigido para dar suporte à obtenção de informações de funcionalidades de um local específico.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7d4ac-256">Conjuntos de parâmetros removidos (' Spark1', 'Spark2') de Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7d4ac-257">Adicionar exemplos aos documentos de ajuda do cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7d4ac-258">O Tipo de saída dos seguintes cmdlets foi alterado:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7d4ac-259">O tipo de saída de Get-AzHDInsightProperties foi alterado de CapabilitiesResponse para AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7d4ac-260">O tipo de saída Remove-AzHDInsightCluster foi alterado de ClusterGetResponse para bool.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7d4ac-261">O tipo de saída Set-AzHDInsightGatewaySettings HttpConnectivitySettings foi alterado para GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7d4ac-262">Alguns casos de teste de cenário foram adicionados.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="7d4ac-263">Remover alguns alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d4ac-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-264">Az.IotHub</span></span>
* <span data-ttu-id="7d4ac-265">Alterações da falha:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-265">Breaking changes:</span></span>
    - <span data-ttu-id="7d4ac-266">O cmdlet 'Add-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7d4ac-267">O conjunto de parâmetros ' __AllParameterSets' para o cmdlet 'Add-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7d4ac-268">O cmdlet 'Get-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7d4ac-269">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Get-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7d4ac-270">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7d4ac-271">A propriedade 'OperationsMonitoringProperties' do tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' foi removida.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7d4ac-272">O cmdlet 'New-AzIotHubExportDevice' não é mais compatível com o alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7d4ac-273">O cmdlet 'New-AzIotHubImportDevice' não é mais compatível com o alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7d4ac-274">O cmdlet 'Remove-AzIotHubEventHubConsumerGroup' não é mais compatível com o parâmetro 'EventHubEndpointName' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7d4ac-275">O conjunto de parâmetros '__AllParameterSets' para o cmdlet 'Remove-AzIotHubEventHubConsumerGroup' foi removido.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7d4ac-276">O cmdlet 'Set-AzIotHub ' não é mais compatível com o parâmetro 'OperationsMonitoringProperties' e nenhum alias foi encontrado para o nome do parâmetro original.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7d4ac-277">O conjunto de parâmetros 'UpdateOperationsMonitoringProperties' para o cmdlet 'Set-AzIotHub' foi removido.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-279">Suporte do Azure Site Recovery para configurar recursos de rede como NSG (grupo de segurança de rede), IP público e balanceadores internos de carga de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7d4ac-280">Suporte do Azure Site Recovery para gravação em discos gerenciados para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7d4ac-281">Suporte do Azure Site Recovery para redução de NIC para vMWare no Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7d4ac-282">Suporte do Azure Site Recovery para rede acelerada do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7d4ac-283">Suporte do Azure Site Recovery para a atualização automática do agente do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7d4ac-284">Suporte do Azure Site Recovery para SSD Standard do Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7d4ac-285">Suporte do Azure Site Recovery para duas passagens do Azure Disk Encryption de Azure para Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7d4ac-286">Suporte do Azure Site Recovery para proteger o disco recém-adicionado do Azure no Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7d4ac-287">Recurso SoftDelete adicionado para VM e testes adicionados para softdelete</span><span class="sxs-lookup"><span data-stu-id="7d4ac-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-288">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-289">Atualize o assembly de dependência Microsoft.Extensions.Caching.Memory de 1.1.1 para 2.2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-290">Az.Network</span></span>
* <span data-ttu-id="7d4ac-291">Altere todos os cmdlets para PrivateEndpointConnection para dar suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7d4ac-292">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="7d4ac-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7d4ac-298">Adicione um novo cmdlet para PrivateLinkResource e ele também dará suporte ao provedor de serviços genérico.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7d4ac-299">Novo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-299">New cmdlet:</span></span>
        - <span data-ttu-id="7d4ac-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7d4ac-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7d4ac-301">Adicionar novos campos e parâmetros para o recurso Protocolo de Proxy V2.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7d4ac-302">Adicionar a propriedade EnableProxyProtocol em PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7d4ac-303">Adicionar a propriedade LinkIdentifier em PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7d4ac-304">New-AzPrivateLinkService atualizado para adicionar um novo parâmetro opcional EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7d4ac-305">Corrigir a descrição de parâmetro incorreta na documentação de referência 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7d4ac-306">Novos cmdlets para dar suporte à política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7d4ac-307">Adicionar suporte para o recurso filho RouteTables do VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7d4ac-308">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-308">New cmdlets added:</span></span>
        - <span data-ttu-id="7d4ac-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7d4ac-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7d4ac-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7d4ac-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7d4ac-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7d4ac-314">Adicionar suporte para novas propriedades SKU de VirtualHub e VirtualWANType de VirtualWan</span><span class="sxs-lookup"><span data-stu-id="7d4ac-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7d4ac-315">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7d4ac-316">New-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7d4ac-317">Update-AzVirtualHub: parâmetro SKU adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7d4ac-318">New-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7d4ac-319">Update-AzVirtualWan: parâmetro VirtualWANType adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7d4ac-320">Adicionar suporte para a propriedade EnableInternetSecurity para HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7d4ac-321">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-321">New cmdlets added:</span></span>
        - <span data-ttu-id="7d4ac-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7d4ac-323">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7d4ac-324">New-AzureRmVirtualHubVnetConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7d4ac-325">New-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7d4ac-326">Update-AzureRmVpnConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7d4ac-327">New-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7d4ac-328">Set-AzureRmExpressRouteConnection: parâmetro EnableInternetSecurity adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7d4ac-329">Adicionar suporte para configuração da Política TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="7d4ac-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7d4ac-330">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-330">New cmdlets added:</span></span>
        - <span data-ttu-id="7d4ac-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7d4ac-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7d4ac-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7d4ac-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7d4ac-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7d4ac-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7d4ac-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7d4ac-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7d4ac-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7d4ac-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7d4ac-337">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7d4ac-338">New-AzApplicationGatewayFirewallPolicy: parâmetros PolicySetting e ManagedRule adicionados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7d4ac-339">Suporte adicionado para o operador de correspondência geográfica no CustomRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7d4ac-340">GeoMatch adicionado para o operador no FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="7d4ac-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7d4ac-341">Suporte adicionado para a política de Firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="7d4ac-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7d4ac-342">Cmdlets atualizados com parâmetros opcionais:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7d4ac-343">New-AzApplicationGatewayHttpListener: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7d4ac-344">New-AzApplicationGatewayPathRuleConfig: parâmetros FirewallPolicy e FirewallPolicyId adicionados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7d4ac-345">Corrigir a sub-rede necessária com o nome AzureBastionSubnet em 'PSBastion' pode não diferenciar maiúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7d4ac-346">Suporte para FQDNs de destino em Regras de Rede e FQDN Traduzido em Regras NAT para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7d4ac-347">Adicionar suporte para os recursos de nível superior RouteTables do IpGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7d4ac-348">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-348">New cmdlets added:</span></span>
        - <span data-ttu-id="7d4ac-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="7d4ac-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7d4ac-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7d4ac-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-354">Remova o cmdlet Add-AzServiceFabricApplicationCertificate, pois esse cenário é coberto por Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-355">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-356">Suporte adicionado para restauração de bancos de dados descartados em Instâncias Gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7d4ac-357">Preterido dos cmdlets de auditoria antiga de código.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7d4ac-358">Foram removidos os aliases preteridos:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7d4ac-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation como alternativa)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7d4ac-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint como alternativa)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7d4ac-361">Remover o cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7d4ac-362">Remover aliases dos cmdlets de configurações de avaliação de vulnerabilidade preteridos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7d4ac-363">Substituir os cmdlets de configurações de detecção avançada de ameaças</span><span class="sxs-lookup"><span data-stu-id="7d4ac-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="7d4ac-364">Adicionar cmdlets para desabilitar e habilitar recomendações confidenciais em colunas em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-365">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-366">O suporte habilita o compartilhamento de arquivos grandes ao criar ou atualizar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7d4ac-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7d4ac-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7d4ac-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7d4ac-369">Ao fechar/obter o identificador de arquivo, ignore verificar se o caminho de entrada for um diretório de arquivo ou um arquivo para evitar falha com o objeto no status DeletePending</span><span class="sxs-lookup"><span data-stu-id="7d4ac-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7d4ac-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7d4ac-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7d4ac-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7d4ac-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="7d4ac-372">2.8.0 – outubro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7d4ac-373">Geral</span><span class="sxs-lookup"><span data-stu-id="7d4ac-373">General</span></span>
* <span data-ttu-id="7d4ac-374">Az.HealthcareApis versão 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-375">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-376">Atualizar a telemetria e a regravação de URL para módulos gerados, corrigir testes de unidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7d4ac-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-377">Az.ApiManagement</span></span>
* <span data-ttu-id="7d4ac-378">**Set-AzApiManagementApi** – Adição de suporte para atualizar a API para ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7d4ac-379">Correção do problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="7d4ac-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-380">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-381">Correção do cmdlet New-AzureAutomationSoftwareUpdateConfiguration para o parâmetro de configuração de reinicialização do Linux.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="7d4ac-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7d4ac-382">Az.Batch</span></span>
* <span data-ttu-id="7d4ac-383">**Get-AzBatchNodeAgentSku** está preterido e será substituído por **Get-AzBatchSupportImage** na versão 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-384">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-385">Adicionar os parâmetros Priority, EvictionPolicy e MaxPrice aos cmdlets New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7d4ac-386">Corrigir mensagem de aviso e documento de ajuda para cmdlets Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="7d4ac-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7d4ac-387">Corrigir a exceção -skipVmBackup para VMs Linux VMs com discos gerenciados para Set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="7d4ac-388">Corrigir o bug nas configurações de criptografia de atualização em Set-AzVMDiskEncryptionExtension, cenário de dupla aprovação.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-389">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-390">Adição de comandos CRUD para o fluxo de dados do ADF V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7d4ac-391">Adição de comandos de ação para a sessão de depuração do fluxo de dados do ADF V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7d4ac-392">Atualizar a versão do SDK do .NET do ADF para 4.2.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-394">Corrigir a validação de conta para que contas com '-' possam ser aprovadas sem domínio</span><span class="sxs-lookup"><span data-stu-id="7d4ac-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7d4ac-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7d4ac-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="7d4ac-396">Atualização da versão do PowerShell para 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7d4ac-397">Atualização da versão do SDK para 1.0.2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7d4ac-398">Atualizar em testes para referir-se à nova versão do SDK</span><span class="sxs-lookup"><span data-stu-id="7d4ac-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7d4ac-399">Atualização da estrutura de saída de aninhada para nivelada.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d4ac-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-400">Az.IotHub</span></span>
* <span data-ttu-id="7d4ac-401">Adicionar nova fonte de roteamento: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="7d4ac-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7d4ac-402">Correção de bug secundária: Get-AzIothub não está retornando subscriptionId</span><span class="sxs-lookup"><span data-stu-id="7d4ac-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="7d4ac-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-403">Az.Monitor</span></span>
* <span data-ttu-id="7d4ac-404">Novos receptores do grupo de ações adicionados ao grupo de ações   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="7d4ac-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7d4ac-405">Usar esquema de alerta comum habilitado para os receptores.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7d4ac-406">Isso não se aplica a SMS, Push de aplicativos do Azure, ITSM e Receptores de voz</span><span class="sxs-lookup"><span data-stu-id="7d4ac-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7d4ac-407">Agora o Webhooks dá suporte à autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-408">Az.Network</span></span>
* <span data-ttu-id="7d4ac-409">Adicionar um novo cmdlet Get-AzAvailableServiceAlias que pode ser chamado para obter os aliases que podem ser usados para Políticas de Ponto de Extremidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7d4ac-410">Adição de suporte dos seletores de tráfego de adição a Conexões de Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="7d4ac-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7d4ac-411">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-411">New cmdlets added:</span></span>
        - <span data-ttu-id="7d4ac-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7d4ac-413">Atualização de cmdlets com o parâmetro opcional -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7d4ac-414">Adicionar suporte para os protocolos ESP e AH em configurações da regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="7d4ac-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7d4ac-415">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="7d4ac-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7d4ac-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7d4ac-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7d4ac-419">Melhorar o tratamento de exceções em cmdlets Cortex</span><span class="sxs-lookup"><span data-stu-id="7d4ac-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7d4ac-420">Novas gerações e SKUs de VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="7d4ac-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7d4ac-421">Introduzir novas gerações para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7d4ac-422">Introduzir novos SKUs de alta taxa de transferência para VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7d4ac-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7d4ac-423">Az.RedisCache</span></span>
* <span data-ttu-id="7d4ac-424">Atualização da documentação de referência 'Set-AzRedisCache' para incluir valores ausentes para o parâmetro '-Size'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-425">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-426">Adicionar suporte para configurar o Administrador do Active Directory na Instância Gerenciada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-427">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-428">Atualizar a Biblioteca de Clientes de Armazenamento para 11.1.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7d4ac-429">Listar contêineres com a API do Plano de gerenciamento, serão listados com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="7d4ac-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7d4ac-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7d4ac-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7d4ac-431">Listar contas de armazenamento com base na assinatura, serão listadas com NextPageLink</span><span class="sxs-lookup"><span data-stu-id="7d4ac-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7d4ac-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7d4ac-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7d4ac-433">Az.StorageSync</span></span>
* <span data-ttu-id="7d4ac-434">Corrigir o Problema 9810 em Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-435">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-436">Set-AzWebApp que atualizava o ASP de um aplicativo estava falhando</span><span class="sxs-lookup"><span data-stu-id="7d4ac-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7d4ac-437">2.7.0 – Setembro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7d4ac-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-438">Az.ApiManagement</span></span>
* <span data-ttu-id="7d4ac-439">Atualizar a descrição do parâmetro '-Format' na documentação de referência do 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7d4ac-440">Remoção das referências do cmdlet preterido 'Update-AzApiManagementDeployment' da documentação de referência.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7d4ac-441">Em vez disso, use 'Set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-442">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-443">Correção do erro de digitação na documentação de referência do 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7d4ac-444">Inclusão de esclarecimentos sobre a restrição de sistema operacional para o Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="7d4ac-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7d4ac-445">Correção da exceção de referência nula do Start-AzAutomationRunbook para a opção -Wait.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-446">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-447">Inclusão do parâmetro UploadSizeInBytes no New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7d4ac-448">Inclusão do parâmetro Incremental no New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7d4ac-449">Adicione um recurso de máquina virtual de baixa prioridade:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7d4ac-450">Os parâmetros MaxPrice, EvictionPolicy e Priority são adicionados ao New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7d4ac-451">O parâmetro MaxPrice é adicionado aos cmdlets New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7d4ac-452">Correção do problema de referência à VM do cmdlet Get-AzAvailabilitySet quando lista todos os conjuntos de disponibilidade na assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7d4ac-453">Correção da exceção nula para Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7d4ac-454">Correção do método VHD Seek para posição relativa ao final.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7d4ac-455">Correção do problema do UltraSSD para New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-456">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-457">Inclusão de três novos comandos para o ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7d4ac-458">Atualização da versão do SDK do ADF .Net para 4.1.3</span><span class="sxs-lookup"><span data-stu-id="7d4ac-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7d4ac-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7d4ac-459">Az.HDInsight</span></span>
* <span data-ttu-id="7d4ac-460">Chamar as alterações de falha</span><span class="sxs-lookup"><span data-stu-id="7d4ac-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d4ac-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-461">Az.IotHub</span></span>
* <span data-ttu-id="7d4ac-462">Acrescentar compatibilidade para invocar failover de um Hub do IoT para a região de recuperação de desastre emparelhada geograficamente.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7d4ac-463">Acrescentar compatibilidade para gerenciar o enriquecimento de mensagens para um Hub do IoT.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7d4ac-464">Os novos cmdlets são:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-464">New cmdlets are:</span></span>
    - <span data-ttu-id="7d4ac-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7d4ac-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7d4ac-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7d4ac-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7d4ac-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7d4ac-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7d4ac-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7d4ac-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d4ac-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-469">Az.Monitor</span></span>
* <span data-ttu-id="7d4ac-470">Aponta para o SDK mais recente do Monitor, por exemplo, a versão prévia 0.24.1</span><span class="sxs-lookup"><span data-stu-id="7d4ac-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7d4ac-471">Acrescenta alterações não relacionadas à falha aos cmdlets Metrics, por exemplo, a enumeração de unidades é compatível com vários novos valores.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7d4ac-472">São cmdlets somente leitura, então não haveria alteração na entrada deles.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7d4ac-473">A versão de API das solicitações **ActionGroups** agora são de **01/06/2019**, antes, eram de **01/03/2018**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="7d4ac-474">Os testes de cenário foram atualizados para acomodar essa alterar.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7d4ac-475">Os construtores das classes **EmailReceiver** e **WebhookReceiver** têm um novo argumento obrigatório, por exemplo, um valor booliano chamado **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7d4ac-476">No momento, o valor é fixado como **false** para ocultar a alteração da falha dos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7d4ac-477">**OBSERVAÇÃO**: é uma alteração temporária que precisa ser validada pela equipe de Alertas.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7d4ac-478">A ordem dos argumentos do construtor da classe **Source** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7d4ac-479">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7d4ac-480">A ordem dos argumentos do construtor da classe **AlertingAction** (relacionada à classe **ScheduledQueryRuleSource**) foi alterada em relação ao SDK anterior.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7d4ac-481">Com essa alteração, foram necessários dois testes de unidade para a correção: elas foram compiladas, mas não passaram nos testes.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7d4ac-482">Compatibilidade com os critérios de Limite Dinâmico para o alerta de métrica V2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7d4ac-483">New-AzMetricAlertRuleV2Criteria: agora também cria critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="7d4ac-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7d4ac-484">Add-AzMetricAlertRuleV2: agora também aceita critérios de limite dinâmico</span><span class="sxs-lookup"><span data-stu-id="7d4ac-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7d4ac-485">Melhorias nos cmdlets da SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7d4ac-486">Os cmdlets aceitarão o parâmetro 'Location' em ambos os formatos: o local (por exemplo, eastus) ou o nome de exibição do local (por exemplo, Leste dos EUA)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7d4ac-487">Ilustração adequada do parâmetro 'Enabled' nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="7d4ac-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7d4ac-488">Inclusão de exemplos para o parâmetro opcional 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7d4ac-489">Melhoria geral nos arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="7d4ac-489">Overall improved help files</span></span>
* <span data-ttu-id="7d4ac-490">Correção de bug ao determinar o tipo de escopo de 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-491">Az.Network</span></span>
* <span data-ttu-id="7d4ac-492">Correção de exemplo incorreto na documentação de referência do 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="7d4ac-493">Inclusão de observação na documentação de referência do 'Get-AzNetworkWatcherPacketCapture' sobre a recuperação de todas as propriedades para captura de pacote</span><span class="sxs-lookup"><span data-stu-id="7d4ac-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7d4ac-494">Correção do exemplo na documentação de referência do 'Test-AzNetworkWatcherIPFlow' para enumerar as NICs corretamente</span><span class="sxs-lookup"><span data-stu-id="7d4ac-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7d4ac-495">Melhoria da análise de exceção de nuvem para exibir detalhes adicionais, caso eles estejam presentes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7d4ac-496">Melhoria da análise de exceção de nuvem para processar outros tipos de exceção do SDK</span><span class="sxs-lookup"><span data-stu-id="7d4ac-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7d4ac-497">Correção do mapeamento incorreto dos modelos de Regra de Segurança</span><span class="sxs-lookup"><span data-stu-id="7d4ac-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7d4ac-498">Inclusão de propriedades de adaptador de rede para recurso de IP privado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7d4ac-499">Inclusão da propriedade 'PrivateEndpoint' como tipo de PSResourceId para PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d4ac-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7d4ac-500">Inclusão da propriedade 'PrivateLinkConnectionProperties' como tipo de PSIpConfigurationConnectivityInformation para PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7d4ac-501">Inclusão de novo modelo da classe PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7d4ac-502">Inclusão de novo 'mssql' de ApplicationRuleProtocolType para recurso do Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7d4ac-503">Compatibilidade com MultiLink na WAN Virtual</span><span class="sxs-lookup"><span data-stu-id="7d4ac-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7d4ac-504">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7d4ac-504">New cmdlets</span></span>
        - <span data-ttu-id="7d4ac-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="7d4ac-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7d4ac-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7d4ac-507">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="7d4ac-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7d4ac-508">New-VpnSite</span></span>
        - <span data-ttu-id="7d4ac-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="7d4ac-509">Update-VpnSite</span></span>
        - <span data-ttu-id="7d4ac-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-510">New-VpnConnection</span></span>
        - <span data-ttu-id="7d4ac-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-511">Update-VpnConnection</span></span>
* <span data-ttu-id="7d4ac-512">Correção de documentos de alguns exemplos do PowerShell para usar cmdlets do Az em vez dos cmdlets do AzureRM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-514">Atualização do objeto AzureVMpolicy com o atributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7d4ac-515">Inclusão de testes de política de VM e restauração de conta de armazenamento original</span><span class="sxs-lookup"><span data-stu-id="7d4ac-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-516">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-517">Correção de bug em que New-AzRoleAssignment não podia ser chamado sem o parâmetro Scope.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-519">Correção de erro de digitação na documentação de referência de 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7d4ac-520">Inclusão de novos cmdlets para gerenciar aplicativos e serviços:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7d4ac-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7d4ac-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7d4ac-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7d4ac-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7d4ac-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7d4ac-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7d4ac-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7d4ac-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7d4ac-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7d4ac-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7d4ac-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7d4ac-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7d4ac-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7d4ac-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7d4ac-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7d4ac-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7d4ac-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="7d4ac-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7d4ac-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7d4ac-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7d4ac-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="7d4ac-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7d4ac-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="7d4ac-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7d4ac-534">Atualização do SDK do Service Fabric para a versão 1.2.0, que usa a versão de API de 01/03/2019 do provedor de recursos do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7d4ac-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7d4ac-535">Az.SignalR</span></span>
* <span data-ttu-id="7d4ac-536">Inclusão dos cmdlets Update, Restart, CheckNameAvailability e GetUsage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-537">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-538">Atualização do exemplo na documentação de referência do 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7d4ac-539">Inclusão de um exemplo do vCore para criar um pool elástico (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7d4ac-540">Remoção da validação de EmailAddresses e confirmação de que EmailAdmins não é false caso EmailAddresses esteja vazio em Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7d4ac-541">Habilitação da remoção das configurações de auditoria de servidor/banco de dados quando houver várias configurações de diagnóstico que habilitam uma categoria de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7d4ac-542">Correção da validação de endereços de email em vários cmdlets de Avaliação de Vulnerabilidade do SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-543">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-544">Atualização do exemplo na documentação de referência do 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7d4ac-545">No upload/download de arquivo do Azure, compatibilidade com a preservação das propriedades SMB do arquivo de origem (atributos, hora de criação, última gravação do arquivo) no arquivo de destino</span><span class="sxs-lookup"><span data-stu-id="7d4ac-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7d4ac-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7d4ac-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7d4ac-548">Correção do upload de blob de blocos com falha de propriedades/metadados no ImmutabilityPolicy habilitado para contêiner.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7d4ac-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7d4ac-550">Compatibilidade com o gerenciamento de compartilhamento de arquivos do Azure com a API de Plano de Gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7d4ac-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7d4ac-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7d4ac-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7d4ac-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7d4ac-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7d4ac-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7d4ac-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7d4ac-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="7d4ac-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-555">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-556">Correção de um problema em que as tags do aplicativo Web eram excluídas quando o aplicativo era migrado para novo ASP</span><span class="sxs-lookup"><span data-stu-id="7d4ac-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7d4ac-557">Correção do Publish-AzureWebapp para funcionar no Linux e no Windows</span><span class="sxs-lookup"><span data-stu-id="7d4ac-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7d4ac-558">Atualização do exemplo na documentação de referência do 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7d4ac-559">2.6.0 – Agosto de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7d4ac-560">Geral</span><span class="sxs-lookup"><span data-stu-id="7d4ac-560">General</span></span>
* <span data-ttu-id="7d4ac-561">Correção de erros de digitação diversos em vários módulos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-562">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-563">Dar suporte ao MSI atribuído pelo usuário na Autenticação do Azure Functions (Nº 9479)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7d4ac-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7d4ac-564">Az.Aks</span></span>
* <span data-ttu-id="7d4ac-565">Corrigir problema com a saída de 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7d4ac-566">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="7d4ac-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7d4ac-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-567">Az.ApiManagement</span></span>
* <span data-ttu-id="7d4ac-568">Correção do problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="7d4ac-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7d4ac-569">Atualizar a versão do nuget do .Net, que não impõe restrições em productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="7d4ac-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7d4ac-570">**Get-AzApiManagementProduct** – Adição de suporte para consultar produtos usando a API.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7d4ac-571">**New-AzApiManagementApiRevision** – Correção de um problema em que ApiRevisionDescription não estava sendo definido ao criar a revisão de API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="7d4ac-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7d4ac-572">Correção de um erro de digitação no modelo 'PsApiManagementOAuth2AuthrozationServer' para 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7d4ac-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7d4ac-573">Az.Batch</span></span>
* <span data-ttu-id="7d4ac-574">Correção de um erro de digitação na mensagem e na documentação de ajuda para grafar Windows com maiúscula</span><span class="sxs-lookup"><span data-stu-id="7d4ac-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d4ac-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d4ac-575">Az.Cdn</span></span>
* <span data-ttu-id="7d4ac-576">Correção de um erro de digitação no auxiliar de conversão do módulo CDN</span><span class="sxs-lookup"><span data-stu-id="7d4ac-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-577">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-578">Adicionar VmssId ao cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7d4ac-579">Adicionar parâmetros TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7d4ac-580">Adicionar a propriedade HyperVGeneration ao objeto de imagem da VM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7d4ac-581">Adicionar os recursos Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7d4ac-582">Novos cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7d4ac-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7d4ac-583">O parâmetro HostId foi adicionado a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7d4ac-584">Atualizar exemplo na documentação 'Invoke-AzVMRunCommand' para usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="7d4ac-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7d4ac-585">Atualizar a descrição '-VolumeType' na documentação de referência 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-586">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-587">Corrigir erro de digitação para grafar 'Windows' com maiúscula na documentação 'New-AzDataFactoryEncryptValue'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7d4ac-588">Atualização para a versão 4.1.2 do SDK do ADF .Net</span><span class="sxs-lookup"><span data-stu-id="7d4ac-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7d4ac-589">Adicionar o parâmetro 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' para o cmd 'Set-AzureRmDataFactoryV2IntegrationRuntime' habilitar a configuração do runtime de integração auto-hospedada como um proxy do SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="7d4ac-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7d4ac-590">Atualização de PSTriggerRun para mostrar pipelines, mensagens e propriedades disparados e de PSActivityRun para mostrar o tipo de atividade</span><span class="sxs-lookup"><span data-stu-id="7d4ac-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-592">Corrigir o deslocamento de Get-DataLakeStoreDeletedItem para erros ou exceções remotas.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d4ac-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-593">Az.EventHub</span></span>
* <span data-ttu-id="7d4ac-594">Correção do problema Nº 9658: Parâmetro VirtualNteworkRule de erro de digitação em Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7d4ac-595">Correção do problema Nº 9558: Set-AzEventHubNamespace está usando PATCH em vez de PUT</span><span class="sxs-lookup"><span data-stu-id="7d4ac-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7d4ac-596">adição do parâmetro EnableKafka para o cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7d4ac-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7d4ac-597">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="7d4ac-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7d4ac-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7d4ac-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7d4ac-599">Correção de erro de digitação do documento em que “Azure” estava escrito inteiramente em letras minúsculas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d4ac-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-600">Az.Monitor</span></span>
* <span data-ttu-id="7d4ac-601">Correção de nomes de parâmetro incorretos na documentação de ajuda</span><span class="sxs-lookup"><span data-stu-id="7d4ac-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-602">Az.Network</span></span>
* <span data-ttu-id="7d4ac-603">Atualização de New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7d4ac-604">Preterição do parâmetro ‘PublicIpAddress’, uma vez que ele nunca foi usado no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7d4ac-605">Adição de um parâmetro opcional 'Primary' que indica se a configuração de IP atual é primária ou não.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7d4ac-606">Melhoria do tratamento de exceção de erro de solicitação do SDK   – Corrige o problema que anteriormente exceções do SDK não eram manipuladas corretamente, o que resultava na não exibição de detalhes de erro de chave</span><span class="sxs-lookup"><span data-stu-id="7d4ac-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7d4ac-607">Ajuste da lógica de validação do Prefixo de IP Ipv6 para verificar o comprimento correto do prefixo IPv6.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="7d4ac-608">Atualização de Get-AzVirtualNetworkSubnetConfig: adição de um conjunto de parâmetros a serem obtidos pela ID de recurso de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7d4ac-609">Atualização da descrição do parâmetro Location para AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="7d4ac-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d4ac-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d4ac-611">Atualização da documentação de 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7d4ac-612">Adição de exemplo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-612">Added example</span></span>
    - <span data-ttu-id="7d4ac-613">Atualização da descrição do parâmetro '-Name'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7d4ac-614">Adição de um exemplo para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7d4ac-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7d4ac-615">Alteração da descrição do parâmetro -Name para New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7d4ac-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-617">Atualizar 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-618">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-619">Adicionar suporte para a nova versão da API 2019-05-10 para Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="7d4ac-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7d4ac-620">Adicionar suporte para 'copy.count = 0' para variáveis, recursos e propriedades</span><span class="sxs-lookup"><span data-stu-id="7d4ac-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7d4ac-621">Os recursos com 'condition = false' ou 'copy.count = 0' serão excluídos no modo completo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7d4ac-622">Adicionar um exemplo de política de atribuição no nível da assinatura ao documento de ajuda</span><span class="sxs-lookup"><span data-stu-id="7d4ac-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7d4ac-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-623">Az.ServiceBus</span></span>
* <span data-ttu-id="7d4ac-624">Correção do problema Nº 9658: Parâmetro VirtualNetworkRule de erro de digitação em Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7d4ac-625">Correção do problema Nº 9786: não foi possível criar uma regra com direitos somente de escuta</span><span class="sxs-lookup"><span data-stu-id="7d4ac-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7d4ac-626">Adição do novo comando 'Test-AzServiceBusNameAvailability' para verificar a disponibilidade do nome da fila e do tópico</span><span class="sxs-lookup"><span data-stu-id="7d4ac-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-628">Corrigir bugs de cmdlet do tipo de nó de adição:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7d4ac-629">bug NullReferenceException quando o grupo de recursos tinha outros vmss não relacionados ao cluster do Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7d4ac-630">Corrige o problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="7d4ac-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7d4ac-631">Corrigir o bug em que o cmdlet falhava se virtualNetwork estivesse em um grupo de recursos diferente do cluster.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7d4ac-632">corrige o problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="7d4ac-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7d4ac-633">Preterição do cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="7d4ac-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-634">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-635">Atualizar a documentação dos antigos cmdlets de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-636">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-637">Atualizar a ajuda para Get/Close-AzStorageFileHandle adicionando mais cenários a exemplos de cmdlet e atualizando descrições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d4ac-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7d4ac-638">Dar suporte a StandardBlobTier em blob de upload e de cópia</span><span class="sxs-lookup"><span data-stu-id="7d4ac-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7d4ac-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7d4ac-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7d4ac-641">Dar suporte à Prioridade de Reidratação no blob de cópia</span><span class="sxs-lookup"><span data-stu-id="7d4ac-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7d4ac-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-643">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-644">Adicionar esclarecimento sobre o parâmetro -AppSettings em Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7d4ac-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7d4ac-645">2.5.0 – julho de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-646">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-647">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7d4ac-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7d4ac-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7d4ac-649">Corrigir exemplo de erros de digitação na documentação 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-650">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-651">Corrigir erros de digitação na cadeia de recursos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d4ac-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d4ac-653">Suporte a NetworkRuleSet adicionado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-654">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-655">Adicionar propriedades ausentes (ComputerName, OsName, OsVersion e HyperVGeneration) de objeto de exibição da instância de VM.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7d4ac-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7d4ac-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7d4ac-657">Corrigir erros de digitação no Remove-AzContainerRegistryReplication para o parâmetro de replicação</span><span class="sxs-lookup"><span data-stu-id="7d4ac-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7d4ac-658">Mais informações podem ser obtidas aqui https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="7d4ac-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-659">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-660">Versão do SDK do ADF .Net para 4.1.0 atualizada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7d4ac-661">Corrigir erros de digitação na documentação de ‘Get-AzDataFactoryV2PipelineRun’</span><span class="sxs-lookup"><span data-stu-id="7d4ac-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d4ac-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-662">Az.EventHub</span></span>
* <span data-ttu-id="7d4ac-663">Novo cmmdlet adicionado para gerar o token SAS: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7d4ac-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7d4ac-664">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="7d4ac-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7d4ac-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d4ac-665">Az.KeyVault</span></span>
* <span data-ttu-id="7d4ac-666">Suporte adicionado para especificar o KeySize para Políticas de Certificado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7d4ac-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7d4ac-667">Az.LogicApp</span></span>
* <span data-ttu-id="7d4ac-668">Correção para Get-AzIntegrationAccountMap para listar todos os tipos de mapa</span><span class="sxs-lookup"><span data-stu-id="7d4ac-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7d4ac-669">Novo parâmetro MapType adicionado para filtragem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7d4ac-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-670">Az.ManagedServices</span></span>
* <span data-ttu-id="7d4ac-671">Suporte adicionado para a versão da API 2019-06-01 (GA)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-672">Az.Network</span></span>
* <span data-ttu-id="7d4ac-673">Adicionar suporte para ponto de extremidade e serviço de link privados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7d4ac-674">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7d4ac-674">New cmdlets</span></span>
        - <span data-ttu-id="7d4ac-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d4ac-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7d4ac-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7d4ac-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7d4ac-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="7d4ac-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7d4ac-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7d4ac-683">Atualizados os comandos para o recurso a seguir: Sinalizador PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies na sub-rede no Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="7d4ac-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7d4ac-684">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig atualizado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7d4ac-685">Inclusão do parâmetro opcional -PrivateEndpointNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no ponto de extremidade privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7d4ac-686">Inclusão do parâmetro opcional -PrivateLinkServiceNetworkPoliciesFlag que habilita ou desabilita a aplicação de políticas de rede no serviço de link privado da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7d4ac-687">O parâmetro de cmdlet 'ServiceName' de AzPrivateLinkService foi renomeado para ‘Name’ com um alias ‘ServiceName’ para compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="7d4ac-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7d4ac-688">Habilitar protocolo ICMP para configurações de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="7d4ac-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7d4ac-689">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-689">Updated cmdlets</span></span>
        - <span data-ttu-id="7d4ac-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7d4ac-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7d4ac-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7d4ac-693">Adicionar ConnectionProtocolType (Ikev1/Ikev2) como um parâmetro configurável de New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7d4ac-694">Adicionar PrivateIpAddressVersion em LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7d4ac-695">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="7d4ac-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7d4ac-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7d4ac-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7d4ac-699">Atualização do comando New-AzApplicationGatewayProbeConfig do Gateway de Aplicativo para dar suporte à porta personalizada na Investigação</span><span class="sxs-lookup"><span data-stu-id="7d4ac-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7d4ac-700">New-AzApplicationGatewayProbeConfig atualizado: Parâmetro opcional Port adicionado que é usado para investigar o servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7d4ac-701">Esse parâmetro é aplicável para Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d4ac-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d4ac-703">A versão padrão atualizada para pesquisas salvas é 1.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="7d4ac-704">Manipulação regex nula de log personalizado corrigida</span><span class="sxs-lookup"><span data-stu-id="7d4ac-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-706">Atualizar 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7d4ac-707">Atualizar 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7d4ac-708">Atualizar 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7d4ac-709">Atualizar 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7d4ac-710">Atualizar 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7d4ac-711">Atualizar 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7d4ac-712">Atualizar 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7d4ac-713">Atualizar 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7d4ac-714">Chamada de serviço atualizada para cancelar o registro do contêiner para o Compartilhamento de Arquivo do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7d4ac-715">Atualizar 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-716">Az.Resources</span></span>
- <span data-ttu-id="7d4ac-717">Remover cmdlet ausente referenciado na documentação 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7d4ac-718">Cmdlets de política atualizados para usar a nova versão da api 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7d4ac-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7d4ac-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-719">Az.ServiceBus</span></span>
* <span data-ttu-id="7d4ac-720">Novo cmmdlet adicionado para gerar o token SAS: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="7d4ac-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7d4ac-721">verificação e mensagem de erro adicionadas para direitos de authorizationrules se apenas 'Manage' for atribuído</span><span class="sxs-lookup"><span data-stu-id="7d4ac-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-722">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-723">Corrigir exemplos ausentes para o cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="7d4ac-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7d4ac-724">Corrigir verificações recorrentes de Avaliação de Vulnerabilidade definida sem fornecer endereços de email</span><span class="sxs-lookup"><span data-stu-id="7d4ac-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7d4ac-725">Corrigir um pequeno erro de digitação em uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-726">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-727">Atualizar exemplo na documentação de referência para ‘Get-AzStorageAccount’ usar o nome de parâmetro correto</span><span class="sxs-lookup"><span data-stu-id="7d4ac-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7d4ac-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7d4ac-728">Az.StorageSync</span></span>
* <span data-ttu-id="7d4ac-729">Adicionar o cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7d4ac-730">Corrigir o problema 9551 para honrar TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="7d4ac-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-731">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-732">Corrigir um bug em que algumas propriedades SiteConfig não foram retornadas por Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d4ac-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7d4ac-733">Adiciona um novo parâmetro Location a Get-AzDeletedWebApp e a Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="7d4ac-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7d4ac-734">Corrige um bug com a clonagem de slots de aplicativo Web usando New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="7d4ac-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7d4ac-735">2.4.0 – Julho de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-736">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-737">Adição de suporte para cmdlets de perfil</span><span class="sxs-lookup"><span data-stu-id="7d4ac-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7d4ac-738">Adição de suporte para ambientes e planos de dados nos cmdlets gerados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7d4ac-739">Correção de bug em que o ponto de extremidade incorreto estava sendo usado em alguns casos para os cmdlets do plano de dados no Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7d4ac-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7d4ac-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-740">Az.Advisor</span></span>
* <span data-ttu-id="7d4ac-741">Versão de GA do Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7d4ac-742">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7d4ac-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-743">Az.ApiManagement</span></span>
* <span data-ttu-id="7d4ac-744">Correção do problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="7d4ac-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7d4ac-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7d4ac-746">Adicionado suporte para consultar as assinaturas por usuário e produto</span><span class="sxs-lookup"><span data-stu-id="7d4ac-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7d4ac-747">Adicionado suporte para consultar usando o escopo '/', '/apis', '/apis/eco-api'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7d4ac-748">Correção dos problemas https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="7d4ac-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7d4ac-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7d4ac-750">Adicionado suporte para especificar 'ApiVersion' e 'ApiVersionSetId' durante a importação de APIs</span><span class="sxs-lookup"><span data-stu-id="7d4ac-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-751">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-752">Corrigido o bug do cmdlet Set-AzAutomationConnectionFieldValue para manipular o valor da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-753">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-754">Adição do parâmetro HyperVGeneration ao New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-755">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-756">Atualização da saída dos cmdlets do ADF das execuções de atividades, pipeline e gatilho do get para oferecer suporte ao pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7d4ac-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7d4ac-757">Az.EventGrid</span></span>
* <span data-ttu-id="7d4ac-758">Correção de erro de digitação na documentação do 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d4ac-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-759">Az.IotHub</span></span>
* <span data-ttu-id="7d4ac-760">Adição de suporte para regenerar as chaves da política de autorização.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-761">Az.Network</span></span>
* <span data-ttu-id="7d4ac-762">Adicionado 'RoutingPreference' às marcas de IP público</span><span class="sxs-lookup"><span data-stu-id="7d4ac-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7d4ac-763">Melhora dos exemplos da documentação de referência do 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7d4ac-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="7d4ac-765">Correção do problema de referência nula no Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="7d4ac-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7d4ac-766">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="7d4ac-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d4ac-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d4ac-768">Correção do modelo de fonte de dados do CustomLog retornado no Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7d4ac-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-770">Correção do comando get-policy para as VMs de IaaS</span><span class="sxs-lookup"><span data-stu-id="7d4ac-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-771">Az.Resources</span></span>
    - <span data-ttu-id="7d4ac-772">Correção do texto de ajuda do parâmetro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="7d4ac-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7d4ac-773">Adição de suporte a paginação do lado do cliente para o Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="7d4ac-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7d4ac-774">Adição de novos parâmetros em Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="7d4ac-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7d4ac-775">Algumas atualizações de documentos e exemplos para cmdlets do Policy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7d4ac-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-776">Az.ServiceBus</span></span>
* <span data-ttu-id="7d4ac-777">Correção para o problema #4938 – New-AzureRmServiceBusQueue retorna BadRequest ao definir MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-778">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-779">Adição de cmdlets do Grupo de Failover da Instância de versão prévia para versão pública</span><span class="sxs-lookup"><span data-stu-id="7d4ac-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7d4ac-780">Suporte para auditoria do Azure SQL Server\Banco de Dados com novos cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7d4ac-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7d4ac-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7d4ac-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7d4ac-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7d4ac-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7d4ac-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7d4ac-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7d4ac-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7d4ac-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7d4ac-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7d4ac-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7d4ac-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7d4ac-787">Remoção das restrições de email das configurações de avaliação da vulnerabilidade</span><span class="sxs-lookup"><span data-stu-id="7d4ac-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-788">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-789">Alteração de 2 parâmetros, '-IndexDocument' e '-ErrorDocument404Path', de obrigatórios para opcionais no cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7d4ac-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7d4ac-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7d4ac-791">Atualização da ajuda do Get-AzStorageBlobContent adicionando um exemplo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7d4ac-792">Mostrar mais informações do erro quando houver falha no cmdlet com o erro StorageException</span><span class="sxs-lookup"><span data-stu-id="7d4ac-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7d4ac-793">Suporte para criação ou atualização da conta de armazenamento com a autenticação de DS do AAD dos Arquivos do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7d4ac-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7d4ac-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7d4ac-796">Suporte para lista ou identificadores de arquivos de fechamento de um compartilhamento de arquivo, um diretório de arquivo ou um arquivo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7d4ac-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7d4ac-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7d4ac-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7d4ac-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7d4ac-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7d4ac-799">Az.StorageSync</span></span>
* <span data-ttu-id="7d4ac-800">Agora esse módulo está incluído como parte do módulo `Az` de rollup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7d4ac-801">2.3.2 – Junho de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-802">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-803">Correção de bug com URL incorreta usada em alguns casos para chamadas do Functions</span><span class="sxs-lookup"><span data-stu-id="7d4ac-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7d4ac-804">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="7d4ac-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7d4ac-805">Correção de problema com aliases do AzureRM para cmdlets do Az</span><span class="sxs-lookup"><span data-stu-id="7d4ac-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7d4ac-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7d4ac-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7d4ac-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="7d4ac-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-808">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-809">Os conjuntos de parâmetros simples New-AzVm e New-AzVmss agora aceitam o parâmetro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7d4ac-810">Correção de erro de digitação na documentação de referência 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7d4ac-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7d4ac-811">Az.Dns</span></span>
* <span data-ttu-id="7d4ac-812">Corrigido erro de digitação nos exemplos de ajuda 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7d4ac-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7d4ac-813">Az.EventGrid</span></span>
* <span data-ttu-id="7d4ac-814">Atualização para usar a versão de API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7d4ac-815">Novos cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-815">New cmdlets:</span></span>
    - <span data-ttu-id="7d4ac-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7d4ac-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7d4ac-817">Cria um novo Domínio na Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7d4ac-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7d4ac-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7d4ac-819">Obtém os detalhes de um Domínio da Grade de Eventos ou obtém uma lista com todos os Domínios da Grade de Eventos da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7d4ac-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7d4ac-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7d4ac-821">Remove um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7d4ac-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7d4ac-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7d4ac-823">Regenera a chave de acesso compartilhada para um Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7d4ac-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7d4ac-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7d4ac-825">Obtém as chaves de acesso compartilhadas usadas para publicar eventos em um Domínio da Grade de Eventos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7d4ac-826">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7d4ac-827">Cria um novo Tópico de Domínio da Grade de Eventos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7d4ac-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7d4ac-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7d4ac-829">Obtém os detalhes de um Tópico de Domínio da Grade de Eventos ou obtém uma lista com todos os Tópicos de Domínio da Grade de Eventos em um Domínio específico da Grade de Eventos do Azure atual</span><span class="sxs-lookup"><span data-stu-id="7d4ac-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="7d4ac-830">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7d4ac-831">Remove um Tópico de Domínio da Grade de Eventos do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7d4ac-832">Cmdlets atualizados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="7d4ac-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7d4ac-834">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o novo Domínio da Grade de Eventos e Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma nova assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7d4ac-835">Adição de novos parâmetros obrigatórios para especificar o novo nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a criação de uma assinatura de evento sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7d4ac-836">Adição de novos conjuntos de parâmetros para domínios e tópicos de domínio a fim de permitir a reutilização de parâmetros existentes (por exemplo, EndPointType, SubjectBeginsWith etc.).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7d4ac-837">Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7d4ac-838">Data de validade da assinatura de evento,</span><span class="sxs-lookup"><span data-stu-id="7d4ac-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7d4ac-839">Parâmetros de filtragem avançada.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7d4ac-840">Adição de nova enumeração para o servicebusqueue como destino.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7d4ac-841">Cancelamento da permissão para uso de 'Todos' na opção -IncludedEventType e substituição por</span><span class="sxs-lookup"><span data-stu-id="7d4ac-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="7d4ac-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7d4ac-843">Adição de novos parâmetros opcionais (Top, ODataQuery and NextLink) para dar suporte à paginação e filtragem dos resultados.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7d4ac-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7d4ac-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7d4ac-845">Adição de novos parâmetros obrigatórios para dar suporte ao redirecionamento para o Domínio da Grade de Eventos e o Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7d4ac-846">Adição de novos parâmetros obrigatórios para especificar o nome do Domínio da Grade de Eventos e/ou do Tópico de Domínio da Grade de Eventos a fim de permitir a remoção de uma assinatura de evento existente sob esses recursos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7d4ac-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-847">Az.FrontDoor</span></span>
* <span data-ttu-id="7d4ac-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7d4ac-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7d4ac-849">Adição de suporte a transformações e do novo valor de preenchimento automático do operador (RegEx)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7d4ac-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7d4ac-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7d4ac-851">Adição de novos valores de preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="7d4ac-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-852">Az.Network</span></span>
* <span data-ttu-id="7d4ac-853">Adição de suporte para o recurso de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7d4ac-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7d4ac-854">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7d4ac-854">New cmdlets</span></span>
        - <span data-ttu-id="7d4ac-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7d4ac-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7d4ac-856">Adição de AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7d4ac-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7d4ac-857">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7d4ac-857">New cmdlets</span></span> 
        - <span data-ttu-id="7d4ac-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7d4ac-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7d4ac-859">Adição de PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7d4ac-860">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7d4ac-860">New cmdlets</span></span> 
        - <span data-ttu-id="7d4ac-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="7d4ac-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7d4ac-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7d4ac-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7d4ac-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7d4ac-866">Adição de PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d4ac-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7d4ac-867">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7d4ac-867">New cmdlets</span></span>
        - <span data-ttu-id="7d4ac-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d4ac-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7d4ac-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d4ac-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7d4ac-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d4ac-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7d4ac-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7d4ac-872">Atualizados os comandos para o recurso a seguir: Sinalizador UseLocalAzureIpAddress em VpnConnection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7d4ac-873">Atualizado New-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7d4ac-874">Atualizado Set-AzVpnConnection: Adicionado o parâmetro opcional -UseLocalAzureIpAddress para indicar que o endereço IP do azure local deve ser usado como endereço de origem ao iniciar a conexão.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7d4ac-875">Adicionado campo somente leitura PeeredConnections no emparelhamento do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7d4ac-876">Adicionado campo somente leitura GlobalReachEnabled no ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7d4ac-877">Adicionado atributo de alteração da falha para chamar a desaprovação do campo AllowGlobalReach no modelo do ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d4ac-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7d4ac-878">Corrigido Problema 8756 Erro ao usar o TargetListenerID com os cmdlets do AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7d4ac-879">Corrigido bug no New-AzApplicationGatewayPathRuleConfig que impedia o conjunto de regras de regeneração de ser definido.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7d4ac-880">Corrigida a exibição do VirtualNetworkTaps no NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7d4ac-881">Corrigidos cmdlets de Get do Cortex para listar todas as partes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7d4ac-882">Corrigida criação de referência do VirtualHub para ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="7d4ac-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7d4ac-883">Adicionado suporte para Zonas de Disponibilidade no AzureFirewall e no NatGateway</span><span class="sxs-lookup"><span data-stu-id="7d4ac-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7d4ac-884">Adicionado o cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="7d4ac-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7d4ac-885">Adição de suporte para vários endereços IP públicos para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7d4ac-886">Atualizado o cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7d4ac-887">Adicionado o parâmetro -PublicIpAddress que aceita um ou mais objetos de Endereço IP Público</span><span class="sxs-lookup"><span data-stu-id="7d4ac-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7d4ac-888">Adicionado o parâmetro -VirtualNetwork que aceita um objeto de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="7d4ac-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7d4ac-889">Adicionados os métodos AddPublicIpAddress e RemovePublicIpAddress no objeto do firewall – eles aceitam um objeto de Endereço IP Público como entrada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7d4ac-890">Preteridos os parâmetros -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7d4ac-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="7d4ac-891">Atualizados os comandos para o recurso a seguir: Definidas as opções de autenticação do VpnClient AAD ao recurso de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="7d4ac-892">New-AzVirtualNetworkGateway atualizado: Adicionados os parâmetros opcionais AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7d4ac-893">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional AadTenantUri, AadAudienceId e AadIssuerUri para definir as opções de autenticação do VPNClient AAD no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7d4ac-894">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro de opção opcional RemoveAadAuthentication para remover as opções de autenticação do VpnClient AAD do Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d4ac-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d4ac-896">Habilitado o tipo de preço **pergb2018** no comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-897">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-898">Suporte para opções adicionais de exportação de modelo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7d4ac-899">Adição do parâmetro '-SkipResourceNameParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7d4ac-900">Adição do parâmetro '-SkipAllParameterization' ao Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7d4ac-901">Adição do parâmetro '-Resource' ao Export-AzResourceGroup para filtragem de recursos exportados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-903">Correção do certificado de adição ByExistingKeyVault que obtinha a impressão digital incorreta em alguns casos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-904">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-905">Correção do sufixo de ponto de extremidade de armazenamento da Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="7d4ac-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7d4ac-906">A correção da habilitação da Segurança de Dados Avançada substitui a política de Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="7d4ac-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7d4ac-907">Novos Cmdlets para o Management.Sql a fim de permitir aos clientes adicionar chaves de TDE e definir o protetor de TDE para instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7d4ac-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7d4ac-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7d4ac-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7d4ac-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7d4ac-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7d4ac-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7d4ac-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7d4ac-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7d4ac-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7d4ac-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-913">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-914">Suporte aos tipos FileStorage e SkuName Premium_ZRS ao criar a conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7d4ac-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7d4ac-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="7d4ac-916">Esclarecida a descrição do cmdlet de imutabilidade de blob</span><span class="sxs-lookup"><span data-stu-id="7d4ac-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7d4ac-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-918">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-919">Otimiza o Get-AzWebAppCertificate para filtrar por grupo de recursos no servidor, em vez do cliente</span><span class="sxs-lookup"><span data-stu-id="7d4ac-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7d4ac-920">Adiciona o parâmetro de opção -UseDisasterRecovery ao Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="7d4ac-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7d4ac-921">2.2.0 – junho de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7d4ac-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d4ac-922">Az.Cdn</span></span>
* <span data-ttu-id="7d4ac-923">Atualização dos cmdlets para dar suporte ao recurso rulesEngine com base na versão de API 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-924">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-925">Adição do parâmetro `NoWait` que inicia a operação e gera o retorno imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7d4ac-926">Cmdlets atualizados:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d4ac-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-927">Az.EventHub</span></span>
* <span data-ttu-id="7d4ac-928">Correção do erro nº 9231 – Get-AzEventHubNamespace não retorna marcas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7d4ac-929">Correção do erro nº 9230 – Get-AzEventHubNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4ac-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-930">Az.Network</span></span>
* <span data-ttu-id="7d4ac-931">Atualização de ResourceId e InputObject para o Gateway do NAT</span><span class="sxs-lookup"><span data-stu-id="7d4ac-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7d4ac-932">Adição de alias a ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="7d4ac-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7d4ac-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="7d4ac-934">Correção do problema de referência nula em Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-936">Alteração do mínimo de retenção em dias da política da IaaSVM de 1 para 7</span><span class="sxs-lookup"><span data-stu-id="7d4ac-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7d4ac-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-937">Az.ServiceBus</span></span>
* <span data-ttu-id="7d4ac-938">Correção do erro nº 9182 – Get-AzServiceBusNamespace retorna ResourceGroup, em vez de ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d4ac-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-940">Correção do erro de digitação na mensagem de erro 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7d4ac-941">Correção do caractere ausente em cmdlines do Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-942">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-943">Adição do parâmetro DnsZonePartner ao cmdlet New-AzureSqlInstance para dar suporte a AutoDr na Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7d4ac-944">Substituição do cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7d4ac-945">Renomeação dos cmdlets de Detecção de Ameaças para Proteção Avançada contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="7d4ac-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7d4ac-946">Os parâmetros New-AzSqlInstance -StorageSizeInGB e -LicenseType agora são opcionais.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-947">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-948">correção do problema em que o uso de Set-AzWebApp e Set-AzWebAppSlot com a propriedade -WebApp removia as marcas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7d4ac-949">2.1.0 – maio de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7d4ac-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-950">Az.ApiManagement</span></span>
* <span data-ttu-id="7d4ac-951">Criação de cmdlets para gerenciar o diagnóstico no escopo global e da API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7d4ac-952">**Get-AzApiManagementDiagnostic** – fazer com que o diagnóstico configure um escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7d4ac-953">**New-AzApiManagementDiagnostic** – criar um diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7d4ac-954">**New-AzApiManagementHttpMessageDiagnostic** – criar a configuração de diagnóstico na qual os cabeçalhos serão registrados em log e o tamanho dos bytes do corpo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7d4ac-955">**New-AzApiManagementPipelineDiagnosticSetting** – criar as configurações de diagnóstico para mensagens HTTP de entrada/saída para o Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7d4ac-956">**New-AzApiManagementSamplingSetting** – criar a configuração de amostragem para as solicitações/a resposta de um diagnóstico</span><span class="sxs-lookup"><span data-stu-id="7d4ac-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7d4ac-957">**Remove-AzApiManagementDiagnostic** – remover uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7d4ac-958">**Set-AzApiManagementDiagnostic** – atualizar uma entidade de diagnóstico no escopo global ou da API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7d4ac-959">Criação de cmdlets para gerenciar o cache no serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7d4ac-960">**Get-AzApiManagementCache** – obter os detalhes do cache especificado pelo identificador ou todos os caches</span><span class="sxs-lookup"><span data-stu-id="7d4ac-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7d4ac-961">**New-AzApiManagementCache** – criar um cache 'padrão' ou um cache em determinada 'região' do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7d4ac-962">**Remove-AzApiManagementCache** – remover um cache</span><span class="sxs-lookup"><span data-stu-id="7d4ac-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7d4ac-963">**Update-AzApiManagementCache** – atualizar um cache</span><span class="sxs-lookup"><span data-stu-id="7d4ac-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7d4ac-964">Criação de cmdlets para gerenciar o esquema da API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7d4ac-965">**New-AzApiManagementSchema** – criar um esquema para uma API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7d4ac-966">**Get-AzApiManagementSchema** – configurar os esquemas na API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7d4ac-967">**Remove-AzApiManagementSchema** – remover o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7d4ac-968">**Set-AzApiManagementSchema** – atualizar o esquema configurado na API</span><span class="sxs-lookup"><span data-stu-id="7d4ac-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7d4ac-969">Criação de um cmdlet para gerar um token de usuário.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="7d4ac-970">**New-AzApiManagementUserToken** – gerar um novo token de usuário válido por 8 horas por padrão. O token para o usuário 'GIT' pode ser gerado usando esse cmdlet./</span><span class="sxs-lookup"><span data-stu-id="7d4ac-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7d4ac-971">Criação de um cmdlet para recuperar o status da rede</span><span class="sxs-lookup"><span data-stu-id="7d4ac-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7d4ac-972">**Get-AzApiManagementNetworkStatus** – obter a conectividade do status da rede de recursos dos quais o serviço Gerenciamento de API depende.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7d4ac-973">Isso é útil ao implantar o serviço ApiManagement em uma Rede Virtual e ao validar se uma das dependências foi desfeita.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7d4ac-974">Atualização do cmdlet **New-AzApiManagement** para gerenciar o serviço ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="7d4ac-975">Adição de suporte para o novo SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7d4ac-976">Adição de suporte para ativar o sinalizador 'EnableClientCertificate' para o SKU de 'Consumo'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7d4ac-977">O novo cmdlet **New-AzApiManagementSslSetting** permite definir a configuração 'TLS/SSL' no 'Backend' e no 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7d4ac-978">Isso também pode ser usado para configurar 'Ciphers' como '3DES' e 'ServerProtocols' como 'Http2' no 'Frontend' de um serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7d4ac-979">Adição de suporte para configurar o nome do host 'DeveloperPortal' no serviço ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7d4ac-980">Atualização dos cmdlets **Get-AzApiManagementSsoToken** para usar o objeto 'PsApiManagement' como entrada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7d4ac-981">Atualização do cmdlet para exibir mensagens de erro embutidas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="7d4ac-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy: Código de erro: ValidationError Mensagem de erro: um ou mais campos contêm valores incorretos: Detalhes do erro: [Code=ValidationError, Message=Erro no elemento 'log-to-eventhub' na linha 3, coluna 10: Agente não encontrado, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7d4ac-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7d4ac-983">Atualização do cmdlet **Export-AzApiManagementApi** para exportar as APIs no formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7d4ac-984">Atualização do cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7d4ac-985">Para importar a API da especificação de documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7d4ac-986">Para substituir a propriedade 'PsApiManagementSchema' especificada em qualquer documento ('Swagger', 'Wadl', 'Wsdl' e 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="7d4ac-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7d4ac-987">Para substituir a propriedade 'ServiceUrl' especificada em qualquer documento.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7d4ac-988">Atualização do cmdlet **Get-AzApiManagementPolicy** para retornar a política no 'formato' não Xml com escape usando 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7d4ac-989">Atualização do cmdlet **Set-AzApiManagementPolicy** para aceitar a política no 'formato' não Xml sem escape usando 'rawxml' e Xml de escape usando 'xml'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7d4ac-990">Atualização do cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="7d4ac-991">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7d4ac-992">Para criar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7d4ac-993">Para clonar uma API usando 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7d4ac-994">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7d4ac-995">Atualização do cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7d4ac-996">Para configurar a API com o servidor de autorização 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7d4ac-997">Para atualizar uma API em um 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="7d4ac-998">Capacidade de configurar 'SubscriptionRequired' no escopo da API.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7d4ac-999">Atualização do cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7d4ac-1000">Para clonar (marcas de cópia, produtos, operações e políticas) uma versão existente usando 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7d4ac-1001">A nova revisão pressupõe o uso da 'ApiId' do pai.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7d4ac-1002">Para fornecer um 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7d4ac-1003">Para substituir a 'ServiceUrl' ao clonar uma API.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7d4ac-1004">Atualização do cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7d4ac-1005">Para configurar 'AAD' ou 'AADB2C' com uma 'Authority'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7d4ac-1006">Para configurar 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7d4ac-1007">Atualização do cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7d4ac-1008">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7d4ac-1009">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7d4ac-1010">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7d4ac-1011">Atualização do cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7d4ac-1012">Para levar em conta o novo SubscriptonModel usando 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7d4ac-1013">Para levar em conta o modelo de assinatura antigo usando 'ProductId' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7d4ac-1014">Adição de suporte para habilitar 'AllowTracing' no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7d4ac-1015">Atualização dos cmdlets a seguir para aceitar 'ResourceId' como entrada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7d4ac-1016">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7d4ac-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7d4ac-1018">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7d4ac-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7d4ac-1020">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7d4ac-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7d4ac-1022">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7d4ac-1023">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7d4ac-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7d4ac-1025">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="7d4ac-1026">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7d4ac-1027">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1028">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1029">Atualização de Get-AzAutomationJobOutputRecord para manipular valores JSON e de registro de texto.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7d4ac-1030">Correção do problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7d4ac-1031">Correção do problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7d4ac-1032">Alteração do comportamento para Start-AzAutomationDscCompilationJob a fim de apenas iniciar o trabalho em vez de aguardar sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7d4ac-1033">Correção do problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7d4ac-1034">Correção para Get-AzAutomationDscNode, em que o uso de -Name retorna todos os nós.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7d4ac-1035">Agora, ele retorna somente o nó correspondente.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1036">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1037">Adição dos parâmetros ProtectFromScaleIn e ProtectFromScaleSetAction ao cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7d4ac-1038">O parâmetro simples New-AzVM agora usa, por padrão, uma localização disponível se não há suporte para a região 'Leste dos EUA'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-1040">Atualização do SDK do ADLS para usar httpclient e integrar o teste do plano de dados com a estrutura do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d4ac-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1041">Az.Monitor</span></span>
* <span data-ttu-id="7d4ac-1042">Correção de nomes de parâmetro incorretos nos exemplos da Ajuda</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1043">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1044">Adição do sinalizador DisableBgpRoutePropagation à saída da tabela de rotas efetivas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7d4ac-1045">Atualização do cmdlet:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="7d4ac-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7d4ac-1047">Correção do traço duplo na documentação de New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1048">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1049">Adição do novo cmdlet Get-AzureRmDenyAssignment para recuperar atribuições de negação</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1050">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1051">Renomeação dos cmdlets de Proteção Avançada contra Ameaças para Segurança de Dados Avançada e habilitação da Avaliação de Vulnerabilidade por padrão</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7d4ac-1052">2.0.0 - maio de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1053">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1054">Atualizar biblioteca de autenticação para corrigir problemas do ADFS com autenticação de nome de usuário/senha</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d4ac-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d4ac-1056">Exiba aviso de isenção de responsabilidade do Bing somente para os Serviços de Pesquisa do Bing.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7d4ac-1057">Corrija o erro quando falha a criação da conta.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1058">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1059">Recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7d4ac-1060">Os seguintes cmdlets novos foram adicionados:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7d4ac-1061">O novo parâmetro ProximityPlacementGroupId é adicionado aos cmdlets a seguir:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7d4ac-1062">O parâmetro StorageAccountType é adicionado ao New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7d4ac-1063">O TargetRegion de New-AzGalleryImageVersion pode conter StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7d4ac-1064">O parâmetro de opção SkipShutdown é adicionado ao Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="7d4ac-1065">Alterações de última hora</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1065">Breaking changes</span></span>
    - <span data-ttu-id="7d4ac-1066">Set-AzVMBootDiagnostics é alterado para Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7d4ac-1067">Export-AzLogAnalyticThrottledRequests é alterado para Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7d4ac-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="7d4ac-1069">Primeira versão disponível dos cmdlets do Gerenciador de Implantação do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7d4ac-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1070">Az.Dns</span></span>
* <span data-ttu-id="7d4ac-1071">Delegação automática de NameServer do DNS</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7d4ac-1072">Crie um cmdlet de zona DNS que aceite o nome da zona pai como parâmetro opcional adicional.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7d4ac-1073">Adicione os registros NS na zona pai para a zona filho recém-criada.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7d4ac-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="7d4ac-1075">Primeira versão disponível dos cmdlets FrontDoor do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7d4ac-1076">Renomear os cmdlets do WAF para incluir 'Waf'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7d4ac-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1077">Az.HDInsight</span></span>
* <span data-ttu-id="7d4ac-1078">Removidos os dois cmdlets:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7d4ac-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7d4ac-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7d4ac-1081">Adicionado um novo cmdlet Set-AzHDInsightGatewayCredential para substituir Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7d4ac-1082">Atualize o cmdlet Get-AzHDInsightJobOutput para distinguir a função de leitor e a função de operador do hdinsight:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7d4ac-1083">Os usuários com função de leitor precisam especificar o parâmetro 'DefaultStorageAccountKey' explicitamente, caso contrário, ocorrerá o erro.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7d4ac-1084">Os usuários com função de operador do HDInsight não serão afetados.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d4ac-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1085">Az.Monitor</span></span>
* <span data-ttu-id="7d4ac-1086">Novos cmdlets para a API SQR (Regra de Consulta Agendada)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="7d4ac-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7d4ac-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7d4ac-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7d4ac-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7d4ac-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7d4ac-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7d4ac-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7d4ac-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7d4ac-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7d4ac-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7d4ac-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7d4ac-1098">[Mais](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informações sobre a API SQR</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7d4ac-1099">Az.Monitor.md atualizado para incluir os cmdlets para a regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1100">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1101">Adicionar suporte para o recurso de Gateway Nat</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7d4ac-1102">Novos cmdlets</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1102">New cmdlets</span></span>
        - <span data-ttu-id="7d4ac-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="7d4ac-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7d4ac-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7d4ac-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7d4ac-1107">Cmdlets atualizados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="7d4ac-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7d4ac-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7d4ac-1110">Atualizados os comandos para o recurso a seguir: Rotas personalizadas definir/remover no Gateway Brooklyn.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7d4ac-1111">New-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7d4ac-1112">Set-AzVirtualNetworkGateway atualizado: Adicionado o parâmetro opcional -CustomRoute para definir os prefixos de endereço como rotas personalizadas a definir no Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7d4ac-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="7d4ac-1114">Suporte para consultar detalhes da avaliação de política.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7d4ac-1115">Adicione o parâmetro '-Expand' ao Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7d4ac-1116">Suporte a '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-1118">Suporte para Assinatura cruzada do Azure do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7d4ac-1119">Marcação das alterações de falhas futuras para o Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7d4ac-1120">Correção de plano de ação final do plano de recuperação do Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7d4ac-1121">Correção de mapeamento de rede de atualização do Azure Site Recovery do Azure para o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7d4ac-1122">Correção de direção de proteção de atualização do Azure Site Recovery do Azure para o Azure para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7d4ac-1123">Outras correções secundárias.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7d4ac-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1124">Az.Relay</span></span>
* <span data-ttu-id="7d4ac-1125">Corrigir erros de digitação nas mensagens voltadas ao cliente</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7d4ac-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="7d4ac-1127">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1128">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-1129">Atualize para a Biblioteca de Clientes de Armazenamento 10.0.1 (o namespace de todos os objetos desse SDK altera de 'Microsoft.WindowsAzure.Storage. *' para 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7d4ac-1130">Atualize para Microsoft.Azure.Management.Storage 11.0.0, para ser compatível com a nova API versão 01-04-2019.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7d4ac-1131">O ‘Kind’ da conta Storage padrão na conta Create Storage alterou de 'Storage' para 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7d4ac-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="7d4ac-1133">Altere a saída do cmdlet da conta Storage Sku.Name para ficar alinhado com a entrada SkuName adicionando '-', como 'StandardLRS' alterado para 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7d4ac-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7d4ac-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7d4ac-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1137">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-1138">A propriedade 'Kind' agora será definida para objetos PSSite retornados por Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7d4ac-1139">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics marcados como preteridos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7d4ac-1140">1.8.0 – abril de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7d4ac-1141">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="7d4ac-1142">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="7d4ac-1143">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7d4ac-1144">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7d4ac-1145">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7d4ac-1146">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d4ac-1147">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1148">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1149">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1150">Atualizar Uninstall-AzureRm para excluir módulos corretamente no Mac</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7d4ac-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1151">Az.Batch</span></span>
* <span data-ttu-id="7d4ac-1152">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d4ac-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1153">Az.Cdn</span></span>
* <span data-ttu-id="7d4ac-1154">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d4ac-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d4ac-1156">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1157">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1158">Corrigir o problema com a instalação do AEM se as IDs do recurso dos discos tiverem grupos de recursos em minúsculas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7d4ac-1159">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d4ac-1160">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1161">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-1162">Adicionar SsisProperties se NodeCount não for nulo para o runtime de integração gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-1164">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7d4ac-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1165">Az.EventGrid</span></span>
* <span data-ttu-id="7d4ac-1166">Atualizado o texto de ajuda do ponto de extremidade para indicar que os recursos devem ser criados antes do uso dos cmdlets de assinatura de evento de criação/atualização.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d4ac-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1167">Az.EventHub</span></span>
* <span data-ttu-id="7d4ac-1168">Novos cmdlets adicionados para serem usados pelo NetworkRuleSet do Namespace</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7d4ac-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1169">Az.HDInsight</span></span>
* <span data-ttu-id="7d4ac-1170">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d4ac-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1171">Az.IotHub</span></span>
* <span data-ttu-id="7d4ac-1172">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7d4ac-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1173">Az.KeyVault</span></span>
* <span data-ttu-id="7d4ac-1174">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d4ac-1175">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7d4ac-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="7d4ac-1177">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7d4ac-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1178">Az.Media</span></span>
* <span data-ttu-id="7d4ac-1179">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d4ac-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1180">Az.Monitor</span></span>
  * <span data-ttu-id="7d4ac-1181">Novos cmdlets para regra de alerta com base em métrica GenV2 (não clássica)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7d4ac-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7d4ac-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7d4ac-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7d4ac-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7d4ac-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7d4ac-1187">SDK do Monitor atualizado para versão 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1188">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1189">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d4ac-1190">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7d4ac-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="7d4ac-1192">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d4ac-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d4ac-1194">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7d4ac-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7d4ac-1196">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-1198">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d4ac-1199">Formato de tabela atualizado para SQL na VM do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7d4ac-1200">Método alternativo adicionado para buscar o local no AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7d4ac-1201">ScheduleRunDays atualizado no objeto SchedulePolicy de acordo com o fuso horário</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7d4ac-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1202">Az.RedisCache</span></span>
* <span data-ttu-id="7d4ac-1203">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1204">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1205">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1206">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1207">Substituir a dependência no SDK do Monitor por código comum</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7d4ac-1208">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d4ac-1209">Processo de classificação de várias colunas aprimorado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7d4ac-1210">Incluir propriedades de SKU (capacidade, família, nome de SKU) na resposta de Get-AzSqlServerServiceObjective e formatar como tabela por padrão.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7d4ac-1211">Capacidade de Get-AzSqlServerServiceObjective por local sem a necessidade de um servidor preexistente na região.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7d4ac-1212">Suporte a parâmetro de fuso horário na criação da Instância Gerenciada.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7d4ac-1213">Corrigir a documentação para caracteres curinga</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1214">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-1215">Corrigir Set-AzWebApp e Set-AzWebAppSlot para que não removam as marcas em execução</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7d4ac-1216">Cmdlets atualizados com substantivos plurais no singular e nomes no plural preteridos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7d4ac-1217">Atualizado o SDK de Sites.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7d4ac-1218">Removida a propriedade AdminSiteName de PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7d4ac-1219">1.7.0 - abril de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7d4ac-1220">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="7d4ac-1221">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="7d4ac-1222">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7d4ac-1223">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7d4ac-1224">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7d4ac-1225">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d4ac-1226">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1227">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1228">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1229">Add-AzEnvironment e Set-AzEnvironment atualizados para aceitar o parâmetro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7d4ac-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="7d4ac-1231">Usando ServiceClient nos cmdlets do plano de dados e removendo a lógica de autenticação original</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7d4ac-1232">Tornando Add-AzureASAccount um wrapper de Connect-AzAccount para evitar uma alteração na falha</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1233">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1234">Corrigido o bug de cmdlet New-AzAutomationSoftwareUpdateConfiguration para inclusões.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7d4ac-1235">Agora os parâmetros IncludedKbNumber e IncludedPackageNameMask devem funcionar.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7d4ac-1236">Correção de bug para o grupo de gerenciamento dinâmico de atualização de automação do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1237">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1238">Adicionar parâmetro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7d4ac-1239">Permitir a criação de VM com a imagem da galeria de outros locatários.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7d4ac-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="7d4ac-1241">Problema corrigido no parâmetro -Command de New-AzContainerGroup que adicionou um argumento vazio à direita</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1242">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-1243">Atualizada a versão do SDK do ADF .NET para 3.0.2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7d4ac-1244">Cmdlet Set-AzDataFactoryV2 atualizado com parâmetros extras para as configurações relacionadas a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1245">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1246">Aperfeiçoar o tratamento de provedores para “Get-AzResource” ao fornecer os parâmetros “-ResourceId” ou “-ResourceGroupName”, “-Name” e “-ResourceType”</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7d4ac-1247">Melhorar o tratamento de erro para 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7d4ac-1248">Controlar erros lançados fora da validação de implantação e incluí-los na saída do comando</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7d4ac-1249">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7d4ac-1250">Adicionar parâmetro do argumento “-IgnoreDynamicParameters” ao conjunto de cmdlets de implantação para ignorar o prompt no script e nos cenários de trabalho</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7d4ac-1251">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1252">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1253">Classificação de Dados no Banco de Dados de Suporte.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1254">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-1255">Relatar detalhes do erro ao criar o contexto de armazenamento com o parâmetro -UseConnectedAccount, mas sem logon na conta do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7d4ac-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="7d4ac-1257">Propriedades do Serviço de Blob de Gerenciamento de Suporte de uma conta de armazenamento especificada com a API do plano de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7d4ac-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7d4ac-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7d4ac-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7d4ac-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7d4ac-1262">Suporte de -AsJob para Blob e cmdlets de upload e download de arquivos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7d4ac-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7d4ac-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7d4ac-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7d4ac-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7d4ac-1267">1.6.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7d4ac-1268">Destaques desde a última versão principal</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="7d4ac-1269">Disponibilidade geral do módulo `Az`</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="7d4ac-1270">Para obter mais informações sobre o módulo `Az`, visite o seguinte: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7d4ac-1271">Recurso de conclusão Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7d4ac-1272">Suporte a caracteres curinga adicionado aos cmdlets Get para Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7d4ac-1273">Autenticação interativa e do nome de usuário/senha adicionada somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d4ac-1274">Suporte adicionado para runbooks do Python 2 em Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1275">Az.LogicApp: Novos cmdlets para os Assemblies da Conta de Integração e da Configuração do Lote</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1276">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1277">Alterar o gerenciamento de atualizações de automação do Azure para dar suporte aos novos recursos a seguir:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7d4ac-1278">Agrupamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="7d4ac-1279">Script de pré-publicação</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1279">Pre-Post script</span></span>
    * <span data-ttu-id="7d4ac-1280">Configuração da Reinicialização</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1281">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1282">Corrigir o problema com resolução de caminho em Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7d4ac-1283">Atualize a biblioteca de clientes de Computação para 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7d4ac-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1284">Az.KeyVault</span></span>
* <span data-ttu-id="7d4ac-1285">Suporte a caracteres curinga adicionado aos cmdlets do KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1286">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1287">Adicionar suporte a Inteligência contra Ameaças para o Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7d4ac-1288">Adicionar recurso superior da Política de Firewall do Gateway de Aplicativo e Regras Personalizadas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-1290">SnapshotRetentionInDays adicionado na política de VM do Azure para dar suporte ao RP instantâneo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7d4ac-1291">Suporte do pipe adicionado para cancelar o registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1292">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1293">Atualizar o suporte a caracteres curinga para Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7d4ac-1294">Atualizar credenciais usadas ao fazer chamadas genéricas para o ARM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1295">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1296">parâmetro dos cmdlets alterado da Detecção de Ameaças (ExcludeDetectionType) do DetectionType para string [], para torná-lo à prova de obsolescência quando novos DetectionTypes forem adicionados e dar suporte ao preenchimento automático também.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1297">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-1298">Suporte para Obter/Definir/Remover Política de Gerenciamento de uma conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7d4ac-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7d4ac-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7d4ac-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7d4ac-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7d4ac-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7d4ac-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1305">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-1306">Corrigir bug do modelo ARM que interrompe a clonagem de todos os slots usando “New-AzWebApp -IncludeSourceWebAppSlots”</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7d4ac-1307">1.5.0 - março de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1308">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1309">Adicionar o comando “Register-AzModule” para dar suporte aos cmdlets gerados pelo AutoRest</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7d4ac-1310">Exemplos de atualização para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1311">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1312">Problema corrigido ao recuperar certas agendas mensais em vários cmdlets da Automação do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7d4ac-1313">Corrigir o Get-AzAutomationDscNode retornando apenas os primeiros 20 nós.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7d4ac-1314">Agora ele retorna todos os nós</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d4ac-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1315">Az.Cdn</span></span>
* <span data-ttu-id="7d4ac-1316">Novos cmdlets do Powershell adicionados para Habilitar/Desabilitar o HTTPS de Domínio Personalizado e preterir os antigos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1317">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1318">Adicionar suporte de caracteres curinga aos cmdlets Get</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1319">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-1320">Versão SDK do ADF .Net atualizada para 3.0.1</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7d4ac-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1321">Az.LogicApp</span></span>
* <span data-ttu-id="7d4ac-1322">Correção para ListWorkflows recuperando apenas a primeira página de resultados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1323">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1324">Adicionar suporte de caracteres curinga aos cmdlets Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-1326">SQL Server adicionado no suporte de VM do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7d4ac-1327">Atualização do SDK</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1327">SDK Update</span></span>
* <span data-ttu-id="7d4ac-1328">Verificação do VMappContainer removida no Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7d4ac-1329">Nome e Nome do Servidor adicionados como parâmetros para Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1330">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1331">Adicionar o parâmetro `-TemplateObject` aos cmdlets de implantação</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7d4ac-1332">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7d4ac-1333">Corrigir problema ao canalizar o resultado de `Get-AzResource` para `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7d4ac-1334">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7d4ac-1335">Corrigir problema com a alteração do tipo de dados JSON ao executar `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7d4ac-1336">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1337">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1338">Atualizando AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7d4ac-1339">Corrigindo o comportamento de um caso de borda ao criar novas configurações de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1340">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-1341">Suporte ao tipo BlockBlobStorage ao criar a conta de Armazenamento      -New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7d4ac-1342">1.4.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7d4ac-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="7d4ac-1344">Preterimento do cmdlet AddAzureASAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1345">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1346">Atualização da ajuda para Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7d4ac-1347">Validação do nome da configuração adicionada ao cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7d4ac-1348">Melhoria do tratamento de erro do cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d4ac-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d4ac-1350">Adição do CustomSubdomainName como um novo parâmetro opcional para New-AzCognitiveServicesAccount, o qual é usado para especificar o subdomínio do recurso.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1351">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1352">Correção do problema com conjuntos de parâmetros de ID</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7d4ac-1353">Atualização da Get-AzVMExtension para listar todas as extensões instaladas se o parâmetro Name não for fornecido</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7d4ac-1354">Adição dos parâmetros Tag e ResourceId para o cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7d4ac-1355">Agora o Get-AzVmssVM sem ID de instância e com InstanceView pode listar VMs do VMSS com exibição de instância.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-1357">Adição de cmdlets para itens excluídos do ADL serem enumerados e restaurados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7d4ac-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1358">Az.EventHub</span></span>
* <span data-ttu-id="7d4ac-1359">Adição da nova propriedade booleana SkipEmptyArchives para ignorar os arquivos vazios na classe CaptureDescription do EventHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7d4ac-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1360">Az.KeyVault</span></span>
* <span data-ttu-id="7d4ac-1361">Correção da marcação em Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7d4ac-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1362">Az.LogicApp</span></span>
* <span data-ttu-id="7d4ac-1363">Adição de SKU básico para contas de integração</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7d4ac-1364">Adição de tipos de XSLT 2.0, XSLT 3.0 e Liquid Map</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7d4ac-1365">Novos cmdlets para assemblies de conta de integração</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7d4ac-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7d4ac-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7d4ac-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7d4ac-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7d4ac-1370">Novos cmdlets para configuração de lote da conta de integração</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7d4ac-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7d4ac-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7d4ac-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7d4ac-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7d4ac-1375">Atualização do SDK de aplicativo lógico da versão 4.1.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7d4ac-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1376">Az.Monitor</span></span>
* <span data-ttu-id="7d4ac-1377">Atualização da ajuda para Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1378">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1379">Atualização do exemplo de ajuda para Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7d4ac-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="7d4ac-1381">Suporte adicional para fonte de dados do ApplicationInsights Get e New.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7d4ac-1382">Adição do novo tipo de “ApplicationInsights” para dar suporte às fontes de dados do ApplicationInsights de Get específico ou todos os Get do workspace determinado.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7d4ac-1383">Adição do cmdlet New-AzOperationalInsightsApplicationInsightsDataSource para criar fontes de dados usando parâmetros de recurso do Application-Insights: subscription Id, resourceGroupName e name.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1384">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1385">Correção do problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7d4ac-1386">Correção do problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7d4ac-1387">Correção do problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7d4ac-1388">Correção de bug que impede a criação repetida de KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1389">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1390">Adição de suporte para a camada de Hiperescala do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7d4ac-1391">Correção do bug em que a restauração pode falhar devido à configuração de propriedades desnecessárias na solicitação de restauração</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1392">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-1393">Correção do exemplo em Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7d4ac-1394">1.3.0 – Fevereiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1395">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1396">Atualização para a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7d4ac-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="7d4ac-1398">Disponibilidade geral do módulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1399">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1400">Extensão do AEM: Adição de suporte para discos UltraSSD e P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7d4ac-1401">Atualização da descrição da ajuda para Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7d4ac-1402">Atualização da descrição de ajuda e do exemplo para Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="7d4ac-1404">Disponibilidade geral do módulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1405">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1406">Correção da marcação dos grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7d4ac-1407">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7d4ac-1408">Correção do problema em que `Get-AzureRmRoleAssignment` não respeita -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7d4ac-1409">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1410">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1411">Adição do Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7d4ac-1412">Correção do problema em que não estar conectado à conta do Azure resultaria na exceção nullref ao executar cmdlets do SQL</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7d4ac-1413">Correção da exceção de referência nula em Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7d4ac-1414">1.2.1 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1415">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1416">Versão com a versão correta de autenticação</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7d4ac-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="7d4ac-1418">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="7d4ac-1420">Versão com a dependência de autenticação atualizada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7d4ac-1421">1.2.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1422">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1423">Adição de autenticação interativa e de nome de usuário/senha somente para o Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7d4ac-1424">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d4ac-1425">Adição de mensagem de aviso no PS Core para Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7d4ac-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1426">Az.Aks</span></span>
* <span data-ttu-id="7d4ac-1427">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7d4ac-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1428">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1429">Adicionado suporte aos runbooks do Python 2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7d4ac-1430">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7d4ac-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1431">Az.Cdn</span></span>
* <span data-ttu-id="7d4ac-1432">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1433">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1434">Adição do cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7d4ac-1435">Adição do parâmetro TempDisk ao Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7d4ac-1436">Correção da mensagem de aviso do New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7d4ac-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7d4ac-1438">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7d4ac-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1439">Az.DataFactory</span></span>
* <span data-ttu-id="7d4ac-1440">Atualizada a versão do SDK do ADF .NET para 3.0.0</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-1442">Correção do problema com o ponto de extremidade do ADLS ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7d4ac-1443">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7d4ac-1444">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d4ac-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1445">Az.IotHub</span></span>
* <span data-ttu-id="7d4ac-1446">Adição do formato de codificação ao cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7d4ac-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1447">Az.KeyVault</span></span>
* <span data-ttu-id="7d4ac-1448">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1449">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1450">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1451">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1452">Correção de exemplos incorretos na documentação de referência de 'New-AzADSpCredential' e 'New-AzADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7d4ac-1453">Correção do problema em que o caminho para o parâmetro '-TemplateFile' não estava sendo resolvido antes da execução dos cmdlets de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7d4ac-1454">Az.Resources: Correção da documentação do valor padrão New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7d4ac-1455">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7d4ac-1456">Az.Resources: Correção do problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7d4ac-1457">Correção do problema de formatação com o objeto 'PSResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7d4ac-1458">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-1460">Reversão quando um certificado é adicionado ao modelo VMSS, mas uma exceção é lançada; isso é para corrigir o bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7d4ac-1461">Correção de mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1461">Fix some error messages.</span></span>
* <span data-ttu-id="7d4ac-1462">Correção da criação do cluster com o modelo do ARM padrão para New-AzServiceFabriCluster que não estava funcionando com a migração para o Az.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7d4ac-1463">Correção da adição de certificado de aplicativo/cluster somente a Conjuntos de Dimensionamento de Máquinas Virtuais que correspondem ao cluster ao verificar a ID do cluster na extensão.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7d4ac-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1464">Az.SignalR</span></span>
* <span data-ttu-id="7d4ac-1465">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1466">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1467">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d4ac-1468">Atualizada a descrição do parâmetro LicenseType com os valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7d4ac-1469">Correção da atualização de identidade da instância gerenciada que não estava funcionando quando ela era a única propriedade atualizada</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7d4ac-1470">Suporte para ordenação personalizada em instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1471">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-1472">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d4ac-1473">Obtenção de mensagem de erro detalhada ao obter/definir métrica/registro de log clássicos na Conta de Armazenamento Premium, uma vez que esta não tem suporte para métrica/registro de logs clássicos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7d4ac-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7d4ac-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7d4ac-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="7d4ac-1477">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1478">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-1479">Atualização de URLs incorretas da ajuda online</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7d4ac-1480">Correção de 'New-AzWebAppSSLBinding' para carregar o certificado para o grupo de recursos+ local corretos se o aplicativo estiver hospedado em um ASE.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7d4ac-1481">Correção de 'New-AzWebAppSSLBinding' para não substituir as marcas que associam um certificado SSL a um aplicativo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7d4ac-1482">1.1.0 – Janeiro de 2019</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1483">Az.Accounts</span></span>
* <span data-ttu-id="7d4ac-1484">Adição de escopo 'Local' ao Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1485">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1486">Um nome agora é opcional no conjunto de parâmetros de ID para Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7d4ac-1487">Atualização da descrição de ID em arquivos de ajuda</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7d4ac-1488">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-1490">Atualização da versão do SDK do plano de dados para 1.1.14 para correções do SDK.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7d4ac-1491">Correção do tratamento do acesstime negativo e modificationtime para getfilestatus e liststatus; correção do token de cancelamento assíncrono</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7d4ac-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1492">Az.EventGrid</span></span>
* <span data-ttu-id="7d4ac-1493">Atualização para usar a versão de API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7d4ac-1494">Atualização dos seguintes cmdlets para dar suporte a novo cenário na versão de API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7d4ac-1495">New-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7d4ac-1496">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7d4ac-1497">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7d4ac-1498">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7d4ac-1499">Update-AzureRmEventGridSubscription: Adição de novos parâmetros opcionais para especificar:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7d4ac-1500">Evento Vida útil</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7d4ac-1501">Número máximo de tentativas de entrega para os eventos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7d4ac-1502">Ponto de extremidade de mensagens mortas</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="7d4ac-1503">Adição de novos valores de enumeração (ou seja, storageQueue e hybridConnection) para a opção EndpointType nos cmdlets New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7d4ac-1504">A exibição de mensagem de aviso ao criar ou atualizar a assinatura de evento deve envolver a ação manual do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7d4ac-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1505">Az.IotHub</span></span>
* <span data-ttu-id="7d4ac-1506">Atualizado para a versão mais recente do SDK do IotHub</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7d4ac-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1507">Az.LogicApp</span></span>
* <span data-ttu-id="7d4ac-1508">Get-AzLogicApp lista tudo sem especificação de nome</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1509">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1510">Correção do problema de conjunto de parâmetros ao fornecer parâmetros '-ODataQuery' e '-ResourceId' para 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7d4ac-1511">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7d4ac-1512">Correção do tratamento do parâmetro -Custom em New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7d4ac-1513">Correção do erro de digitação na documentação de New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7d4ac-1514">Obrigação do uso do parâmetro '-MailNickname' para 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7d4ac-1515">Mais informações podem ser obtidas aqui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7d4ac-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1516">Az.SignalR</span></span>
* <span data-ttu-id="7d4ac-1517">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1518">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1519">Conversão da dependência de cliente de gerenciamento de armazenamento para a implementação de SDK comum.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7d4ac-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1520">Az.Storage</span></span>
* <span data-ttu-id="7d4ac-1521">Definição do StorageAccountName do contexto de armazenamento como o Nome de conta de armazenamento real quando ele é criado com o Token Sas, OAuth ou Anonymous</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7d4ac-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="7d4ac-1523">Criação do Token Sas do Objeto de instantâneo de blobs com o parâmetro '-FullUri'; correção do Uri de retorno para ser o Uri do instantâneo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7d4ac-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1525">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-1526">Correção de um bug de análise de data no 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7d4ac-1527">Correção do problema de compatibilidade com versões anteriores do módulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7d4ac-1528">1.0.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7d4ac-1529">Geral</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1529">General</span></span>

- <span data-ttu-id="7d4ac-1530">Disponibilidade geral do Módulo Az</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="7d4ac-1531">Ajuda online para cada módulo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1531">Online help for each module</span></span>
- <span data-ttu-id="7d4ac-1532">Para obter mais detalhes e um roteiro, confira a [página de Comunicado do Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7d4ac-1533">Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter informações sobre como migrar do AzureRM</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7d4ac-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1534">Az.Accounts</span></span>
- <span data-ttu-id="7d4ac-1535">Alterado de Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="7d4ac-1536">Corrigidos os formatos de tabela para tipos de perfil e contexto</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7d4ac-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="7d4ac-1538">Correções para #7002</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1538">Fixes for #7002</span></span>
- <span data-ttu-id="7d4ac-1539">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7d4ac-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1540">Az.Batch</span></span>
- <span data-ttu-id="7d4ac-1541">Adicionada a capacidade de ver qual versão do agente de nó do Lote do Azure está em execução em cada uma das VMs em um pool, através da nova propriedade `NodeAgentInformation` em `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7d4ac-1542">O padrão `Caching` para `PSDataDisk` agora é `ReadWrite` em vez de `None`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7d4ac-1543">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7d4ac-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1544">Az.Billing</span></span>
- <span data-ttu-id="7d4ac-1545">Combina os cmdlets Billing, Consumption e UsageAggregates. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7d4ac-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="7d4ac-1547">Adiciona complementos para SkuName e Typem disponíveis na operação New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7d4ac-1548">Removido o conjunto de parâmetros GetSkusWithAccountParamSetName de Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7d4ac-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="7d4ac-1550">Adicionado suporte para ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7d4ac-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7d4ac-1552">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="7d4ac-1554">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7d4ac-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1555">Az.Monitor</span></span>
- <span data-ttu-id="7d4ac-1556">Az.Insights renomeado para Az.Monitor e outras pequenas alterações. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7d4ac-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1557">Az.KeyVault</span></span>
- <span data-ttu-id="7d4ac-1558">Removida a propriedade “PurgeDisabled” preterida dos tipos de saída</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7d4ac-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="7d4ac-1560">Incluídos os cmdlets do módulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7d4ac-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1561">Az.Media</span></span>
- <span data-ttu-id="7d4ac-1562">Removido o alias -Tags de New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1563">Az.Network</span></span>
<span data-ttu-id="7d4ac-1564">Adicionado suporte para a configuração de RewriteRuleSets no Gateway de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7d4ac-1565">Novos cmdlets adicionados:</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="7d4ac-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d4ac-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d4ac-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d4ac-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d4ac-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7d4ac-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7d4ac-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7d4ac-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7d4ac-1574">Cmdlets atualizados com o parâmetro opcional -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7d4ac-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7d4ac-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7d4ac-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7d4ac-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7d4ac-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7d4ac-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Adicionado suporte para KeyVault para o Gateway de Aplicativo usando Identity.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7d4ac-1581">Cmdlets atualizados com o parâmetro opcional KeyVaultSecretId-, - KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7d4ac-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7d4ac-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7d4ac-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7d4ac-1585">Cmdlet New-AzApplicationGateway atualizado com o parâmetro opcional -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7d4ac-1586">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7d4ac-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="7d4ac-1588">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7d4ac-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1589">Az.Profile</span></span>
- <span data-ttu-id="7d4ac-1590">Nome do módulo alterado para Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="7d4ac-1592">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7d4ac-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1593">Az.Resources</span></span>
- <span data-ttu-id="7d4ac-1594">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="7d4ac-1596">Suporte para especificação de certificado pelo nome comum e impressão digital</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7d4ac-1597">Alterações de falha pequenas. Consulte o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7d4ac-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="7d4ac-1599">Disponibilidade Geral de cmdlets do PowerShell para o SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7d4ac-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1600">Az.Sql</span></span>
- <span data-ttu-id="7d4ac-1601">Adicionado novos tipos de detecção Data_Exfiltration e Unsafe_Action aos cmdlets da detecção de ameaças</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7d4ac-1602">Exemplos de documentação atualizados para cmdlets de auditoria do SQL</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7d4ac-1603">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7d4ac-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1604">Az.Storage</span></span>
- <span data-ttu-id="7d4ac-1605">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1606">Az.Websites</span></span>
- <span data-ttu-id="7d4ac-1607">Alterações de falha pequenas. Confira o [Guia de Migração](https://aka.ms/azps-migration-guide) para obter detalhes</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7d4ac-1608">0.7.0 - Dezembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7d4ac-1609">Geral</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1609">General</span></span>

* <span data-ttu-id="7d4ac-1610">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7d4ac-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1611">Az.Compute</span></span>

* <span data-ttu-id="7d4ac-1612">Adicionado suporte para UltraSSD e imagens da Galeria nos conjuntos de parâmetro simples para cmdlets `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="7d4ac-1614">Corrigida a barra à direita do domínio da conta do ADLS</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7d4ac-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="7d4ac-1616">Corrigidos alguns links desfeitos</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="7d4ac-1617">Nos artigos New-AzureRmFrontDoor e Set-AzureRmFrontDoor, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7d4ac-1618">No artigo New-AzureRmFrontDoorManagedRuleObject, foi corrigido o link para o artigo do cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7d4ac-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="7d4ac-1620">Adicionadas validações do lado do cliente para operações de restauração do Compartilhamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7d4ac-1621">Agora storageAccountName e storageAccountResourceGroupName são opcionais para restauração do AFS.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7d4ac-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1622">Az.Resources</span></span>

* <span data-ttu-id="7d4ac-1623">Correção para https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7d4ac-1624">Atualizado Get-AzureRmRoleAssignment para usar o escopo de assinatura, se ele for fornecido ao solicitar aos administradores clássicos.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7d4ac-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1625">Az.Sql</span></span>

* <span data-ttu-id="7d4ac-1626">Pequenas alterações para a futura transição de AzureRM para Az</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7d4ac-1627">Corrigido o problema com o uso de Get-AzureRmSqlDatabaseVulnerabilityAssessment com núcleo DotNet</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7d4ac-1628">Documentação modificada de mensagens de Ajuda relacionadas aos cmdlets de Auditoria do SQL.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7d4ac-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1629">Az.Storage</span></span>

* <span data-ttu-id="7d4ac-1630">Adicionado -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7d4ac-1631">Corrigido o problema em que o cmdlet Copy File não podia reutilizar o contexto de origem no destino quando a entrada não era -DestContext</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7d4ac-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7d4ac-1633">Suporte para a Configuração do Site Estático</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="7d4ac-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7d4ac-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1636">Az.Websites</span></span>

* <span data-ttu-id="7d4ac-1637">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7d4ac-1638">Novo parâmetro (-AzureStoragePath) adicionado para especificar caminhos do Armazenamento do Azure que serão montados em aplicativos de contêiner do Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7d4ac-1639">Use a saída do novo cmdlet New-AzureRmWebAppAzureStoragePath como um parâmetro para definir os caminhos do Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7d4ac-1640">0.6.1 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7d4ac-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="7d4ac-1642">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7d4ac-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1643">Az.Automation</span></span>
* <span data-ttu-id="7d4ac-1644">Cmdlets de Automação do Azure baseados no Swagger</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7d4ac-1645">Cmdlets de Gerenciamento de Atualizações Adicionados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7d4ac-1646">Cmdlets de Controle do Código-fonte adicionados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7d4ac-1647">Cmdlet Remove-AzureRmAutomationHybridWorkerGroup adicionado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7d4ac-1648">Corrigido o comando de Nó do Registro de DSC</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7d4ac-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1649">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1650">Problema de identidade corrigido para a identidade SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7d4ac-1651">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7d4ac-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="7d4ac-1653">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7d4ac-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7d4ac-1655">atualizar a descrição de exemplos dos cmdlets do marketplace</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1656">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1657">Cmdlets New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError adicionados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7d4ac-1658">ICMP adicionado aos Protocolos de Rede do AzureFirewall com suporte</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7d4ac-1659">Atualizar cmdlet Test-AzureRmNetworkWatcherConnectivity, adicionar validação no id de destino, endereço e porta.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7d4ac-1660">Corrigir problemas com o uso da memória no mapa VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7d4ac-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7d4ac-1662">Corrigir para modificar a política para um compartilhamento de arquivos protegido.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7d4ac-1663">Fuso horário da política convertido em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7d4ac-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7d4ac-1665">Exemplo corrigido em New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7d4ac-1666">Atualizar as dependências para o problema de mapeamento do tipo</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7d4ac-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1667">Az.Relay</span></span>
* <span data-ttu-id="7d4ac-1668">Parâmetro opcional -KeyValue adicionado ao cmdlet New-AzureRmRelayKey, que permite ao usuário fornecer o KeyValue.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7d4ac-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1669">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1670">Atualizar documentação de ajuda para a identidade do recurso relacionada aos parâmetros em `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7d4ac-1671">Adicionar um exemplo para New-AzureRmPolicyDefinition que usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7d4ac-1672">Corrigir para permitir a preservação das letras maiúsculas e minúsculas nas chaves de Marca em NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-1674">Adicionar mensagens preteridas para futuras alterações da falha</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7d4ac-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1675">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1676">Novos cmdlets adicionados para operações CRUD na Instância Gerenciada do Banco de Dados SQL do Azure e no Banco de Dados SQL do Azure Gerenciado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7d4ac-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d4ac-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d4ac-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d4ac-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7d4ac-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7d4ac-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7d4ac-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7d4ac-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7d4ac-1685">Gerenciamento da Política de Auditoria Estendida Habilitado em um servidor ou banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7d4ac-1686">Um novo parâmetro (PredicateExpression) foi adicionado para habilitar a filtragem dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7d4ac-1687">Os cmdlets foram modificadas para usar os clientes SQL, em vez dos clientes herdados.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7d4ac-1688">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7d4ac-1689">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7d4ac-1690">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7d4ac-1691">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7d4ac-1692">Problema corrigido ao usar Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings com o conjunto de parâmetros de nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7d4ac-1693">0.5.0 - Novembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7d4ac-1694">Geral</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1694">General</span></span>
* <span data-ttu-id="7d4ac-1695">Adicionados Complementos de Recursos para vários cmdlets principais - eles permitem alternar entre as abas dos nomes dos recursos existentes ao invocar os cmdlets interativamente</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7d4ac-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1696">Az.Profile</span></span>
* <span data-ttu-id="7d4ac-1697">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7d4ac-1698">Renomear o parâmetro TenantId no cmdlet Connect-AzAccount para Tenant e adicionar um alias para TenantId</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7d4ac-1699">Atualizada a descrição de TenantId atualizada para Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7d4ac-1700">Corrigir a mensagem de erro de logon com falha ao fornecer o domínio de locatário</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7d4ac-1701">Corrigir o problema com o conflitos de nome do contexto para contas sem assinaturas no locatário</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7d4ac-1702">Corrigir o problema com pontos de extremidade DataLake ao usar o MSI</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7d4ac-1703">Corrigir o problema em que “Disconnect-AzAccount” seria lançado quando não conectado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7d4ac-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d4ac-1705">Adicionada a operação Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1706">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1707">Adicionar cmdlets Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7d4ac-1708">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7d4ac-1709">Os valores de opção -BootstrapOptions e -JsonAttribute do SetAzVMChefExtension corrigidos não estão de acordo com a configuração no formato json.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-1711">Atualizar o pacote de DataLake para 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7d4ac-1712">Adicionar o padrão de Simultaneidade às operações multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7d4ac-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1713">Az.Insights</span></span>
* <span data-ttu-id="7d4ac-1714">Correção do problema #7267 (área de dimensionamento automático)</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7d4ac-1715">Problemas ao criar uma nova regra de dimensionamento automático não definindo corretamente os parâmetros enumerados (sempre os defina para o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7d4ac-1716">Corrigido o problema #7513 [Insights] em que Set-AzDiagnosticSetting requer a especificação explícita das categorias durante a criação da configuração</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7d4ac-1717">Agora o cmdlet não requer uma indicação explícita das categorias para habilitar durante a criação, ou seja, ele funciona conforme está documentado</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1718">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1719">Alterado o PeeringType para ser um parâmetro obrigatório para os seguintes cmdlets:-</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7d4ac-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7d4ac-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7d4ac-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7d4ac-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7d4ac-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7d4ac-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7d4ac-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="7d4ac-1727">Adicionados cmdlets de correção de política</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1728">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1729">Correção para https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7d4ac-1730">Permitir a listagem de recursos usando o parâmetro “-ResourceId” para “Get-AzResource”</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7d4ac-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="7d4ac-1732">Adicionada propriedade somente leitura de MigrationState para PSServiceBusMigrationConfigurationAttributes, o que ajudará a conhecer o estado de Migração.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7d4ac-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="7d4ac-1734">Correção do certificado de adição para Vmss do Linux.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7d4ac-1735">Corrigido “Add-AzServiceFabricClusterCertificate”</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7d4ac-1736">Usando a impressão digital correta do novo certificado (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7d4ac-1737">Exibir exceções corretamente (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7d4ac-1738">Corrigido “Update-AzServiceFabricDurability” para atualizar a configuração do cluster antes de iniciar a operação CreateOrUpdate do Vmss.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7d4ac-1739">0.4.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7d4ac-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1740">Az.Profile</span></span>
* <span data-ttu-id="7d4ac-1741">Corrigido o problema com Get-AzSubscription no CloudShell</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7d4ac-1742">Atualizar código comum para usar a versão mais recente do ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1743">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1744">Adicionados novos tamanhos à lista de permissões de tamanhos de VM para o qual a aceleração de rede será ativada ao usar o conjunto de parâmetros simples para “New-AzVm”</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7d4ac-1745">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7d4ac-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="7d4ac-1747">Adicionar suporte às Regras da Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7d4ac-1748">Get-AzDataLakeStoreVirtualNetworkRule: Obtém ou lista a regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7d4ac-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adiciona uma regra da rede virtual à conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7d4ac-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifica a regra da rede virtual especificada na conta do Data Lake Store especificada.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7d4ac-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Exclui uma regra da rede virtual do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1752">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1753">Atualizar o cmdlet Test-AzNetworkWatcherConnectivity, passar o valor de protocolo para o back-end.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7d4ac-1754">Adicionado o finalizador do argumento ResourceName para todos os cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1755">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1756">Corrigido o problema em que Get-AzRoleDefinition gera uma exceção ininteligível (quando o perfil padrão não tem nenhuma assinatura nele e nenhum escopo for especificado) com a adição de uma exceção significativa no cenário.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7d4ac-1757">Também defina o conjunto de parâmetros padrão como 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7d4ac-1758">0.3.0 - Outubro de 2018</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7d4ac-1759">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1759">Azure.Storage</span></span>
* <span data-ttu-id="7d4ac-1760">Correção de Copiar Blob/O arquivo não copiará os metadados quando o destino tiver problemas de metadados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7d4ac-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7d4ac-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7d4ac-1763">O suporte para obter o uso dos recursos de armazenamento de um local específico e adicionar mensagem de aviso para obter o uso dos recursos de armazenamento global é obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7d4ac-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7d4ac-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="7d4ac-1766">Suporte para Get-AzCognitiveServicesAccountSkus sem uma conta existente.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7d4ac-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1767">Az.Compute</span></span>
* <span data-ttu-id="7d4ac-1768">Corrigido Get-AzVM -ResourceGroupName <rg> para retornar mais de 50 resultados se necessário</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7d4ac-1769">Adicionado um exemplo de “SimpleParameterSet” para a ajuda do cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7d4ac-1770">Corrigido um erro de digitação na mensagem de progresso do Azure Disk Encryption</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7d4ac-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7d4ac-1772">Atualizada a versão do SDK do ADF .NET para 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7d4ac-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1773">Az.Network</span></span>
* <span data-ttu-id="7d4ac-1774">Adicionada a funcionalidade NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7d4ac-1775">Novos cmdlets adicionados</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1775">new cmdlets added</span></span>
    - <span data-ttu-id="7d4ac-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d4ac-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d4ac-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d4ac-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7d4ac-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7d4ac-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7d4ac-1782">Link de associação de serviço adicionado no modelo de sub-rede</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7d4ac-1783">Adicionados os cmdlets New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7d4ac-1784">Adicionados os cmdlets Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7d4ac-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1785">Az.RedisCache</span></span>
* <span data-ttu-id="7d4ac-1786">Permissão de qualquer cadeia de caracteres como parâmetro Size de agora em diante.</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7d4ac-1787">Adição do P5 na pop-up PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7d4ac-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1788">Az.Resources</span></span>
* <span data-ttu-id="7d4ac-1789">Adicionado o parâmetro -Mode ausente a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7d4ac-1790">Corrigido o bug do cmdlet Get-AzProviderOperation para operações com a Origem que contém o Usuário</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7d4ac-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1791">Az.Sql</span></span>
* <span data-ttu-id="7d4ac-1792">Corrigido o problema no qual alguns cmdlets de backup não reconheciam a assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7d4ac-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1793">Az.Websites</span></span>
* <span data-ttu-id="7d4ac-1794">Novo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl: obtém a URL do Webhook de Implantação Contínua do Contêiner</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7d4ac-1795">Novos cmdlets New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession: iniciam a sessão remota do PowerShell em um aplicativo contêiner do Windows</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7d4ac-1796">0.2.0 - Setembro de 2018</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7d4ac-1797">Versão Inicial</span><span class="sxs-lookup"><span data-stu-id="7d4ac-1797">Initial Release</span></span>